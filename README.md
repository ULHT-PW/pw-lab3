**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**
 
# Programação Web - Laboratório 3: <br>*inclusão de formulários e imagens SVG no meu website* 

## Objetivo
* Neste laboratório estenderá o website criado no Laboratório 2, incluindo formulários e imagens SVG.
* Este laboratório deverá ser concluido antes da sua aula prática da semana de 8 de março. Este será avaliado nessa aula. 

* Este laboratório deverá ser concluido antes da sua aula prática da semana de 14.3, onde será avaliado. 

## Recomendações
* Leia o enunciado todo com atenção antes de o começar a resolver para entender o que fará.
* Execute com atenção cada passo, certificando-se que implementa todos os detalhes. Contém todos os detalhes para a criação do website. 
* Se tiver alguma dúvida, recorra aos slides da aula que contêm todos os conhecimentos que precisa para realizar o laboratório.

## Pré-requisitos
* Deverá ter o Pycharm instalado para editar o código HTML de forma fácil.
* Deverá ter feito os [lab1](https://github.com/ULHT-PW/pw-lab1) e [lab2](https://github.com/ULHT-PW/pw-lab2). Caso não tenha feito, faça antes de fazer este laboratório.
* Deverá ter instalado o git no seu computador.

# 1. Estruturação do repositório de laboratórios
1. Clone  (descarregue uma cópia) o seu repositório no seu computador local da seguinte forma:
    1. abra um processador de comandos (Tecla Windows e escreva `cmd`, ou `Powershell`, ou `git bash`)
    2. escolha a pasta onde quer colocar o repositório (navegando com o comando `cd nome-de-pasta` para entrar numa determinada pasta)
    3. escreva o comando `git clone https://github/seuusername/pw-labs-nomeapelido-numero` (hiperlink do seu repositório, com o seu username do GitHub e nome do repositório).

2. Crie a pasta `lab3`. 

3. Atualize o `index.html` do seu website, incluindo agora um link para o Laboratório 3.

3. Copie os conteúdos do `lab2` para a pasta `lab3`, que servirão de base para este laboratório.
4. Neste laboratório irá criar mais duas páginas. Atualize o menu de todas as páginas HTML existentes com dois novos links: Quizz (na página `quizz.html`) e Comentários (na página `comentarios.html`). Coloque-os antes da página Home.


# 2. Página com Quizz

1. Crie uma nova página HTML `quizz.html` que tenha o mesmo cabeçalho das restantes.
2. Insira um elemento h3 com a palavra Quizz.
3. Esta página irá ter um formulário com um quizz sobre a cidade. Deverá fazer perguntas de vários tipos sobre a cidade, o formulário sendo enviado para um endereço de email (quando desenvolvermos o back-end, poderá processar os dados enviados e apresentar ao utilizador uma resposta). 
4. Deverá ter uma primeira área (elemento `fieldset`) para inserção de dados pessoais:
   * Nome
   * apelido
   * email

5. Noutro(s) elemento(s) `fieldset` crie um quiz sobre a cidade, explorando de forma imaginativa os elementos `input`, `select`, `textarea`, `datalist`, `label`, `fieldset`, `output`. * Deverá usar todos os seguintes tipos de input (atributos `type`):
   * `text`
   * `radio`
   * `checkbox`
   * `date`
   * `image`
   * `color`
   * `number`
   * `range`

6. Na totalidade dos elementos que utilizar deverá garantir que utiliza pelo menos uma vez cada um dos seguintes atributos de input:
   * `value`
   * `placeholder`
   * `autocomplete`
   * `size`
   * `maxlength`
   * `form`
   * `multiple`
   * `autofocus`
   * `required`
   * `step`
   * `output`

5. Inclua um elemento do tipo `submit` para submeter o seu formulário:
   * No atributo `method`especifique o método `post`
   * o atributo `action` deverá ter como valor um endero de email. Assim, receberá o quizz no seu email.
   * Quando desenvolvermos o back-end, poderá processar os dados enviados e apresentar ao utilizador uma resposta.

# 3. Página Comentários

1. Crie uma nova página HTML `comentarios.html` que tenha o mesmo cabeçalho das restantes.
2. Insira um elemento h3 com a palavra Comentários.
3. Esta página servirá para recolher opiniões sobre o seu website assim como ideias de coisas a melhorar.
4. Crie um formulário para recolher opiniões sobre o seu website, avaliando 10 critérios. Listam-se em baixo alguns padrões intelectuais do pensamento crítico: 
    * clareza (compreensível, em que o significado pode ser identificado sem que haja confusão ou ambiguidade.)
    * rigor (livre de erros)
    * precisão (exato, segundo o nível necessário do pormenor)
    * profundidade (contém complexidades e múltiplas inter-relações)
    * amplitude (que abrange diferentes aspectos, pontos de vista, pespectivas)
    * lógica (em que as partes fazem sentido num todo, sem contradições: faz sentido no conjunto, provém de evidências)
    * significância (focado no importante, não trivial)
    * originalidade (criativo e original)
    Para tal, utilize elementos `input` com atributos `range`, `checkbox` e `radio`. Deverá igualmente ter um elemento `textarea` que permita submeter sugestões de melhoria.
6. Inclua um elemento escondido que identifica que se trata da opinião relativa ao website do laboratório 3. De facto, os laboratórios seguintes trarão várias melhorias ao seu website que resultarãm em comentários ainda melhores. 
7. Quando desenvolver o *back-end*, será capaz de processar estes dados introduzidos por
utilizadores e será capaz de fazer uma análise do seu website assim como uma visão crítica deste. 

# 4. Desenhos SVG

1. Altere a wordcloud que criou por forma a que seja um SVG embutido no HTML com a wordcloud:
   * inclua a wordcloud que criou no Laboratório 2 (com o elemento `image`). 
   * Sobreponha na imagem da wordcloud elementos transparentes sobre agumas palavras, com hiperlinks para páginas do seu website (abra a imagem no Paint para extrair as coordenadas dos vértices dos poçígonos sobre cada palavra). 
   * Deverá usar uma área default que cubra todo a imagem (restantes palavras para as quais não inseriu links específicos), e que remete para a introdução do seu website. Garanta que esta se encontra "por baixo" dos restantes elementos.

2. Crie um menu usando um SVG embutido no HTML ao estilo de uma wordcloud:
   * aplique efeitos a cada uma das palavras rodadas ou encurvadas, diferentes tamanhos, formas, cores, etc.
   * cada palavra deverá conter um elemento `animate` que deverá especificar como muda no tempo um determinado atributo. Explore o atributo `begin` também.
   * cada palavra deverá ter um hiperlink para a respetiva página.
   * coloque esta imagem no final de cada página do seu website.

3. Inspirado nalgum aspecto da cidade que escolheu, faça um desenho criativo embutido no HTML utilizando a maior diversidade de formas que consiga e utilizando os elementos animate, animateMotion e animateTransform. Coloque-o na secção Multimedia, especificando numa legenda os aspectos que o inspiraram para tal.

4. Inspirado nalgum aspecto da cidade que escolheu, utilize um editor SVG (por exemplo (Boxy-svg)[https://boxy-svg.com/app]) para criar um ficheiro SVG, explorando as ferramentas disponíveis. Coloque-o na secção Multimedia, especificando numa legenda os aspectos que o inspiraram para tal.

5. Na página `local.html` insira um SVG com o mapa SVG da localidade escolhida:
    * procure um mapa SVG da sua cidade (aqui)[https://commons.wikimedia.org/wiki/Category:SVG_maps_of_freguesias_in_Portugal] ou na Wikimedia Commons (se a cidade não for em Portugal).
    * insira no mapa pontos de interesse, objetos com hiperlinks que abram imagens sobre essa zona. 
    * Veja o [slide](https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/800079/course/section/398731/pw-02.1-html.pdf?time=1614518293580) 50 da aula sobre [html](https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/800079/course/section/398731/pw-02.1-html.pdf?time=1614518293580) que explia como fazer isso.
    * deverá criar um objeto iframe por baixo do mapa com um nome (`name`)
    * espicifique como target de cada hiperlink do mapa o nome da iframe, de forma a que a imagem abra dentro da iframe.

# 5. Multimedia

Na página de multimedia altere também a forma como abrem as fotografias grandes.
1. Veja o [slide](https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/800079/course/section/398731/pw-02.1-html.pdf?time=1614518293580) 50 da aula sobre [html](https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/800079/course/section/398731/pw-02.1-html.pdf?time=1614518293580).
2. insira um elemento iframe com a dimensão das fotografias (largura  800 pixels). Atribua um nome à iframe.
3. no target do hiperlink de cada imagem pequena especifique o nome da iframe.
4. quando clicar numa imagem pequena, a foto grande abrirá dentro da iframe. 

# 6. Referências

Quanto maior for o número de referências no seu website para outros websites, maior a relevância que o website ganhará assim como a visibilidade nos motores de busca. Coloque uma referência no final de um parágrafo de texto que tenha extraído de uma fonte online, assim como na legenda de uma fotografia. Pode usar a notação `[1]` colocando um hiperlink para a página de onde foi extraída informação. 

# 7. Submissão

1. Verifique que todos os links do seu website funcionam devidamente.
2. Carregue a sua pasta no seu repositório Github através dos seguintes passos:
    1.  abra o processador de comandos e posicione-se dentro da pasta do seu repositório (`pw-labs-nomeapelido-numero`).
    2.  escreva as seguintes instruções:
        * `git add *`
        * `git commit –m "submissão laboratório 3"`
        * `git push`
3. Sincronize o GitHub com o Heroku tal como fez no [lab1](https://github.com/ULHT-PW-2020-21/pw-lab1). Deverá ir ao Heroku e, em Deploy, fazer deploy branch, de forma a colocar disponível na cloud os novos conteúdos criados. 
4. Verifique que o seu website online fucnioa corretamente, mostra todas as imagens e os hiperlinks funcionam devidamente.
5. No seguinte [ficheiro](https://drive.google.com/file/d/1kphRYAo78NSxWznBXHqNbPksELqlyloI/view) garanta que esteja:
    * link da sua aplicação Heroku
    * link do seu repositório privado no GitHub
    * adicione os docentes de PW como membros do seu repositório, que têm como usernames no GitHub: luciostuder, logdarkmatter, rfgsantos.

Esperamos que tenha gostado de aplicar os conhecimentos de HTML e de ter feito um website &#127760;!


**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**
 
# Programação Web - Laboratório 4: Integração de elementos semânticos HTML5 no meu website e estilização com seletores e propriedades CSS 

## Objetivo
* O objetivo deste laboratório é experimentar os elementos HTML5 assim como seletores e propriedades CSS com base nos conteúdos do laboratório 3.

## Pré-requisitos
* Deverá ter feito o [lab3](https://github.com/ULHT-PW-2020-21/pw-lab3).
* 🔴 Antes de fazer este lab deverá ver o video sobre [propriedades CSS](https://educast.fccn.pt/vod/clips/2ea2z4vajw/html5.html?locale=en); consulte os respetivos [slides](https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/800079/course/section/398731/pw-02.6-propriedades-css.pdf). É material extra à aula teórica desta semana que precisam de saber para realizar este laboratório 🔴.


## Recomendações
* Leia primeiro o enunciado todo antes de o começar a resolver, para entender o que fará.
* Execute com atenção cada passo, certificando-se que implementa todos os detalhes. Contém todos os detalhes para a criação do website. 
* Se tiver alguma dúvida, consulte os slides sobre [HTML5 e seus elementos semanticos](https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/800079/course/section/398731/pw-02.4-html5-e-elementos-semanticos.pdf) e [CSS e seus seletores](https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/800079/course/section/398731/pw-02.5-css-e-seus-seletores.pdf) para ver como integrar os vários aspectos técnicos que são pedidos. Tem também disponivel o [video da aula](https://educast.fccn.pt/vod/clips/2qr2g6hysf/html5.html?locale=en) com capítulos sobre cada tópico. Estes contêm todos os conhecimentos que precisa para realizar este laboratório.
* Este laboratório deverá ser concluido antes da sua aula prática da semana de 15 de março. Este será avaliado nessa aula. 
 

# 1. Estruturação do repositório de laboratórios
1. Clone  (descarregue uma cópia) o seu repositório no seu computador local da seguinte forma:
    1. abra um processador de comandos (Tecla Windows e escreva `cmd`, ou `Powershell`, ou `git bash`)
    2. escolha a pasta onde quer colocar o repositório (navegando com o comando `cd nome-de-pasta` para entrar numa determinada pasta)
    3. escreva o comando `git clone https://github/seuusername/pw-labs-nomeapelido-numero` (hiperlink do seu repositório, com o seu username do GitHub e nome do repositório).

2. Crie a pasta `lab4`. 

3. Atualize o `index.html` da sua aplicação, incluindo na lista o nome deste laboratório com um link para lab4/index.html.

3. Copie os conteúdos do `lab3` para a pasta `lab4`, que servirão de base para este laboratório.

5. Neste laboratório irá criar mais umas página. Atualize o menu de todas as páginas HTML existentes com um novo link: html5-css.html.


# 2. Nova estrutura das páginas

1. Todas as suas páginas HTML deverão ser reestruturadas com elementos semânticos HTML5. No `body` deverá ter:
    1. dentro de um elemento `header` deverá incluir o cabeçalho, com o titulo do site e fotografia 
    2. o menu de navegação deverá estar dentro do elemento `nav`
    3. o conteúdo dentro de um elemento `main`. Dentro do `main`, use elementos `section` para dividir o conteúdo em secções (cada elemento `section` deverá ter um elemento `hx` e parágrafos `p`).
    4. um novo elemento `footer` com o seu nome, numero, universidade, e ano, tudo numa linha.
2. Nas tabelas, utilize os elementos `caption`, `thead`, `tbody`, `tfoot`.
3. Nas imagens recorra a elemento `figure` e `figcaption`, tendo neste ultimo um elemento `details` para mostrar/esconder mais detalhes sobre a imagem.

Se visualizar no seu navegador as páginas HTML, verá que estes elementos nada mudaram em termos visuais. No entanto, estes permitirão aplicar estilos. Neste primeiro laboratório aplicaráa esta estrutura estilizações simples. No entanto, no lab5 esta estrutura permitirá criar layouts dinâmicos, configurados pelo CSS.

# 3. Página HTML5 & CSS

1. Crie uma nova página HTML `html5-css.html` que tenha o mesmo cabeçalho das restantes.
2. Insira um elemento `h3` com o título HTML5 e CSS. Esta página terá 3 secções, estruturadas com elementos `section`, onde cada uma terá um breve texto e uma tabela. 
3. Crie uma secção com o elemento intitulada HTML 5 onde deverá incluir:
    1. uma frase introdutória sobre o HTML5
    2. um tabela com :
       * na primeira coluna todos os elementos HTML5 apresentados na aula, um por linha. 
       * na segunda coluna, para cada elemento HTML5 deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google)
       * na terceira coluna deverá incluir uma breve descrição a explicar onde utilizou. 
4. Crie uma subsecção intitulada CSS onde deverá incluir:
    1. uma frase introdutória sobre CSS 
    2. uma tabela com todos os tipos de seletores CSS, um por linha. Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google), e na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou. 
    3. uma tabela com todos os combinadores de seletores apresentados na aula, um por linha. Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google), e na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou.

# 4. Estilização com CSS

Para a definição dos estilos será usado um único ficheiro estilos.css, que guardará todos os estilos usados nas páginas. Em cada ficheiro HTML deverá existir um link para este ficheiro, de modo a permitir usar os estilos.

1. crie o ficheiro estilos.css 
2. deverá utilizar todos os tipos seletores apresentados na aula em pelo menos 3 sitios diferentes. 
3. Deverá utilizar pelo menos três composições de selectores (descendentes, filhos `>`, adjacentes `~`, imediatamente adjacentes `+`, agrupados `,`). 
4. Para o texto do menu, deverá utilizar os selectores de pseudo-classe `link`, `visited`, `hover`, `active` para configurar os links utilizando apenas as cores da palete, assim como os selectores `before` e `after` no menu quando passar com o rato por cima. Inclua, antes de cada palavra do menu, um icon adequado, usando ícones Google, Awesome Font ou Bootstrap. 
5. Escolha e use uma Google font para o seu website.
6. Configure a cor de background do seu website, assim como de alguns elementos HTML5 usando seletores adequados. 
7. Em particular nas tabelas e no poema os selectores de pseudo-classe assim como os pseudo-elementos, explorando cores de fonte e fundos diferentes. Por exemplo, introduza variedades de cor nas linhas pares e impares das tabelas.
9. Deverá recorrer aos 6 seletores de atributo `=`, `~=`, `|=`, `^=`, `$=` e `*=` para configurar as cores e larguras das molduras em redor das imagens da página interesses.
10. No texto descritivo, use os pseudo-elementos first-letter, first-line para estilizá-lo.
11. nos seus formulários, remova o uso de quebras de linha `br` para colocar inputs em linhas diferentes. Em vez disso, transforme os elementos `input` em blocos através da propriedade `display`. 
12. No formulário de comentário, atualize a informação relativa ao elemento escondido, que deverá indicar que o comentário é referente ao lab 4.
13. estilize as molduras (border) das imagens e iframes usando seletores, sem recorrer a classes.

# 5. Multimedia

1. Na página de multimédia insira mais algumas imagens, aplicando a técnica de sobreposição de imagens e texto umas por cima das outras, recorrendo a posições absolutas e relativas. 
2. Explore também com a propriedade sticky e fixed, em imagens a colocar no background.

# 6. Submissão

1. Verifique que todos os links do seu website funcionam devidamente.
2. Inclua um ficheiro README.md com o link para a sua palicação no Heroku.
3. Carregue a sua pasta no seu repositório Github através dos seguintes passos:
    1.  abra o processador de comandos e posicione-se dentro da pasta do seu repositório (`pw-labs-nomeapelido-numero`).
    2.  escreva as seguintes instruções:
        * `git add *`
        * `git commit –m "submissão laboratório 3"`
        * `git push`
4. Sincronize o GitHub com o Heroku tal como fez no [lab1](https://github.com/ULHT-PW-2020-21/pw-lab1). Deverá ir ao Heroku e, em Deploy, fazer deploy branch, de forma a colocar disponível na cloud os novos conteúdos criados. 
5. Verifique que o seu website online funciona corretamente, mostra todas as imagens e os hiperlinks funcionam devidamente.
6. No seguinte [ficheiro](https://drive.google.com/file/d/1kphRYAo78NSxWznBXHqNbPksELqlyloI/view) garanta que esteja:
    * link da sua aplicação Heroku
    * link do seu repositório privado no GitHub
    * adicione os docentes de PW como membros do seu repositório, que têm como usernames no GitHub: luciostuder, logdarkmatter, rfgsantos.

Esperamos que tenha gostado de aplicar os conhecimentos de HTML5 e CSS!

