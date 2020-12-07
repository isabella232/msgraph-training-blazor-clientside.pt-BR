---
ms.openlocfilehash: 9029486df6b08042681c0a1a67b156cbbd0381a0
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584525"
---
# <a name="how-to-run-the-completed-project"></a><span data-ttu-id="7b53e-101">Como executar o projeto concluído</span><span class="sxs-lookup"><span data-stu-id="7b53e-101">How to run the completed project</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7b53e-102">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7b53e-102">Prerequisites</span></span>

<span data-ttu-id="7b53e-103">Para executar o projeto concluído nessa pasta, você precisará do seguinte:</span><span class="sxs-lookup"><span data-stu-id="7b53e-103">To run the completed project in this folder, you need the following:</span></span>

- <span data-ttu-id="7b53e-104">O [SDK do .NET Core](https://dotnet.microsoft.com/download) instalado em sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7b53e-104">The [.NET Core SDK](https://dotnet.microsoft.com/download) installed on your development machine.</span></span> <span data-ttu-id="7b53e-105">(**Observação:** este tutorial foi escrito com o .NET Core SDK versão 3.1.402.</span><span class="sxs-lookup"><span data-stu-id="7b53e-105">(**Note:** This tutorial was written with .NET Core SDK version 3.1.402.</span></span> <span data-ttu-id="7b53e-106">As etapas deste guia podem funcionar com outras versões, mas que não foram testadas.</span><span class="sxs-lookup"><span data-stu-id="7b53e-106">The steps in this guide may work with other versions, but that has not been tested.)</span></span>
- <span data-ttu-id="7b53e-107">Uma conta pessoal da Microsoft com uma caixa de correio no Outlook.com ou uma conta corporativa ou de estudante da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b53e-107">Either a personal Microsoft account with a mailbox on Outlook.com, or a Microsoft work or school account.</span></span>

<span data-ttu-id="7b53e-108">Se você não tem uma conta da Microsoft, há algumas opções para obter uma conta gratuita:</span><span class="sxs-lookup"><span data-stu-id="7b53e-108">If you don't have a Microsoft account, there are a couple of options to get a free account:</span></span>

- <span data-ttu-id="7b53e-109">Você pode [se inscrever para uma nova conta pessoal da Microsoft](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1).</span><span class="sxs-lookup"><span data-stu-id="7b53e-109">You can [sign up for a new personal Microsoft account](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1).</span></span>
- <span data-ttu-id="7b53e-110">Você pode [se inscrever no programa para desenvolvedores do office 365](https://developer.microsoft.com/office/dev-program) para obter uma assinatura gratuita do Office 365.</span><span class="sxs-lookup"><span data-stu-id="7b53e-110">You can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

## <a name="register-a-web-application-with-the-azure-active-directory-admin-center"></a><span data-ttu-id="7b53e-111">Registrar um aplicativo Web com o centro de administração do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7b53e-111">Register a web application with the Azure Active Directory admin center</span></span>

1. <span data-ttu-id="7b53e-112">Abra um navegador e navegue até o [centro de administração do Azure Active Directory](https://aad.portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="7b53e-112">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com).</span></span> <span data-ttu-id="7b53e-113">Faça logon usando uma **conta pessoal** (também conhecida como Conta da Microsoft) ou **Conta Corporativa ou de Estudante**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-113">Login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="7b53e-114">Selecione **Azure Active Directory** na navegação esquerda e selecione **Registros de aplicativos** em **Gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-114">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

    ![<span data-ttu-id="7b53e-115">Uma captura de tela dos registros de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7b53e-115">A screenshot of the App registrations</span></span> ](../tutorial/images/aad-portal-app-registrations.png)

1. <span data-ttu-id="7b53e-116">Selecione **Novo registro**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-116">Select **New registration**.</span></span> <span data-ttu-id="7b53e-117">Na página **Registrar um aplicativo**, defina os valores da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="7b53e-117">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="7b53e-118">Defina **Nome** para `Blazor Graph Tutorial`.</span><span class="sxs-lookup"><span data-stu-id="7b53e-118">Set **Name** to `Blazor Graph Tutorial`.</span></span>
    - <span data-ttu-id="7b53e-119">Defina **Tipos de conta com suporte** para **Contas em qualquer diretório organizacional e contas pessoais da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-119">Set **Supported account types** to **Accounts in any organizational directory and personal Microsoft accounts**.</span></span>
    - <span data-ttu-id="7b53e-120">Em **URI de Redirecionamento**, defina o primeiro menu suspenso para `Web` e defina o valor como `https://localhost:5001/authentication/login-callback`.</span><span class="sxs-lookup"><span data-stu-id="7b53e-120">Under **Redirect URI**, set the first drop-down to `Web` and set the value to `https://localhost:5001/authentication/login-callback`.</span></span>

    ![Uma captura de tela da página registrar um aplicativo](../tutorial/images/aad-register-an-app.png)

1. <span data-ttu-id="7b53e-122">Selecione **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-122">Select **Register**.</span></span> <span data-ttu-id="7b53e-123">Na página de **tutorial do gráfico** mais novo, copie o valor da **ID do aplicativo (cliente)** e salve-o, você precisará dele na próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="7b53e-123">On the **Blazor Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.</span></span>

    ![Uma captura de tela da ID do aplicativo do novo registro de aplicativo](../tutorial/images/aad-application-id.png)

1. <span data-ttu-id="7b53e-125">Selecione **Autenticação** em **Gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-125">Select **Authentication** under **Manage**.</span></span> <span data-ttu-id="7b53e-126">Localize a seção **Grant implícita** e habilite **tokens de acesso** e **tokens de ID**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-126">Locate the **Implicit grant** section and enable **Access tokens** and **ID tokens**.</span></span> <span data-ttu-id="7b53e-127">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-127">Select **Save**.</span></span>

## <a name="configure-the-sample"></a><span data-ttu-id="7b53e-128">Configurar o exemplo</span><span class="sxs-lookup"><span data-stu-id="7b53e-128">Configure the sample</span></span>

1. <span data-ttu-id="7b53e-129">Renomeie o **/GraphTutorial/wwwroot/appsettings.example.jsno** arquivo para **appsettings.js**.</span><span class="sxs-lookup"><span data-stu-id="7b53e-129">Rename the **/GraphTutorial/wwwroot/appsettings.example.json** file to **appsettings.json**.</span></span>

1. <span data-ttu-id="7b53e-130">Edite **appsettings.js** e substitua `YOUR_APP_ID_HERE` pela ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b53e-130">Edit **appsettings.json** and replace `YOUR_APP_ID_HERE` with your application ID.</span></span>

## <a name="run-the-sample"></a><span data-ttu-id="7b53e-131">Executar o exemplo</span><span class="sxs-lookup"><span data-stu-id="7b53e-131">Run the sample</span></span>

<span data-ttu-id="7b53e-132">Na sua CLI, execute o seguinte comando para iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b53e-132">In your CLI, run the following command to start the application.</span></span>

```Shell
dotnet run
```
