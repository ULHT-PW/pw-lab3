**PROGRAMAÇÃO WEB - aplicações web por perfeccionistas criativos**
 
# Lab 3: *Website com Quizz 🔘 e CSS 🖌* 

## Objetivos
* Estender o website criado no Laboratório 2 com mais algumas páginas.
* Explorar os vários tipos de entrada de formulário através da construção de um quizz sobre a cidade que escolheu.
* Praticar CSS, experimentando todos os seletores CSS aprendidos. O objetivo é conhecer os comandos de formatação, não fazer um website com super UX design! Isso aprenderá na disciplina Interação Humano Máquina.


## Recomendações
* Leia o enunciado todo com atenção antes de o começar a resolver para entender o que fará.
* Execute com atenção cada passo, certificando-se que implementa todos os detalhes. Contém todos os detalhes para a criação do website. 
* Se tiver alguma dúvida, recorra aos slides da aula que contêm todos os conhecimentos que precisa para realizar o laboratório.
* Este laboratório deverá ser concluido antes da sua aula prática da semana de 14.3, onde será avaliado. 
* Todos estes conteúdos (em especial os seletores e formularios) são conteúdos que saem na frequencia, pelo que exercite-os no laboratório para os conhecer.

## Pré-requisitos
* Deverá ter o Pycharm instalado para editar o código HTML de forma fácil.
* Deverá ter feito os [lab1](https://github.com/ULHT-PW/pw-lab1) e [lab2](https://github.com/ULHT-PW/pw-lab2). Caso não tenha feito, faça antes de fazer este laboratório.
* Deverá ter instalado o git no seu computador.

# 1. Estruturação do repositório de laboratórios

1. Clone (descarregue uma cópia) do GitHub para o seu computador o seu repositório com os laboratórios de Programação Web do GitHub:
    1. abra um processador de comandos (prima a tecla Windows e escreva `cmd` ou `Powershell`)
    2. escolha a pasta onde quer colocar o repositório (navegando com o comando `cd nome-de-pasta` para entrar numa determinada pasta)
    3. clone o seu repositório com o comando:
    ```bash
    > git clone https://github/seuUserName/pw-labs-nomeapelido-numero
    ```

2. Ainda usando a consola crie uma cópia do lab2 chamada lab3:
   * em linux:
    ```bash
    > cp -R lab2 lab3
    ```
   * em windows:
    ```bash
    > robocopy lab2 lab3 /E
    ```

3. Atualize o ficheiro `index.html`, índice dos seus laboratórios, incluindo na lista dos laboratórios este novo laboratório com um hiperlink para `lab3/index.html`:
        * Laboratório 3: Website com Quizz e seletores CSS

4. A estrutura da sua pasta `pw-labs-nomeapelido-numero` deverá ser como em baixo:
```
pw-labs-nomeapelido-numero
+-- index.php
+-- composer.json
+-- index.html
+-- lab1
+-- lab2
+-- lab3
```

7. Abra o ficheiro `index.html` na pasta clonada `pw-labs-nomeapelido-numero`. Verifique que os hiperlinks para o lab1, lab2 e lab3 funcionam devidamente. O lab3 para já é igual ao lab2.


# 2. Nova estrutura das páginas

1. Todas as suas páginas HTML deverão ser reestruturadas para integrar com elementos semânticos HTML5. No `body` deverá ter:

    1. dentro de um elemento `header` deverá incluir o cabeçalho, com o titulo do site e fotografia 
    
    3. o menu de navegação deverá estar dentro dum elemento `nav`
    
    5. o conteúdo dentro de um elemento `main`. Dentro do `main`, use elementos `section` caso existam várias secções (cada elemento `section` deverá ter dentro um elemento `h1` ou outro, e parágrafos `p`). Por exemplo, na página multimedia.html, utilize elementos `section` para dividir os vários conteúdos que tem (fotos, video e poema).
    
    7. um novo elemento `footer` com o seu nome, numero, universidade, e ano, tudo numa linha.
    
3. Nas imagens, vídeos e mapa, recorra a elemento `figure` e `figcaption`, tendo neste ultimo um elemento `details` para mostrar/esconder mais detalhes sobre a imagem.

Se visualizar no seu navegador as páginas HTML, verá que estes elementos nada mudaram em termos visuais. No entanto, estes permitirão aplicar estilos. Neste primeiro laboratório aplicará a esta estrutura estilizações simples. No entanto, no lab4 esta estruturação com elementos semânticos permitirá criar layouts dinâmicos, configurados pelo CSS.


# 3. Página com Quizz 🤓

1. Crie uma nova página HTML `quizz.html` que tenha o mesmo cabeçalho das restantes.

1. Esta página irá ter um formulário com um quizz sobre a cidade. Deverá fazer perguntas de vários tipos sobre a cidade, o formulário sendo enviado para um endereço de email (quando desenvolvermos o back-end, poderá processar os dados enviados e apresentar ao utilizador uma resposta). Nesta página irá experimentar todos os tipos de entrada que foram falados na aula. Implemente os passos a seguir descritos.

1. Insira um elemento h3 com a palavra Quizz.

3. insira um parágrafo com um texto introdutório a explicar que nesta página será feito um quizz para testar se o utilizador conhece bem a cidade que a página apresenta.

1. Crie dentro do form um elemento `fieldset`, coma uma legenda (por exemplo, "Quizz sobre «cidade»", "City quizz", "Mostre que conhece «cidade»"

1. Crie outro elemento `fieldset` para inserção de dados pessoais, com o titulo "info" (`fieldset` dentro de `fieldset`, sim 🤩!):
   * Nome
   * apelido
   * email (input de tipo email)

1. Crie outro elemento `fieldset` para inserção das perguntas do quizz, com título "perguntas":

1. Crie um quiz com perguntas sobre a cidade, explorando de forma imaginativa elementos input. 
    * Deverá utilizar cada um dos seguintes tipos (atributo `type`):
        * `text`
        * `radio`
        * `checkbox`
        * `date`
        * `image`
        * `color`
        * `number`
        * `range`
 
    * Deverá garantir que utiliza pelo menos uma vez cada um dos seguintes atributos:
        * `value`
        * `placeholder`
        * `autocomplete`
        * `size`
        * `max` e `min`
        * `maxlength`
        * `form`
        * `multiple`
        * `autofocus`
        * `required`
        * `pattern`

1. Inclua também perguntas usando os seguintes elementos:
   * `select`
   * `datalist`
   * `label`

1. Inclua  um elemento `textarea` para inserir um comentário

1. Inclua um elemento do tipo `submit` para submeter o seu formulário.

1. No marcador form, inclua os seguintes atributos `<form method="POST" action="mailto: seuemail@gmail.com" enctype="multipart/form-data">`. Assim, quem abrir a sua página, ao submeter o formulário enviará por email para si este.  
   * Quando desenvolvermos o back-end, poderá processar os dados enviados e apresentar ao utilizador uma resposta.

 
# 4. Página HTML5 & CSS 😎

1. Crie uma nova página HTML intitulada `html5-css.html` que tenha o mesmo cabeçalho das restantes.
 
2. Insira um elemento `h3` com o título HTML5 e CSS. Esta página terá 3 secções, estruturadas com elementos `section`, onde cada uma terá um breve texto e uma tabela. 
 
3. Crie uma secção com o elemento intitulada HTML 5 onde deverá incluir:
    1. uma frase introdutória sobre o HTML5
    2. um tabela com 3 colunas:
       * na primeira coluna, os elementos semânticos HTML5 apresentados na aula, um por linha. 
       * na segunda coluna, para cada elemento HTML5 deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use icones Google, por exemplo ❌ e ✔, ou então 😀 e 🙄)
       * na terceira coluna deverá incluir uma breve descrição a explicar onde utilizou. 
 
4. Crie uma subsecção intitulada CSS onde deverá incluir:
    1. uma frase introdutória sobre CSS 
    2. uma tabela com todos os tipos de seletores CSS, um por linha. Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google), e na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou. 
    3. uma tabela com todos os combinadores de seletores apresentados na aula, um por linha. Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google), e na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou.

# 5. Estilização com CSS 🖌

Para a definição dos estilos será usado um único ficheiro estilos.css, que guardará todos os estilos usados nas páginas. Em cada ficheiro HTML deverá existir um link para este ficheiro, de modo a permitir usar os estilos.

1. crie o ficheiro estilos.css 
 
2. deverá utilizar todos os tipos de seletores (tipo, classe, id, atributo, pseudo-classe, pseudo-elemento, veja o [slide](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.4-css-e-seus-seletores.pdf) 17), em pelo menos 3 sítios diferentes do seu HTML. A seguir sugere-se onde utilizar alguns destes. Não se esqueça de registar na tabela onde os utiliza!
 
3. Deverá utilizar pelo menos três composições de selectores (descendentes, filhos `>`, adjacentes `~`, imediatamente adjacentes `+`, agrupados `,`), veja o [slide](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.4-css-e-seus-seletores.pdf) 32). 

5. Escolha e use uma [fonte Google](https://fonts.google.com/) no o seu website. Veja no [video](https://lh3.googleusercontent.com/-PO1uxMdsqoA/Xpmn6QDUKHI/AAAAAAAA2qg/l1B6uSjPRu0eg_3EZkjp04siUjJb1dQxQCK8BGAsYHg/s0/2020-04-17.gif) como se procede:
    1. escolha uma fonte que gosta
    2. selecione os estilo que quer usar (no caso de apresentar várias variantes)
    3. copie na janela direita o link e insira no head de cada uma das suas páginas HTML
    4. especifique no ficheiro CSS que quer usar essa fonte em todo o lado, usando o seletor universal * e a regra CSS para especificar a familia da fonte, por exemplo 
`* {font-family: 'Syne Mono', monospace;} `
 
6. Configure a cor de background do seu website, assim como de alguns elementos HTML5 usando seletores adequados. em particular, na pagina do Quizz, use cores diferentes para o fundo de cada umdos `fieldsets`.
 
7. Para os elementos do seu menu:
    * utilize selectores de pseudo-classe (`link`, `visited`, `hover`, `active`) para configurar cores para os links (veja o [slide](https://moodle.ensinolusofona.pt/pluginfile.php/318343/mod_label/intro/pw-02.4-css-e-seus-seletores.pdf) 27)
    * especifique com selectores `before` e `after` (slide 31) efeitos que acontecem quando passa com o rato por cima de cada elemento do menu (use `hover`). 
    * No HTML inclua, antes de cada palavra do menu, um icon adequado premindo no teclado em `Windows + .` (pode escolher por exemplo 🏡 para home, 📷 para multimédia,🗺 localizaçao, etc). Pode também explorar [aqui](https://www.w3schools.com/icons/icons_reference.asp) ícones Google, Awesome Font ou Bootstrap; clique em "try" para entender como se usam:
       * deve incluir no elemento head um link ao repositório de icons. 
       * veja como se especifica o icon que pretende inserir (depende do repositório). Estes icones são extremamente leves e variados.

8. Nas tabelas e no poema os selectores de pseudo-classe assim como os pseudo-elementos, explorando cores de fonte e fundos diferentes. Por exemplo, introduza variedades de cor nas linhas pares e impares das tabelas.
  
9. Recorra a seletores de atributo (slide 25) para configurar as cores e larguras das molduras em redor das imagens da página interesses.
 
10. No texto descritivo (por exemplo no parágrafo da introdução), use os pseudo-elementos first-letter, first-line para estilizá-lo.
 
11. nos seus formulários, remova o uso de quebras de linha `br` para colocar inputs em linhas diferentes. Em vez disso, transforme os elementos `input` em blocos através da propriedade `display`. 
 
13. estilize as molduras (border) das imagens e iframes usando seletores, sem recorrer a classes.
 

# 7. Menu
Garanta que o menu inclui hiperlinks para as 3 novas páginas criadas (semelhante a todas as páginas).

# 7. Submissão

1. Verifique que todos os links do seu website funcionam devidamente.
2. Carregue a sua pasta do seu repositório (com as modificações efetuadas) no seu repositório Github através dos seguintes passos:
    1.  abra o processador de comandos e posicione-se dentro da pasta do seu repositório (`pw-labs-nomeapelido-numero`).
    2.  escreva as seguintes instruções:
        * `git add *`
        * `git commit –m "laboratório 3"`
        * `git push`
             * `git add` serve para propor mudaças, incluindo todos os ficheiros e pastas existentes como. o `commit` serve para confirmar as mudanças e que estas fiquem guardadas. o `push` serve para enviar as alterações (upload) para o repositório no GitHub.
3. Sincronize o GitHub com o Heroku tal como fez no [lab1](https://github.com/ULHT-PW/pw-lab1). Deverá ir ao Heroku e, em Deploy, fazer deploy branch, de forma a colocar disponível na cloud os novos conteúdos criados. 
3. Garanta que os docentes de PW são membros do seu repositório, que têm como usernames no GitHub: luciostuder, logdarkmatter, rfgsantos.
4. Verifique que o seu website online funciona corretamente, em particular mostra todas as imagens e os hiperlinks funcionam devidamente.
5. Garanta que preencheu o formulário do lab2, [form](https://forms.gle/d5sS3XtaHzRnfzQ87)

 # Fim ☀
 
Esperamos que tenha gostado de aplicar os conhecimentos sobre formulários e CSS no seu website &#127760;!
