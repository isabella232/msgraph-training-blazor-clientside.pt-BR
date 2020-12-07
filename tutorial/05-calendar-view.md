---
ms.openlocfilehash: 33bdb86a4a4af997c8ca522e23ec2f883fdeda88
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584532"
---
<!-- markdownlint-disable MD002 MD041 -->

Nesta seção, você incorporará o Microsoft Graph ao aplicativo para obter um modo de exibição do calendário do usuário para a semana atual.

## <a name="get-a-calendar-view"></a>Obter um modo de exibição de calendário

1. Crie um novo arquivo no diretório **./Pages** chamado **Calendar. Razor** e adicione o código a seguir.

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

1. Adicione o código a seguir na `@code{}` seção.

    :::code language="csharp" source="../demo/GraphTutorial/Pages/Calendar.razor" id="GetEventsSnippet":::

    Considere o que esse código faz.

    - Ele obtém o fuso horário, o formato de data e o formato de hora do usuário atual das declarações personalizadas adicionadas ao usuário.
    - Ele calcula o início e o fim da semana atual no fuso horário preferencial do usuário.
    - Ele obtém uma visão de calendário do Microsoft Graph para a semana atual.
        - Inclui o `Prefer: outlook.timezone` cabeçalho para fazer com que o Microsoft Graph retorne as `start` `end` Propriedades e no fuso horário especificado.
        - Ele usa `Top(50)` para solicitar até 50 eventos na resposta.
        - Ele usa `Select(u => new {})` para solicitar apenas as propriedades usadas pelo aplicativo.
        - Ele usa `OrderBy("start/dateTime")` para classificar os resultados por hora de início.

1. Salve todas as suas alterações e reinicie o aplicativo. Escolha o item de navegação do **calendário** . O aplicativo exibe uma representação JSON dos eventos retornados do Microsoft Graph.

## <a name="display-the-results"></a>Exibir os resultados

Agora você pode substituir o despejo JSON por algo mais amigável.

1. Adicione a função a seguir na `@code{}` seção.

    :::code language="csharp" source="../demo/GraphTutorial/Pages/Calendar.razor" id="FormatDateSnippet":::

    Este código usa uma cadeia de caracteres de data ISO 8601 e a converte no formato de data e hora preferencial do usuário.

1. Substitua o `<code>` elemento dentro do `<Authorized>` elemento com o seguinte.

    :::code language="razor" source="../demo/GraphTutorial/Pages/Calendar.razor" id="CalendarViewSnippet":::

    Isso cria uma tabela dos eventos retornados pelo Microsoft Graph.

1. Salve suas alterações e reinicie o aplicativo. Agora, a página de **calendário** renderiza uma tabela de eventos.

    ![Uma captura de tela do aplicativo mostrando uma tabela de eventos](images/calendar-view.png)
