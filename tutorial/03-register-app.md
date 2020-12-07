---
ms.openlocfilehash: 766f41b3d838130a5e0b64ba22425496eecb1c71
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584531"
---
<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="c6377-101">Neste exercício, você criará um novo registro de aplicativo Web do Azure AD usando o centro de administração do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6377-101">In this exercise, you will create a new Azure AD web application registration using the Azure Active Directory admin center.</span></span>

1. <span data-ttu-id="c6377-102">Abra um navegador e navegue até o [centro de administração do Azure Active Directory](https://aad.portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="c6377-102">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com).</span></span> <span data-ttu-id="c6377-103">Faça logon usando uma **conta pessoal** (também conhecida como Conta da Microsoft) ou **Conta Corporativa ou de Estudante**.</span><span class="sxs-lookup"><span data-stu-id="c6377-103">Login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="c6377-104">Selecione **Azure Active Directory** na navegação esquerda e selecione **Registros de aplicativos** em **Gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="c6377-104">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

    ![<span data-ttu-id="c6377-105">Uma captura de tela dos registros de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6377-105">A screenshot of the App registrations</span></span> ](./images/aad-portal-app-registrations.png)

1. <span data-ttu-id="c6377-106">Selecione **Novo registro**.</span><span class="sxs-lookup"><span data-stu-id="c6377-106">Select **New registration**.</span></span> <span data-ttu-id="c6377-107">Na página **Registrar um aplicativo**, defina os valores da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="c6377-107">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="c6377-108">Defina **Nome** para `Blazor Graph Tutorial`.</span><span class="sxs-lookup"><span data-stu-id="c6377-108">Set **Name** to `Blazor Graph Tutorial`.</span></span>
    - <span data-ttu-id="c6377-109">Defina **Tipos de conta com suporte** para **Contas em qualquer diretório organizacional e contas pessoais da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="c6377-109">Set **Supported account types** to **Accounts in any organizational directory and personal Microsoft accounts**.</span></span>
    - <span data-ttu-id="c6377-110">Em **URI de Redirecionamento**, defina o primeiro menu suspenso para `Web` e defina o valor como `https://localhost:5001/authentication/login-callback`.</span><span class="sxs-lookup"><span data-stu-id="c6377-110">Under **Redirect URI**, set the first drop-down to `Web` and set the value to `https://localhost:5001/authentication/login-callback`.</span></span>

    ![Uma captura de tela da página registrar um aplicativo](./images/aad-register-an-app.png)

1. <span data-ttu-id="c6377-112">Selecione **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="c6377-112">Select **Register**.</span></span> <span data-ttu-id="c6377-113">Na página de **tutorial do gráfico** mais novo, copie o valor da **ID do aplicativo (cliente)** e salve-o, você precisará dele na próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="c6377-113">On the **Blazor Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.</span></span>

    ![Uma captura de tela da ID do aplicativo do novo registro de aplicativo](./images/aad-application-id.png)

1. <span data-ttu-id="c6377-115">Selecione **Autenticação** em **Gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="c6377-115">Select **Authentication** under **Manage**.</span></span> <span data-ttu-id="c6377-116">Localize a seção **Grant implícita** e habilite **tokens de acesso** e **tokens de ID**.</span><span class="sxs-lookup"><span data-stu-id="c6377-116">Locate the **Implicit grant** section and enable **Access tokens** and **ID tokens**.</span></span> <span data-ttu-id="c6377-117">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="c6377-117">Select **Save**.</span></span>
