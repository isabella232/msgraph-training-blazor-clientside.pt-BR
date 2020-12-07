---
ms.openlocfilehash: 33bdb86a4a4af997c8ca522e23ec2f883fdeda88
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584532"
---
<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="bdbc1-101">Nesta seção, você incorporará o Microsoft Graph ao aplicativo para obter um modo de exibição do calendário do usuário para a semana atual.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-101">In this section you will further incorporate Microsoft Graph into the application to get a view of the user's calendar for the current week.</span></span>

## <a name="get-a-calendar-view"></a><span data-ttu-id="bdbc1-102">Obter um modo de exibição de calendário</span><span class="sxs-lookup"><span data-stu-id="bdbc1-102">Get a calendar view</span></span>

1. <span data-ttu-id="bdbc1-103">Crie um novo arquivo no diretório **./Pages** chamado **Calendar. Razor** e adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-103">Create a new file in the **./Pages** directory named **Calendar.razor** and add the following code.</span></span>

    ```razor
    @page "/calendar"
    @using Microsoft.Graph
    @using TimeZoneConverter

    @inject GraphTutorial.Graph.GraphClientFactory clientFactory

    <AuthorizeView>
        <Authorized>
            <!-- Temporary JSON dump of events -->
            <code>@graphClient.HttpProvider.Serializer.SerializeObject(events)</code>
        </Authorized>
        <NotAuthorized>
            <RedirectToLogin />
        </NotAuthorized>
    </AuthorizeView>

    @code{
        [CascadingParameter]
        private Task<AuthenticationState> authenticationStateTask { get; set; }

        private GraphServiceClient graphClient;
        private IList<Event> events = new List<Event>();
        private string dateTimeFormat;
    }
    ```

1. <span data-ttu-id="bdbc1-104">Adicione o código a seguir na `@code{}` seção.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-104">Add the following code inside the `@code{}` section.</span></span>

    :::code language="csharp" source="../demo/GraphTutorial/Pages/Calendar.razor" id="GetEventsSnippet":::

    <span data-ttu-id="bdbc1-105">Considere o que esse código faz.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-105">Consider what this code does.</span></span>

    - <span data-ttu-id="bdbc1-106">Ele obtém o fuso horário, o formato de data e o formato de hora do usuário atual das declarações personalizadas adicionadas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-106">It gets the current user's time zone, date format, and time format from the custom claims added to the user.</span></span>
    - <span data-ttu-id="bdbc1-107">Ele calcula o início e o fim da semana atual no fuso horário preferencial do usuário.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-107">It calculates the start and end of the current week in the user's preferred time zone.</span></span>
    - <span data-ttu-id="bdbc1-108">Ele obtém uma visão de calendário do Microsoft Graph para a semana atual.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-108">It gets a calendar view from Microsoft Graph for the current week.</span></span>
        - <span data-ttu-id="bdbc1-109">Inclui o `Prefer: outlook.timezone` cabeçalho para fazer com que o Microsoft Graph retorne as `start` `end` Propriedades e no fuso horário especificado.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-109">It includes the `Prefer: outlook.timezone` header to cause Microsoft Graph to return the `start` and `end` properties in the specified time zone.</span></span>
        - <span data-ttu-id="bdbc1-110">Ele usa `Top(50)` para solicitar até 50 eventos na resposta.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-110">It uses `Top(50)` to request up to 50 events in the response.</span></span>
        - <span data-ttu-id="bdbc1-111">Ele usa `Select(u => new {})` para solicitar apenas as propriedades usadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-111">It uses `Select(u => new {})` to request just the properties used by the app.</span></span>
        - <span data-ttu-id="bdbc1-112">Ele usa `OrderBy("start/dateTime")` para classificar os resultados por hora de início.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-112">It uses `OrderBy("start/dateTime")` to sort the results by start time.</span></span>

1. <span data-ttu-id="bdbc1-113">Salve todas as suas alterações e reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-113">Save all of your changes and restart the app.</span></span> <span data-ttu-id="bdbc1-114">Escolha o item de navegação do **calendário** .</span><span class="sxs-lookup"><span data-stu-id="bdbc1-114">Choose the **Calendar** nav item.</span></span> <span data-ttu-id="bdbc1-115">O aplicativo exibe uma representação JSON dos eventos retornados do Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-115">The app displays a JSON representation of the events returned from Microsoft Graph.</span></span>

## <a name="display-the-results"></a><span data-ttu-id="bdbc1-116">Exibir os resultados</span><span class="sxs-lookup"><span data-stu-id="bdbc1-116">Display the results</span></span>

<span data-ttu-id="bdbc1-117">Agora você pode substituir o despejo JSON por algo mais amigável.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-117">Now you can replace the JSON dump with something more user-friendly.</span></span>

1. <span data-ttu-id="bdbc1-118">Adicione a função a seguir na `@code{}` seção.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-118">Add the following function inside the `@code{}` section.</span></span>

    :::code language="csharp" source="../demo/GraphTutorial/Pages/Calendar.razor" id="FormatDateSnippet":::

    <span data-ttu-id="bdbc1-119">Este código usa uma cadeia de caracteres de data ISO 8601 e a converte no formato de data e hora preferencial do usuário.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-119">This code takes an ISO 8601 date string and converts it into the user's preferred date and time format.</span></span>

1. <span data-ttu-id="bdbc1-120">Substitua o `<code>` elemento dentro do `<Authorized>` elemento com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-120">Replace the `<code>` element inside the `<Authorized>` element with the following.</span></span>

    :::code language="razor" source="../demo/GraphTutorial/Pages/Calendar.razor" id="CalendarViewSnippet":::

    <span data-ttu-id="bdbc1-121">Isso cria uma tabela dos eventos retornados pelo Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-121">This creates a table of the events returned by Microsoft Graph.</span></span>

1. <span data-ttu-id="bdbc1-122">Salve suas alterações e reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-122">Save your changes and restart the app.</span></span> <span data-ttu-id="bdbc1-123">Agora, a página de **calendário** renderiza uma tabela de eventos.</span><span class="sxs-lookup"><span data-stu-id="bdbc1-123">Now the **Calendar** page renders a table of events.</span></span>

    ![Uma captura de tela do aplicativo mostrando uma tabela de eventos](images/calendar-view.png)
