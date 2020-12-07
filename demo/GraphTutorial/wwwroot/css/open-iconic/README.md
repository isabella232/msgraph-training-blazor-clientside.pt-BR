---
ms.openlocfilehash: 3965884c8e0d7116f5d8a42e6aefb0dc5be94f1e
ms.sourcegitcommit: 5067c508675fbedbc7eead0869308d00b63be8e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49584509"
---
<a name="open-iconic-v111"></a>[Abrir o icônico v 1.1.1](http://useiconic.com/open)
===========

### <a name="open-iconic-is-the-open-source-sibling-of-iconic-it-is-a-hyper-legible-collection-of-223-icons-with-a-tiny-footprintmdashready-to-use-with-bootstrap-and-foundation-view-the-collection"></a>Abra icônico é o irmão de fonte aberta de [icônico](http://useiconic.com). É uma coleção do Hyper-legíveis de ícones 223 com uma pequena ocupação &mdash; pronta para uso com inicialização e Fundação. [Exibir a coleção](http://useiconic.com/open#icons)



## <a name="whats-in-open-iconic"></a>O que há no Open icônico?

* 223 ícones projetados para serem legíveis a 8 pixels
* Arquivos SVG super claros-61,8 para o conjunto inteiro 
* SVG Sprite &mdash; a substituição moderna para fontes de ícone
* Formatos webfont (EOT, OTF, SVG, TTF, WOFF), PNG e WebP
* Folhas de estilo do webfont (incluindo versões de inicialização e Fundação) em formatos CSS, menos, SCSS e Stylus
* Imagens do PNG e do WebP rasterizadas no 8px, 16px, medianiz 24px, medianiz 32px, 48px e 64px.


## <a name="getting-started"></a>Introdução

#### <a name="for-code-samples-and-everything-else-you-need-to-get-started-with-open-iconic-check-out-our-icons-and-reference-sections"></a>Para obter exemplos de código e tudo o que você precisa para começar a usar o icônico aberto, Confira nossos [ícones](http://useiconic.com/open#icons) e seções de [referência](http://useiconic.com/open#reference) .

### <a name="general-usage"></a>Uso geral

#### <a name="using-open-iconics-svgs"></a>Usando o SVGs do icônico

Gostaríamos de SVGs e achamos que eles são a maneira de exibir ícones na Web. Como as icônico abertas são apenas SVGs básicas, sugerimos que você as exiba como faria com qualquer outra imagem (não esqueça o `alt` atributo).

```
<img src="/open-iconic/svg/icon-name.svg" alt="icon name">
```

#### <a name="using-open-iconics-svg-sprite"></a>Usando o icônico de SVG do Open

Abrir o icônico também vem em uma entidade de grupo SVG que permite que você exiba todos os ícones no conjunto com uma única solicitação. É como uma fonte de ícone, sem ser um ataque.

A adição de um ícone de uma entidade de conteúdo SVG é um pouco diferente do que você está acostumado, mas ainda é uma parte do bolo. *Dica: para tornar os seus ícones facilmente estilos, sugerimos adicionar uma classe geral à* `<svg>` *marca e um nome de classe exclusivo para cada ícone diferente na* `<use>` *marca.*  

```
<svg class="icon">
  <use xlink:href="open-iconic.svg#account-login" class="icon-account-login"></use>
</svg>
```

Ícones de dimensionamento só precisam de CSS básicos. Todos os ícones estão em um formato quadrado, portanto, basta definir a `<svg>` marca com dimensões de largura e altura iguais.

```
.icon {
  width: 16px;
  height: 16px;
}
```

Ícones de coloração é ainda mais fácil. Tudo o que você precisa fazer é definir a `fill` regra na `<use>` marca.

```
.icon-account-login {
  fill: #f00;
}
```

Para saber mais sobre os sprites SVG, leia o [guia da Carla Coyier](http://css-tricks.com/svg-sprites-use-better-icon-fonts/).

#### <a name="using-open-iconics-icon-font"></a>Usando a fonte do ícone do Open icônico...


##### <a name="with-bootstrap"></a>... com inicialização

Você pode encontrar nossas folhas de estilo de Bootstrap no `font/css/open-iconic-bootstrap.{css, less, scss, styl}`


```
<link href="/open-iconic/font/css/open-iconic-bootstrap.css" rel="stylesheet">
```


```
<span class="oi oi-icon-name" title="icon name" aria-hidden="true"></span>
```

##### <a name="with-foundation"></a>... com base

Você pode encontrar as folhas de estilo de base no `font/css/open-iconic-foundation.{css, less, scss, styl}`

```
<link href="/open-iconic/font/css/open-iconic-foundation.css" rel="stylesheet">
```


```
<span class="fi-icon-name" title="icon name" aria-hidden="true"></span>
```

##### <a name="on-its-own"></a>... por conta própria

Você pode encontrar nossas folhas de estilo padrão no `font/css/open-iconic.{css, less, scss, styl}`

```
<link href="/open-iconic/font/css/open-iconic.css" rel="stylesheet">
```

```
<span class="oi" data-glyph="icon-name" title="icon name" aria-hidden="true"></span>
```


## <a name="license"></a>Licença

### <a name="icons"></a>Ícones

Todo o código (incluindo a marcação SVG) está sob a [licença MIT](http://opensource.org/licenses/MIT).

### <a name="fonts"></a>Fontes

Todas as fontes estão sob o [Sil licenciado](http://scripts.sil.org/cms/scripts/page.php?item_id=OFL_web).
