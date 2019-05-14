# Dicas para desenvolver para Smart TVs

[English](README.md)

## Fabricantes e Sistema Operacionais
* Samsung
    - Tizen
    - Orsay
* LG
    - webOS
    - Netcast
* Sony
    - Linux
    - Android
* Panasonic
    - Firefox OS
* Philips
* TCL
* Philco

## Visão Geral
* Como são vários sistemas operacionais e browsers diferentes, funcionar em um modelo de TV não garante que em outro modelo a sua aplicação funcionará.
* Algumas TVs possuem mouse no controle, como por exemplo a webOS. Então essa funcionalidade deve ser implementada caso queira que seu app seja aprovado na loja da mesma.

## DOM
* Evite o uso de `https`.
* O uso de `document.*`, `element.*`, `JSON.parse` e `XMLHttpRequest` é custoso para a TV processar.
* Atualizar o DOM enquanto existe uma animação em andamento, faz o framerate cair drasticamente. Faça sempre uma coisa de cada vez.
* Utilizar `.focus()` afeta a performance. Utilize classes no CSS para saber qual elemento está focado.

## Imagens
* Tente utilizar imagens no lugar de CSS para as propriedades: `border`, `background`, `box-shadow` e `gradient`, pois tudo que é gerado via CSS, precisa ser calculado, renderizado e depois, pintado.
* `opacity` e `transform` são propriedades que podem ser animadas (com moderação) pois performam bem nas TVs.

## CSS
* Evite o uso das propriedades `grid` e `flex` pois algumas TVs não a suportam totalmente.