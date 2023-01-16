<h1 align="center">Revisão simples de CSS basico<h1>


# CSS

- Cascading Style Sheet,CSS,é uma linguagem de estilo, responsavel pela parte estética de uma aplicação.

- Sua sintex é composta por um “Seletor” seguido de aspas” { }”,Dentro da aspa ficaram os estilos separados por “;”

       Seletor {

          Estilo:atributo;

       }

- Com CSS você pode criar desde estilos simples,efeitos e animações avançadas.

---

# Seletores

- O Seletores dizem qual elemento vai ser estilizado.
- Por tag: pode-se chamar diretamente uma tag do html.
- Por classe: tags html que tem classes podem ser chamadas assim → .classe
- Por ID: tags html que tem IDs podem ser chamadas assim → #classe
- Por atributo: pode chamar tags e entre [] colocar algum de seus atributos
- Existe outros seletores para filhos,adjacentes,irmãos entre outros.

---

# Comentários

- Uma coisa importantíssima para organização e facilitar a leitura do codigo são os comentários!!
- Para usar comentários no CSS basta usar a seguinte sintaxe

       /*  Seu Comentário! */

---

# Cores

- Agora vamos aprender as primeiras propriedades do CSS
- Para mudar cores de “Conteúdos”(oque fica entre tags no html) use → color:   ;
- Para mudar a cor de fundo de um elemento, use → background-color:  ;

---

# Tamanhos

- No css temos diversas formas de definir o tamanho de algo, iremos focar nas principais
- Para mudar a largura de um elemeto, use → width:  ;
- Para mudar a altura de uma elemento,use → height: ;
- Para mudar o tamanho de um caractere, use → font-size:  ;

---

# Margens

- No CSS os elementos possuem margens internas e externas
- Margem externa é a distância da “borda” do elemento em relação a outros elementos
- Margem interna é a distância da “borda” do elemento em relação ao seu conteúdo

---

# Borda

- No CSS elementos possuem borda que por padrão a grande maioria dos elementos vem como invisivel, porém ela está la!
- As bordas podem ter largura, cores e estilo
- A propriedade “ borde:  ; “ recebe pode receber 3 valores

      border: largura estilo cor;

- Alguns estilos q uma borda pode receber são:
- none: invisivel
- dotted: pontilhado
- solid: uma linha padrão
- double: linha dupla

---

# Display

- Um elemento pode ter duas propriedades de Tela, uma para si, e uma para seus filhos
- Principais propriedades para si:

       display: block;  /* O elemento quebra linha antes e depois de si */

       display: inline;  /* O elemento não quebra linhas, ele se posiciona onde ouver espaço */

       display: inline-block; /* O elemento não quebra linhas, ele se posiciona onde ouver espaço */

- A diferença entre “inline” e “inline-block” é bem simples, o “inline” ele mantem o conteudo como tamanho maximo da “caixa”, enquanto no inline-block, por mais q não quebre linhas, ele mantem propriedades de largura e altura como foram definidas.

### Flex box

       display: flex; /* Os filho podem ser manipulados com mais liberdade dentro do elemento *

- Com o display flex, novas propriedades podem ser aplicadas no componente, como:

       flex-direction: row; /* Padrão quando se usa display flex, os filhos  se organizam em linha *

       flex-direction: column; /* Os filhos se organizam em coluna */

- Tanto row como column podem inverter a ordem dos filhos usando column-reverse ou row-reverse

- No display flex existem as propriedades de alinhamento, as principais são:

       justify-content: start / center / end ; /* Alinha elementos na horizontal */

       align-items: start / center / end ; /* Alinha elementos na vertical */

       gap:  value;  /* Da uma margem entre os filhos */

- obs: caso seja o caso do “ flex-direction: column; ” o “justify-content” passa a alinhar na vertical e o “align-items” na horizontal

       

### Grid layout

       display: grid; /* Um sistema “malha” é definido para seus filhos */

- Com o display grid, novas propriedades podem ser aplicadas no componente, como:

       grid-template-columns: value; 

       grid-template-rows: value;

- Com o “template-columns” e “template-rows” você pode definir quantas colunas e linhas terão e o tamanho de cada uma

       grid-template-rows: 100px 100px 100px;

       grid-template-columns:  100px 100px 100px; 

- No grid também funciona o gap: value;

- Junto ao “grid-template-columns” você pode usar a seguinte propriedade

       grid-template-areas:  .  .  . 

                                          .  .  . ;

- No exemplo acima, está definido 3 colunas e 2 linhas onde os filhos irão se organizar

- Você também pode usar propriedades nos filho com o “grid-area: nome do filho;”
- Com isso você terá mais liberdade na malha como por exemplo:

       grid-template-areas:  filho1  filho2  filho2

                                          filho1  filho3  filho3 ;

# Posições

- No CSS existe a propriedade “position” ela pode ter os seguintes valores:

       position: static;  /* Padrão do css */

       position: relative; /* Matem o fluxo,mas podendo ser posicionado de outras formas*/

       position: absolute; /* é posicionado a partir do seu “ancestral posicionado mais proximo” */

- Para alinhar elementos “relative” e “absolute” são usado as propriedades:

       top:  ;

       bottom:  ;

       left:  ;

       right  ;

- Elementos posicionados podem usar a propriedade “z-index”, que nada mais é q um posicionamento de “profundidade”, quanto maior o valor mais pra frente, quanto menor mais pra trás.
