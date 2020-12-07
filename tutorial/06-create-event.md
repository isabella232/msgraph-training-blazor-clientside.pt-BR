---
ms.openlocfilehash: 723f1d08b9d1085d47d0d5fac71da5371badc3d0
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584510"
---
<!-- markdownlint-disable MD002 MD041 -->

Nesta seção, você adicionará a capacidade de criar eventos no calendário do usuário.

1. Crie um novo arquivo no diretório **./Pages** chamado **NewEvent. Razor** e adicione o código a seguir.

    :::code language="razor" source="../demo/GraphTutorial/Pages/NewEvent.razor" id="NewEventFormSnippet":::

    Isso adiciona um formulário à página para que o usuário possa inserir valores para o novo evento.

1. Adicione o código a seguir ao final do arquivo.

    :::code language="razor" source="../demo/GraphTutorial/Pages/NewEvent.razor" id="NewEventCodeSnippet":::

    Considere o que esse código faz.

    - `OnInitializedAsync`Ele obtém o fuso horário do usuário autenticado.
    - `CreateEvent`Ele inicializa um novo objeto **Event** usando os valores do formulário.
    - Ele usa o SDK do Graph para adicionar o evento ao calendário do usuário.

1. Salve todas as suas alterações e reinicie o aplicativo. Na página **calendário** , selecione **novo evento**. Preencha o formulário e escolha **criar**.

    ![Uma captura de tela do novo formulário de evento](images/create-event.png)
