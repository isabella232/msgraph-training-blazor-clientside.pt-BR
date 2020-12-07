---
ms.openlocfilehash: 723f1d08b9d1085d47d0d5fac71da5371badc3d0
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584510"
---
<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="514ca-101">Nesta seção, você adicionará a capacidade de criar eventos no calendário do usuário.</span><span class="sxs-lookup"><span data-stu-id="514ca-101">In this section you will add the ability to create events on the user's calendar.</span></span>

1. <span data-ttu-id="514ca-102">Crie um novo arquivo no diretório **./Pages** chamado **NewEvent. Razor** e adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="514ca-102">Create a new file in the **./Pages** directory named **NewEvent.razor** and add the following code.</span></span>

    :::code language="razor" source="../demo/GraphTutorial/Pages/NewEvent.razor" id="NewEventFormSnippet":::

    <span data-ttu-id="514ca-103">Isso adiciona um formulário à página para que o usuário possa inserir valores para o novo evento.</span><span class="sxs-lookup"><span data-stu-id="514ca-103">This adds a form to the page so the user can enter values for the new event.</span></span>

1. <span data-ttu-id="514ca-104">Adicione o código a seguir ao final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="514ca-104">Add the following code to the end of the file.</span></span>

    :::code language="razor" source="../demo/GraphTutorial/Pages/NewEvent.razor" id="NewEventCodeSnippet":::

    <span data-ttu-id="514ca-105">Considere o que esse código faz.</span><span class="sxs-lookup"><span data-stu-id="514ca-105">Consider what this code does.</span></span>

    - <span data-ttu-id="514ca-106">`OnInitializedAsync`Ele obtém o fuso horário do usuário autenticado.</span><span class="sxs-lookup"><span data-stu-id="514ca-106">In `OnInitializedAsync` it gets the authenticated user's time zone.</span></span>
    - <span data-ttu-id="514ca-107">`CreateEvent`Ele inicializa um novo objeto **Event** usando os valores do formulário.</span><span class="sxs-lookup"><span data-stu-id="514ca-107">In `CreateEvent` it initializes a new **Event** object using the values from the form.</span></span>
    - <span data-ttu-id="514ca-108">Ele usa o SDK do Graph para adicionar o evento ao calendário do usuário.</span><span class="sxs-lookup"><span data-stu-id="514ca-108">It uses the Graph SDK to add the event to the user's calendar.</span></span>

1. <span data-ttu-id="514ca-109">Salve todas as suas alterações e reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="514ca-109">Save all of your changes and restart the app.</span></span> <span data-ttu-id="514ca-110">Na página **calendário** , selecione **novo evento**.</span><span class="sxs-lookup"><span data-stu-id="514ca-110">On the **Calendar** page, select **New event**.</span></span> <span data-ttu-id="514ca-111">Preencha o formulário e escolha **criar**.</span><span class="sxs-lookup"><span data-stu-id="514ca-111">Fill in the form and choose **Create**.</span></span>

    ![Uma captura de tela do novo formulário de evento](images/create-event.png)
