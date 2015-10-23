#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Álvaro Gianni Pagliari
### Artigo de revisão de CSS3

<br/>
##### Funcionalidade:  calc()
##### O que é?
A função calc() permite que os desenvolvedores realizem cálculos para determinar valores nas propriedades do CSS. A função tem como parâmetro uma expressão que suporta números em formatos diversos (ex.: *%* com *em*) e as quatro operações básica da matemática (+, -, * e /). Também é permitido o uso de parênteses para estabelecer a ordem do cálculo.

##### Onde usar
A função pode ser utilizada em qualquer lugar que aceite os tipos *length*, *frequency*, *angle*, *time*, *number* e *integer*.

##### Como usar
```css
seletor {
    propriedade: calc(expressão);
}
```

#####Exemplo de uso
```css
body {
 margin: 0;
 padding: 0;
}

div {
 width: 90%;                /* para navegadores que não suportam calc() */
 width: calc(100% - 100px); /* para suporte nativo */
 margin: 0 auto;
 height: 200px;
 border: 1px solid black ;
 background: lime;
}
```
##### Referência
[https://developer.mozilla.org/en-US/docs/Web/CSS/calc](https://developer.mozilla.org/en-US/docs/Web/CSS/calc)<br/>
[http://www.maujor.com/tutorial/css3-funcao-css-calc.php](http://www.maujor.com/tutorial/css3-funcao-css-calc.php)

<br/>

##### Funcionalidade:  Seletores Avançados - :not 
##### O que é?
O CSS3 definiu vários novos seletores para uso avançado, apresentamos aqui um deles. O seletor :not é definido como uma pseudo-classe de negação no formato *:not(X)* onde *X* é um seletor simples (exceto a própria pseudo-classe de negação). Ele é utilizado para selecionar um conjunto de classes e excluir outra, ou seja, utilizando a sintaxe da seção **Como Usar** abaixo o resultado da seleção seriam todas os elementos que contem *seletorA* exceto os que contenham o *seletorB*.

##### Onde usar
Utilizado para facilitar a aplicação de estilos através da exclusão seletiva de algumas classes.

##### Como usar
```css
seletorA:not(seletorB){
    ...propriedades...
}
```
#####Exemplo de uso
```css
div:not(.footer) {
     font-weight: bold;
}
```
##### Referência
[http://www.w3.org/TR/css3-selectors/](http://www.w3.org/TR/css3-selectors/)<br/>
[https://developer.mozilla.org/pt-BR/docs/Web/CSS/%3Anot](https://developer.mozilla.org/pt-BR/docs/Web/CSS/%3Anot)<br/>
[http://codigofonte.uol.com.br/artigos/10-seletores-de-css-que-voce-deveria-usar](http://codigofonte.uol.com.br/artigos/10-seletores-de-css-que-voce-deveria-usar)<br/>

<br/>

##### Funcionalidade:  Transições CSS
##### O que é?
No CSS as transições são utilizadas como uma forma de mudar propriedades do CSS, porém ao invés da mudança ser instantânea é possível fazer com que ela dure por um período de tempo (utilizando uma curva de aceleração). É possível controlar quais itens serão animados (*transition-property*), quando uma trasição vai ocorrer (*transition-delay*), por quanto tempo ela ocorrerá (*transition-duration*) e como ela ocorrerá (*transition-timing-function*, curva de aceleração). As transições são definidas por várias propriedades CSS conforme explicitado na seção **Como Usar**.

##### Onde usar
Nem todas as propriedades CSS podem ser animadas, existe uma [lista](http://www.w3.org/TR/css3-transitions/#animatable-css) definida pela W3C de quais propriedades são animáveis. As funções de curva de aceleração também são uma lista pré-definida pela W3C.

##### Como usar
```css
seletor {
    transition-property: <um dos itens animáveis pelo CSS>;
    transition-duration: <tempo>;
    transition-delay: <tempo>;
    transition-timing-function: <função de cálculo do tempo>
}
```
#####Exemplo de uso
```css
.menuButton {
  position: relative;
  transition-property: background-color, color;
  transition-duration: 1s;
  transition-timing-function: ease-out;
  text-align: left;
  background-color: grey;
  left: 5px;
  top: 5px;
  height: 26px;
  color: white;
  border-color: black;
  font-family: sans-serif;
  font-size: 20px;
  text-decoration: none;
  box-shadow: 2px 2px 1px black;
  padding: 2px 4px;
  border: solid 1px black;
}

.menuButton:hover {
  position: relative;
  transition-property: background-color, color;
  transition-duration: 1s;
  transition-timing-function: ease-out;
  background-color:white;
  color:black;
  box-shadow: 2px 2px 1px black;
}
```
##### Referência
[http://www.w3.org/TR/css3-transitions/](http://www.w3.org/TR/css3-transitions/)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)<br/>
[http://tableless.com.br/transition-e-animation/](http://tableless.com.br/transition-e-animation/)

<br/>

##### Funcionalidade:  Gradientes - linear-gradient()
##### O que é?
Essa função CSS é utilizada para criar uma imagem que representa o gradiente linear definido pelas cores informadas na função. O resultado desta função é um objeto CSS do tipo *gradient*. Para utilizar esta função é necessário informar o ponto inicial e um ângulo de inclinação, bem como as cores inicial e final e as possíveis cores intermediárias.

##### Onde usar
Geralmente esta função é utilizada para definir o background do site, permitindo que não sejam utilizadas imagens pré-definidas para tal (o que deixa o site maior e mais difícil de se adaptar a diversos tamanhos).

##### Como usar
A sintaxe desta função mudou diversas vezes, por isso segue as possíveis formas de utilização.

```css
-webkit-gradient(<type>, <point> [, <radius>]?, <point> [, <radius>]? [, <stop>]*)

-moz-linear-gradient([ [ [top | bottom] || [left | right] ],]? <color-stop>[, <color-stop>]+);

linear-gradient( [ [ <angle> | [top | bottom] || [left | right] ],]? <color-stop>[, <color-stop>]+);

/*Sintaxe final da função*/
linear-gradient([ [ [ <angle> | to [top | bottom] || [left | right] ],]? <color-stop>[, <color-stop>]+);
```

#####Exemplo de uso
```css
div {
  background: linear-gradient(to right, red, orange, yellow, green, blue, indigo, violet);
}

#grad {
  background: -webkit-linear-gradient(left,rgba(255,0,0,0),rgba(255,0,0,1)); /*Safari 5.1-6*/
  background: -o-linear-gradient(right,rgba(255,0,0,0),rgba(255,0,0,1)); /*Opera 11.1-12*/
  background: -moz-linear-gradient(right,rgba(255,0,0,0),rgba(255,0,0,1)); /*Fx 3.6-15*/
  background: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1)); /*Standard*/
}
```
##### Referência
[http://www.w3schools.com/css/css3_gradients.asp](http://www.w3schools.com/css/css3_gradients.asp)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient](https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient)<br/>
[https://developer.mozilla.org/pt-BR/docs/Web/CSS/Using_CSS_gradients](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Using_CSS_gradients)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)<br/>

<br/>

##### Funcionalidade:  Layout Multi-Coluna
##### O que é?
O layout multi-coluna é uma adição ao CSS3 que permite extender o modo do layout de bloco para facilmente definir múltiplas colunas de texto. Duas propriedades de controle são as mais utilizadas, a *column-count* e a *column-width*. Outras propriedades também são definidas para melhor controlar a quebra das colunas, são elas: *column-gap*, *column-rule-style*, *column-rule-width*, *column-rule-color*, *column-rule* e *column-span*. Sem estas propriedades é extremamente difícil fazer um layout de coluna sem que o mesmo fique complexo ou restrito ao tamanho utilizado. 

##### Onde usar
Utilizar nas tags HTML que estejam sendo usadas para controlar o texto que se quer quebrar em mais de uma coluna.

##### Como usar
```css
seletor {
    column-count: <valor>;
    column-count: <valor>;
    column-fill: <valor>;
    column-gap: <valor>;
    column-rule: <valor>;
    column-rule-color: <valor>;
    column-rule-style: <valor>;
    column-rule-width: <valor>;
    column-span: <valor>;
    column-width: <valor>;
 }
```
#####Exemplo de uso
```css
.columns3 {
    -webkit-column-count: 3; /* Chrome, Safari, Opera */
    -moz-column-count: 3; /* Firefox */
    column-count: 3;
    -webkit-column-gap: 50px; /* Chrome, Safari, Opera */
    -moz-column-gap: 50px; /* Firefox */
    column-gap: 50px;
    -webkit-column-rule: 15px outset #00ffff; /* Chrome, Safari, Opera */
    -moz-column-rule: 15px outset #00ffff; /* Firefox */
    column-rule: 15px outset #00ffff;
}

```
##### Referência
[http://www.w3schools.com/css/css3_multiple_columns.asp](http://www.w3schools.com/css/css3_multiple_columns.asp)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Columns/Using_multi-column_layouts](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Columns/Using_multi-column_layouts)<br/>
[https://css-tricks.com/snippets/css/multiple-columns/](https://css-tricks.com/snippets/css/multiple-columns/)<br/>
[http://www.htmlgoodies.com/primers/html/CSS3_Multi_column_Layouts.html#fbid=0zyW6ZBa15B](http://www.htmlgoodies.com/primers/html/CSS3_Multi_column_Layouts.html#fbid=0zyW6ZBa15B)

<br/>

##### Funcionalidade:  Webfonts
##### O que é?
As WebFonts permitem que os designers utilizem fontes em suas páginas web que não estejam instaladas no computador do usuário. É recomendado o uso desta tecnologia quando o designer quer manter o estilo da fonte e não utilizar uma imagem no lugar do texto, melhorando a busca no site e a acessibilidade. A regra utilizada pelo CSS para permitir o uso de WebFonts é @font-face, sendo vários formatos de fonte possíveis (de acordo com o browser utilizado), como: arquivos TTF/OTF, WOFF, WOFF2, SVG e EOT.

##### Onde usar
Pode ser utilizada em qualquer elemento que aceite definições de padrão de texto.

##### Como usar
```css
@font-face {
  [ font-family: <family-name>; ] ||
  [ src: [ <uri> [format(<string>#)]? | <font-face-name> ]#; ] ||
  [ unicode-range: <urange>#; ] ||
  [ font-variant: <font-variant>; ] ||
  [ font-feature-settings: normal | <feature-tag-value>#; ] ||
  [ font-stretch: <font-stretch>; ] ||
  [ font-weight: <weight>; ] ||
  [ font-style: <style>; ]
}
```

De uma forma simplificada
```css
@font-face {
    font-family: nome_da_familia;
    src: url(local da fonte);
}

seletor {
    font-family: nome_da_familia;
}
```
#####Exemplo de uso
```css
@font-face {
  font-family: 'Tagesschrift';
  src: url('tagesschrift.ttf');
}

h1, h2, h3 { font-family: 'Tagesschrift', 'Georgia', serif; }

```
##### Referência
[http://www.w3schools.com/css/css3_fonts.asp](http://www.w3schools.com/css/css3_fonts.asp)<br/>
[http://www.html5rocks.com/en/tutorials/webfonts/quick/?redirect_from_locale=pt](http://www.html5rocks.com/en/tutorials/webfonts/quick/?redirect_from_locale=pt)<br/>
[https://developer.mozilla.org/pt-BR/docs/Web/CSS/@font-face](https://developer.mozilla.org/pt-BR/docs/Web/CSS/@font-face)


<br/>

##### Funcionalidade:  Media Queries
##### O que é?
Media queries são funções que permitem ao CSS3 através de *media types* aplicar estilos de forma condicional. Ou seja, somente se as expressões definidas como *media features* forem verdadeiras as regras definidas dentro de uma Media Querie será aplicada. Desta forma é possível tornar o CSS mais adaptável a diferentes formatos de tela e resoluções.

##### Onde usar
Utilizar na definição das regras CSS do site sendo desenvolvido, para escolher quais estilos aplicar de acordo com características do dispositivo que o usuário está utilizando para acessar o site.

##### Como usar
A Media Queries possuem uma BNF definindo sua utilização, conforme segue:

```css
media_query_list: <media_query> [, <media_query> ]*
media_query: [[only | not]? <media_type> [ and <expression> ]*]
  | <expression> [ and <expression> ]*
expression: ( <media_feature> [: <value>]? )
media_type: all | aural | braille | handheld | print |
  projection | screen | tty | tv | embossed
media_feature: width | min-width | max-width
  | height | min-height | max-height
  | device-width | min-device-width | max-device-width
  | device-height | min-device-height | max-device-height
  | aspect-ratio | min-aspect-ratio | max-aspect-ratio
  | device-aspect-ratio | min-device-aspect-ratio | max-device-aspect-ratio
  | color | min-color | max-color
  | color-index | min-color-index | max-color-index
  | monochrome | min-monochrome | max-monochrome
  | resolution | min-resolution | max-resolution
  | scan | grid
```

De uma forma mais simplificada
```css
@media not|only mediatype and (media feature) {
    CSS-Code;
}
```

#####Exemplo de uso
```css
/*Muda a cor do fundo se a largura da tela for maior que 480 pixels*/
@media screen and (min-width: 480px) {
    body {
        background-color: lightgreen;
    }
}
```
##### Referência
[https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)<br/>
[http://www.w3schools.com/cssref/css3_pr_mediaquery.asp](http://www.w3schools.com/cssref/css3_pr_mediaquery.asp)<br/>
[http://tableless.com.br/introducao-sobre-media-queries/](http://tableless.com.br/introducao-sobre-media-queries/)


<br/>

##### Funcionalidade:  Backgrounds Múltiplos
##### O que é?
Permite que o desenvolvedor defina várias imagens de background que serão compostas em uma única imagem pelo browser. A primeira imagem definida será a imagem do topo e a última imagem será a do fundo. Apenas a última imagem pode definir uma cor de fundo. Pode ser utilizada a propriedade atalho *background* ou então as propriedades *background-attachment*, *background-clip*, *background-image*, *background-origin*, *background-position*, *background-repeat* e *background-size*.

##### Onde usar
Utilizada em qualquer componente que possua a propriedade background.

##### Como usar
```css
[ <bg-layer> , ]* <final-bg-layer>
where 
<bg-layer> = <bg-image> || <position> [ / <bg-size> ]? || <repeat-style> || <attachment> || <box>{1,2}
<final-bg-layer> = <bg-image> || <position> [ / <bg-size> ]? || <repeat-style> || <attachment> || <box> || <box> || <'background-color'>
where 
<bg-image> = none | <image>
<bg-size> = [ <length> | <percentage> | auto ]{1,2} | cover | contain
<repeat-style> = repeat-x | repeat-y | [repeat | space | round | no-repeat]{1,2}
<attachment> = scroll | fixed | local
<box> = border-box | padding-box | content-box
```

De uma forma simplificada
```css
seletor {
    background-image: url(imagem1), url(imagem2), url(imagem3);
    background-position: valor;
    background-repeat: valor;
}
```
#####Exemplo de uso
```css
div {
width:600px;
height:500px;
border:1px solid black;
background:
url(gradiente-top.png) top left repeat-X,
url(gradiente-baixo.png) bottom left repeat-X,
url(gradiente-esquerda.png) top left repeat-Y,
url(gradiente-direita.png) top right repeat-Y;
}
```
##### Referência
[http://tableless.com.br/multiplos-backgrounds-com-css/](http://tableless.com.br/multiplos-backgrounds-com-css/)<br/>
[http://www.css3.info/preview/multiple-backgrounds/](http://www.css3.info/preview/multiple-backgrounds/)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Background_and_Borders/Using_CSS_multiple_backgrounds](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Background_and_Borders/Using_CSS_multiple_backgrounds)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/background](https://developer.mozilla.org/en-US/docs/Web/CSS/background)

<br/>

##### Funcionalidade:  Text Shadow
##### O que é?
A propriedade text-shadow permite adicionar sombra a um texto de um elemento. Cada sombra é especificada através de uma distância do texto, bem como uma cor opcional e o valor de raio do blur. Também é possível informar várias sombras que serão ordenadas da frente para o fundo.

##### Onde usar
É possível utilizar esta função em qualquer elemento que tenha texto.

##### Como usar
```css
seletor {
    text-shadow: h-shadow v-shadow blur-radius color|none|initial|inherit;
}
```

#####Exemplo de uso
```css
/*Apresenta uma sombra vermelha com um brilho estilo neon verde*/
h1 {
    text-shadow: 0 0 3px #FF0000, 0 0 5px #00FF00;
}
```
##### Referência
[http://www.w3schools.com/cssref/css3_pr_text-shadow.asp](http://www.w3schools.com/cssref/css3_pr_text-shadow.asp)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow)

<br/>

##### Funcionalidade:  Animações CSS
##### O que é?
As animações em CSS permitem animar a maioria dos elementos HTML sem a utilização de Javascript ou Flash. As animações, se bem utilizadas, permitem tornar a experiência de usuário de um site melhor, permitindo chamar a atenção do usuário para determinadas áreas importantes ou simplesmente adicionar interesse a interface.

Para realizar as animações é necessário primeiro definir os *Keyframes* que definem os estágios e estilos da animação. Em um segundo momento estes *Keyframes* são atribuídos a propriedades de animação definidos em elementos CSS.

Cada *Keyframe* é composto de um nome, estágios de animação (valores percentuais de 0% a 100%) e propriedades CSS. No segundo estágio é atribuído o nome da animação a propriedade *animation-name* de algum elemento HTML animável. Outras funções que podem ser utilizadas para controlar as animações são: *animation-duration*, *animation-timing-function*, *animation-delay*, *animation-direction*, *animation-iteration-count*, *animation-fill-mode* e *animation-play-state*.

##### Onde usar
As Animações CSS podem ser utilizadas de acordo com uma lista definida e publicada pela W3C conforme listado em [propriedades animáveis](http://www.w3.org/TR/css3-transitions/#animatable-properties).

##### Como usar
A sintaxe formal definida para as animações é:
```css
<single-animation-name> || <time> || <timing-function> || <time> || <single-animation-iteration-count> || <single-animation-direction> || <single-animation-fill-mode> || <single-animation-play-state>
where 
<single-animation-name> = none | IDENT
<single-animation-iteration-count> = infinite | <number>
<single-animation-direction> = normal | reverse | alternate | alternate-reverse
<single-animation-fill-mode> = none | forwards | backwards | both
<single-animation-play-state> = running | paused
```

De uma forma simplificada
```css
@keyframes nome_keyframe {
    from{propriedades css}
    to {propriedades css}
}

/* OU */

@keyframes nome_keyframe {
    0% {propriedades css}
    50% {propriedades css}
    100% {propriedades css}
}

/* ENTÃO */

seletor {
    animation-name: nome_keyframe;
    animation-duration: tempo;
}
```
#####Exemplo de uso
```css
/* The animation code */
@keyframes example {
    0%   {background-color: red; left:0px; top:0px;}
    25%  {background-color: yellow; left:200px; top:0px;}
    50%  {background-color: blue; left:200px; top:200px;}
    75%  {background-color: green; left:0px; top:200px;}
    100% {background-color: red; left:0px; top:0px;}
}

/* The element to apply the animation to */
div {
    width: 100px;
    height: 100px;
    position: relative;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
    animation-iteration-count: 3;
    animation-direction: alternate;
}
```
##### Referência
[http://www.w3schools.com/css/css3_animations.asp](http://www.w3schools.com/css/css3_animations.asp)<br/>
[https://robots.thoughtbot.com/css-animation-for-beginners](https://robots.thoughtbot.com/css-animation-for-beginners)<br/>
[https://developer.mozilla.org/en-US/docs/Web/CSS/animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)<br/>
[http://www.w3.org/TR/css3-transitions](http://www.w3.org/TR/css3-transitions)
