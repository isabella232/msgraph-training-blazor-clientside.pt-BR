---
ms.openlocfilehash: 3965884c8e0d7116f5d8a42e6aefb0dc5be94f1e
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584509"
---
<a name="open-iconic-v111"></a>[<span data-ttu-id="15f27-101">Abrir o icônico v 1.1.1</span><span class="sxs-lookup"><span data-stu-id="15f27-101">Open Iconic v1.1.1</span></span>](http://useiconic.com/open)
===========

### <a name="open-iconic-is-the-open-source-sibling-of-iconic-it-is-a-hyper-legible-collection-of-223-icons-with-a-tiny-footprintmdashready-to-use-with-bootstrap-and-foundation-view-the-collection"></a><span data-ttu-id="15f27-102">Abra icônico é o irmão de fonte aberta de [icônico](http://useiconic.com).</span><span class="sxs-lookup"><span data-stu-id="15f27-102">Open Iconic is the open source sibling of [Iconic](http://useiconic.com).</span></span> <span data-ttu-id="15f27-103">É uma coleção do Hyper-legíveis de ícones 223 com uma pequena ocupação &mdash; pronta para uso com inicialização e Fundação.</span><span class="sxs-lookup"><span data-stu-id="15f27-103">It is a hyper-legible collection of 223 icons with a tiny footprint&mdash;ready to use with Bootstrap and Foundation.</span></span> [<span data-ttu-id="15f27-104">Exibir a coleção</span><span class="sxs-lookup"><span data-stu-id="15f27-104">View the collection</span></span>](http://useiconic.com/open#icons)



## <a name="whats-in-open-iconic"></a><span data-ttu-id="15f27-105">O que há no Open icônico?</span><span class="sxs-lookup"><span data-stu-id="15f27-105">What's in Open Iconic?</span></span>

* <span data-ttu-id="15f27-106">223 ícones projetados para serem legíveis a 8 pixels</span><span class="sxs-lookup"><span data-stu-id="15f27-106">223 icons designed to be legible down to 8 pixels</span></span>
* <span data-ttu-id="15f27-107">Arquivos SVG super claros-61,8 para o conjunto inteiro</span><span class="sxs-lookup"><span data-stu-id="15f27-107">Super-light SVG files - 61.8 for the entire set</span></span> 
* <span data-ttu-id="15f27-108">SVG Sprite &mdash; a substituição moderna para fontes de ícone</span><span class="sxs-lookup"><span data-stu-id="15f27-108">SVG sprite&mdash;the modern replacement for icon fonts</span></span>
* <span data-ttu-id="15f27-109">Formatos webfont (EOT, OTF, SVG, TTF, WOFF), PNG e WebP</span><span class="sxs-lookup"><span data-stu-id="15f27-109">Webfont (EOT, OTF, SVG, TTF, WOFF), PNG and WebP formats</span></span>
* <span data-ttu-id="15f27-110">Folhas de estilo do webfont (incluindo versões de inicialização e Fundação) em formatos CSS, menos, SCSS e Stylus</span><span class="sxs-lookup"><span data-stu-id="15f27-110">Webfont stylesheets (including versions for Bootstrap and Foundation) in CSS, LESS, SCSS and Stylus formats</span></span>
* <span data-ttu-id="15f27-111">Imagens do PNG e do WebP rasterizadas no 8px, 16px, medianiz 24px, medianiz 32px, 48px e 64px.</span><span class="sxs-lookup"><span data-stu-id="15f27-111">PNG and WebP raster images in 8px, 16px, 24px, 32px, 48px and 64px.</span></span>


## <a name="getting-started"></a><span data-ttu-id="15f27-112">Introdução</span><span class="sxs-lookup"><span data-stu-id="15f27-112">Getting Started</span></span>

#### <a name="for-code-samples-and-everything-else-you-need-to-get-started-with-open-iconic-check-out-our-icons-and-reference-sections"></a><span data-ttu-id="15f27-113">Para obter exemplos de código e tudo o que você precisa para começar a usar o icônico aberto, Confira nossos [ícones](http://useiconic.com/open#icons) e seções de [referência](http://useiconic.com/open#reference) .</span><span class="sxs-lookup"><span data-stu-id="15f27-113">For code samples and everything else you need to get started with Open Iconic, check out our [Icons](http://useiconic.com/open#icons) and [Reference](http://useiconic.com/open#reference) sections.</span></span>

### <a name="general-usage"></a><span data-ttu-id="15f27-114">Uso geral</span><span class="sxs-lookup"><span data-stu-id="15f27-114">General Usage</span></span>

#### <a name="using-open-iconics-svgs"></a><span data-ttu-id="15f27-115">Usando o SVGs do icônico</span><span class="sxs-lookup"><span data-stu-id="15f27-115">Using Open Iconic's SVGs</span></span>

<span data-ttu-id="15f27-116">Gostaríamos de SVGs e achamos que eles são a maneira de exibir ícones na Web.</span><span class="sxs-lookup"><span data-stu-id="15f27-116">We like SVGs and we think they're the way to display icons on the web.</span></span> <span data-ttu-id="15f27-117">Como as icônico abertas são apenas SVGs básicas, sugerimos que você as exiba como faria com qualquer outra imagem (não esqueça o `alt` atributo).</span><span class="sxs-lookup"><span data-stu-id="15f27-117">Since Open Iconic are just basic SVGs, we suggest you display them like you would any other image (don't forget the `alt` attribute).</span></span>

```
<img src="/open-iconic/svg/icon-name.svg" alt="icon name">
```

#### <a name="using-open-iconics-svg-sprite"></a><span data-ttu-id="15f27-118">Usando o icônico de SVG do Open</span><span class="sxs-lookup"><span data-stu-id="15f27-118">Using Open Iconic's SVG Sprite</span></span>

<span data-ttu-id="15f27-119">Abrir o icônico também vem em uma entidade de grupo SVG que permite que você exiba todos os ícones no conjunto com uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="15f27-119">Open Iconic also comes in a SVG sprite which allows you to display all the icons in the set with a single request.</span></span> <span data-ttu-id="15f27-120">É como uma fonte de ícone, sem ser um ataque.</span><span class="sxs-lookup"><span data-stu-id="15f27-120">It's like an icon font, without being a hack.</span></span>

<span data-ttu-id="15f27-121">A adição de um ícone de uma entidade de conteúdo SVG é um pouco diferente do que você está acostumado, mas ainda é uma parte do bolo.</span><span class="sxs-lookup"><span data-stu-id="15f27-121">Adding an icon from an SVG sprite is a little different than what you're used to, but it's still a piece of cake.</span></span> <span data-ttu-id="15f27-122">*Dica: para tornar os seus ícones facilmente estilos, sugerimos adicionar uma classe geral à* `<svg>` *marca e um nome de classe exclusivo para cada ícone diferente na* `<use>` *marca.*</span><span class="sxs-lookup"><span data-stu-id="15f27-122">*Tip: To make your icons easily style able, we suggest adding a general class to the* `<svg>` *tag and a unique class name for each different icon in the* `<use>` *tag.*</span></span>  

```
<svg class="icon">
  <use xlink:href="open-iconic.svg#account-login" class="icon-account-login"></use>
</svg>
```

<span data-ttu-id="15f27-123">Ícones de dimensionamento só precisam de CSS básicos.</span><span class="sxs-lookup"><span data-stu-id="15f27-123">Sizing icons only needs basic CSS.</span></span> <span data-ttu-id="15f27-124">Todos os ícones estão em um formato quadrado, portanto, basta definir a `<svg>` marca com dimensões de largura e altura iguais.</span><span class="sxs-lookup"><span data-stu-id="15f27-124">All the icons are in a square format, so just set the `<svg>` tag with equal width and height dimensions.</span></span>

```
.icon {
  width: 16px;
  height: 16px;
}
```

<span data-ttu-id="15f27-125">Ícones de coloração é ainda mais fácil.</span><span class="sxs-lookup"><span data-stu-id="15f27-125">Coloring icons is even easier.</span></span> <span data-ttu-id="15f27-126">Tudo o que você precisa fazer é definir a `fill` regra na `<use>` marca.</span><span class="sxs-lookup"><span data-stu-id="15f27-126">All you need to do is set the `fill` rule on the `<use>` tag.</span></span>

```
.icon-account-login {
  fill: #f00;
}
```

<span data-ttu-id="15f27-127">Para saber mais sobre os sprites SVG, leia o [guia da Carla Coyier](http://css-tricks.com/svg-sprites-use-better-icon-fonts/).</span><span class="sxs-lookup"><span data-stu-id="15f27-127">To learn more about SVG Sprites, read [Chris Coyier's guide](http://css-tricks.com/svg-sprites-use-better-icon-fonts/).</span></span>

#### <a name="using-open-iconics-icon-font"></a><span data-ttu-id="15f27-128">Usando a fonte do ícone do Open icônico...</span><span class="sxs-lookup"><span data-stu-id="15f27-128">Using Open Iconic's Icon Font...</span></span>


##### <a name="with-bootstrap"></a><span data-ttu-id="15f27-129">... com inicialização</span><span class="sxs-lookup"><span data-stu-id="15f27-129">…with Bootstrap</span></span>

<span data-ttu-id="15f27-130">Você pode encontrar nossas folhas de estilo de Bootstrap no `font/css/open-iconic-bootstrap.{css, less, scss, styl}`</span><span class="sxs-lookup"><span data-stu-id="15f27-130">You can find our Bootstrap stylesheets in `font/css/open-iconic-bootstrap.{css, less, scss, styl}`</span></span>


```
<link href="/open-iconic/font/css/open-iconic-bootstrap.css" rel="stylesheet">
```


```
<span class="oi oi-icon-name" title="icon name" aria-hidden="true"></span>
```

##### <a name="with-foundation"></a><span data-ttu-id="15f27-131">... com base</span><span class="sxs-lookup"><span data-stu-id="15f27-131">…with Foundation</span></span>

<span data-ttu-id="15f27-132">Você pode encontrar as folhas de estilo de base no `font/css/open-iconic-foundation.{css, less, scss, styl}`</span><span class="sxs-lookup"><span data-stu-id="15f27-132">You can find our Foundation stylesheets in `font/css/open-iconic-foundation.{css, less, scss, styl}`</span></span>

```
<link href="/open-iconic/font/css/open-iconic-foundation.css" rel="stylesheet">
```


```
<span class="fi-icon-name" title="icon name" aria-hidden="true"></span>
```

##### <a name="on-its-own"></a><span data-ttu-id="15f27-133">... por conta própria</span><span class="sxs-lookup"><span data-stu-id="15f27-133">…on its own</span></span>

<span data-ttu-id="15f27-134">Você pode encontrar nossas folhas de estilo padrão no `font/css/open-iconic.{css, less, scss, styl}`</span><span class="sxs-lookup"><span data-stu-id="15f27-134">You can find our default stylesheets in `font/css/open-iconic.{css, less, scss, styl}`</span></span>

```
<link href="/open-iconic/font/css/open-iconic.css" rel="stylesheet">
```

```
<span class="oi" data-glyph="icon-name" title="icon name" aria-hidden="true"></span>
```


## <a name="license"></a><span data-ttu-id="15f27-135">Licença</span><span class="sxs-lookup"><span data-stu-id="15f27-135">License</span></span>

### <a name="icons"></a><span data-ttu-id="15f27-136">Ícones</span><span class="sxs-lookup"><span data-stu-id="15f27-136">Icons</span></span>

<span data-ttu-id="15f27-137">Todo o código (incluindo a marcação SVG) está sob a [licença MIT](http://opensource.org/licenses/MIT).</span><span class="sxs-lookup"><span data-stu-id="15f27-137">All code (including SVG markup) is under the [MIT License](http://opensource.org/licenses/MIT).</span></span>

### <a name="fonts"></a><span data-ttu-id="15f27-138">Fontes</span><span class="sxs-lookup"><span data-stu-id="15f27-138">Fonts</span></span>

<span data-ttu-id="15f27-139">Todas as fontes estão sob o [Sil licenciado](http://scripts.sil.org/cms/scripts/page.php?item_id=OFL_web).</span><span class="sxs-lookup"><span data-stu-id="15f27-139">All fonts are under the [SIL Licensed](http://scripts.sil.org/cms/scripts/page.php?item_id=OFL_web).</span></span>
