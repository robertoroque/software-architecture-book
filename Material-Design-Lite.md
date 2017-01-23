# Material Design Lite

Por [Roberto Roque Silva](https://github.com/robertoroque) e [Virgínia Azevedo Soares](https://github.com/virsoares)

*Universidade Federal de Minas Gerais*

Material Design Lite permite que  o visual e o layout do Material Design para Android seja incorporado aos websites. Material Design Lite não foi construído a partir de nenhum framework JavaScript e visa otimizar o uso em cross-device, ou seja, utilização em diferentes plataformas web e permitir que os websites sejam automaticamente acessíveis.

## Introdução
Material Design Lite é uma biblioteca de componentes front-end que permite o desenvolvedor implementar a especificação do Material Design do Google usando HTML, CSS e JavaScript.  É uma implementação leve da especificação do Material Design (poucas dependências, baixa recursos, bem focado) por isso, chamado de "Lite".

O Material Design Lite é desenvolvido e mantido pela Google, sob a licença [Apache 2](https://github.com/google/material-design-lite/blob/master/LICENSE). 
Foi lançado em Julho de 2015.

### O que é Material Design Lite?

O Material Design Lite foi criado com o objetivo de ser uma linguagem visual que sintetiza os princípios do bom design com a inovação da ciência e tecnologia.

Os componentes são usados para criar sites e aplicativos atraentes, consistentes e funcionais. Páginas criadas com MDL conta com princípios de web design moderno, com a portabilidade do navegador, a independência do dispositivo e uma degradação suave.

A biblioteca de componentes MDL inclui novas versões dos controles de interface de usuários comuns, tais como botões, caixas de seleção e campos de texto adaptados para seguir os conceitos de Material Design. A biblioteca também inclui recursos avançados e especializados, como cartões, layouts, sliders, spinners, tabs, tipografia, entre outros. 

O MDL é gratuito para baixar e usar e pode ser usado com ou sem um ambiente de biblioteca ou de desenvolvimento. É um cross-browser, cross-OS web que pode ser usado por qualquer pessoa que queira escrever uma página web mais produtiva, portátil e, mais importante, utilizável.

### Utilização do MDL
A utilização do Material Design Lite na construção de um site é bem simples e pode ser feita de duas formas diferentes:
* Incluindo no seu HTML o CSS e JavaScript hospedados pela Google:
````HTML
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
<link rel="stylesheet" href="https://code.getmdl.io/1.2.1/material.indigo-pink.min.css">
<script defer src="https://code.getmdl.io/1.2.1/material.min.js"></script>
`````
* Fazendo o download do código do Material Design Lite:
Build no GitHub:
````shell
# Clone/copy the Material Design lite source code.
git clone https://github.com/google/material-design-lite.git
# Go into the newly created folder containing the source code.
cd material-design-lite
# Install necessary dependencies.
npm install && npm install -g gulp
# Build a production version of the components.
gulp
````
Via Bower:
````bower
bower install material-design-lite --save
````
Via NPM:
````npm
npm install material-design-lite --save
````
E depois referenciar no seu HTML no caminho que foi salvo:
````html
<link rel="stylesheet" href="./material.min.css">
<script src="./material.min.js"></script>
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
````
## Componentes
Material Design Lite (MDL) é uma biblioteca de componentes para desenvolvedores web baseados na filosofia do Material Design criado pela Google: 
> "A linguagem visual para nossos usuários que sintetiza os princípios clássicos de um bom design com a inovação e possibilidade de tecnologia e da ciência." 

Compreensão dos objetivos e princípios do Material Design é fundamental para o uso adequado dos componentes do MDL.

Como conceito de desenvolvimento e de técnica de UX e UI, o Material Design para Android usa o [Polymer](https://www.polymer-project.org/1.0/), que propõe para alta interatividade, sites orientados por dados e aplicativos. Já o MDL, foca primeiramente em sites com conteúdos simples como blogs, marketing e landing pages. Para isso, criou o conceito de Componentes.

### Layout
Layout apropriado e acessível é uma característica fundamental de todas as interfaces de usuário, independentemente do conteúdo ou função de um site. Design de página e apresentação é, portanto, um fator importante para a experiência geral do usuário. De acordo com as especificações do Material Design, o material que o Layout se baseia é o papel. A disposição da tela é como uma folha de papel, que pode ser dobrada para ser dividida, por exemplo.

Uso de princípios de layout MDL simplifica a criação de páginas escaláveis, fornecendo componentes reutilizáveis e incentiva a consistência em ambientes através da criação de elementos visuais reconhecíveis, aderindo às redes estruturais lógicas, e mantendo espaçamento apropriado através de múltiplas plataformas e tamanhos de tela. Layout do MDL é extremamente poderoso e dinâmico, permitindo uma grande consistência na aparência e no comportamento, mantendo a flexibilidade de desenvolvimento e facilidade de uso.

O componente de layout apresenta uma série de blocos de construção para a construção de páginas. Por exemplo, o grid: uma característica fundamental de qualquer framework front-end. O grid do MDL é construído com Flexbox e uma pequena ajuda do calc() do CSS.  Tem 12 colunas preparadas para grandes janelas, 8 colunas para o que podemos chamar de janelas do tamanho de tablet, e 4 colunas para janelas menores.

O componente de Layout do MDL também inclui navegação, tabs, footers, cada um dos quais tem sido otimizado para diferentes tamanhos de janelas.

![Layout com header fixo](https://i.imgur.com/vpcBjss.png)
*Imagem 1: Layout com header fixo*

Um Layout simples em MDL pode ser adicionado à uma página HTML, conforme a imagem acima, de acordo com o código de exemplo a seguir:
````html
<!-- Always shows a header, even in smaller screens. -->
<div class="mdl-layout mdl-js-layout mdl-layout--fixed-header">
  <header class="mdl-layout__header">
    <div class="mdl-layout__header-row">
      <!-- Title -->
      <span class="mdl-layout-title">Title</span>
      <!-- Add spacer, to align navigation to the right -->
      <div class="mdl-layout-spacer"></div>
      <!-- Navigation. We hide it in small screens. -->
      <nav class="mdl-navigation mdl-layout--large-screen-only">
        <a class="mdl-navigation__link" href="">Link</a>
        <a class="mdl-navigation__link" href="">Link</a>
        <a class="mdl-navigation__link" href="">Link</a>
        <a class="mdl-navigation__link" href="">Link</a>
      </nav>
    </div>
  </header>
  <div class="mdl-layout__drawer">
    <span class="mdl-layout-title">Title</span>
    <nav class="mdl-navigation">
      <a class="mdl-navigation__link" href="">Link</a>
      <a class="mdl-navigation__link" href="">Link</a>
      <a class="mdl-navigation__link" href="">Link</a>
      <a class="mdl-navigation__link" href="">Link</a>
    </nav>
  </div>
  <main class="mdl-layout__content">
    <div class="page-content"><!-- Your content goes here --></div>
  </main>
</div>
````

### Grid
O componente Grid do MDL é um método simplificado para organizar o conteúdo do site para vários tamanhos de tela. Ele reduz a carga de codificação normalmente necessário para exibir corretamente blocos de conteúdo em uma variedade de condições de exibição.

O Grid de MDL é definido e fechado por um container. A grade tem 12 colunas no tamanho da tela desktop, 8 no tamanho tablet, e 4 no tamanho do telefone, cada tamanho tem margens e espaçamentos predefinidos. As células são dispostas sequencialmente em uma linha, na ordem em que são definidos, com algumas exceções:

* Se uma célula não se encaixa na linha em um dos tamanhos de tela, ela passa para a seguinte linha.
* Se uma célula tem um tamanho de coluna igual ou maior do que o número de colunas para o tamanho da tela corrente, leva-se a totalidade da sua fila.

Grid é um recurso relativamente novo e não-padronizado na maioria das interfaces de usuário, e fornecer aos usuários uma maneira de visualizar o conteúdo de uma forma organizada que poderia ser difícil de compreender ou manter. Sua concepção e utilização é um fator importante na experiência geral do usuário.

![Estrutura do Grid do MDL](https://i.imgur.com/1iZ5sjx.png)

*Imagem 2: Estrutura do Grid do MDL*

### Tabs

O componente tab do MDL é um elemento da interface do usuário que permite que diferentes blocos de conteúdo compartilhem o mesmo espaço na tela de forma mutuamente exclusivos. Tabs são sempre apresentadas em conjuntos de duas ou mais e podem tornar mais fácil para explorar e alternar entre diferentes visões e aspectos funcionais de um aplicativo.

Tabs servem como "posições" para seus respectivos conteúdos; a guia ativa - aquela cujo conteúdo é exibido no momento - é sempre visualmente distinguida dos outros para que o usuário saiba que lidera o conteúdo atual apresentado.

Tabs são recursos estabelecidos, mas não padronizados em interfaces de usuários, permitem aos utilizadores visualizar blocos de conteúdos (geralmente chamados de painéis). Tabs salvam as telas nos estados reais e fornecem acesso intuitivo e lógico de dados, reduzindo a confusão dos usuários na navegação. Sua concepção e utilização é um fator importante na experiência geral do usuário.

![Estrutura do tab do MDL](http://i.imgur.com/RExinDJ.jpg)

*Imagem 3: Estrutura do Tab do MDL*

### Button

O componente button do MDL é uma versão melhorada do elemento ```` <button> ```` do HTML padrão. Um botton consiste em texto e/ou imagem que comunica de forma clara qual ação ocorrerá quando o usuário clicar ou tocar. O componente button fornece vários tipos de botões que permitem que você adicione tanto a tela quanto os efeitos de clique.

Os botões são recursos onipresentes na maiorias das interfaces de usuário, independe do conteúdo ou função do site. Sua concepção é, portanto, um fator importante para a experiência geral do usuário.

![Exemplos de botões do MDL](http://i.imgur.com/fSyqsBp.jpg)

![Exemplos de botões do MDL](http://i.imgur.com/YwuiSsT.jpg)
![Exemplos de botões do MDL](http://i.imgur.com/aeJaFYS.jpg)


*Imagem 4: Exemplos de botões do MDL*

### Table

O componente data-table do MDL é uma versão melhorada do elemento ```` <table> ```` do HTML padrão. A tabela de dados consiste em linhas e colunas de dados bem formatados e capacidade de interação com usuário apropriada.

As linhas/colunas/células disponíveis em uma tabela de dados utilizam, em sua maioria, autoformatação, ou seja, uma vez que uma tabela é definida, as células individuais requerem pouca atenção específica. A sua facilidade de utilização a torna um componente conveniente para o programador e atraente e intuitiva para o usuário.

![Estrutura de uma tabela de dados do MDL](http://i.imgur.com/FCM1kCX.png)

*Imagem 5: Estrutura de uma tabela de dados do MDL*

Uma tabela de dados pode ser adicionada à uma página HTML, conforme a imagem acima, de acordo com o código de exemplo a seguir: 
````html
<table class="mdl-data-table mdl-js-data-table mdl-data-table--selectable mdl-shadow--2dp">
  <thead>
    <tr>
      <th class="mdl-data-table__cell--non-numeric">Material</th>
      <th>Quantity</th>
      <th>Unit price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="mdl-data-table__cell--non-numeric">Acrylic (Transparent)</td>
      <td>25</td>
      <td>$2.90</td>
    </tr>
    <tr>
      <td class="mdl-data-table__cell--non-numeric">Plywood (Birch)</td>
      <td>50</td>
      <td>$1.25</td>
    </tr>
    <tr>
      <td class="mdl-data-table__cell--non-numeric">Laminate (Gold on Blue)</td>
      <td>10</td>
      <td>$2.35</td>
    </tr>
  </tbody>
</table>
````
### Badge

O componente Badge do MDL é um elemento de notificação na tela. Um badge é constituído por um pequeno círculo, tipicamente contendo um número ou outro caractere, que aparece próximo a outro objeto. Um badge pode ser um notificador de que há itens adicionais em um objeto ou um indicador de quantos itens existem.

Um badge pode ser usado para chamar a atenção do usuários para itens que ele pode não ter percebido ou para enfatizar itens que precisam da sua atenção. Por exemplo:

* Uma notificação de "Nova Mensagem" pode vir  acompanhada de um badge contendo o número de mensagens não lidas;
* Uma notificação de "Você tem itens não comprados no seu carrinho de compras" pode vir acompanhada de um badge contendo o número de itens no carrinho.

O badge é quase sempre acompanhado por um link, de forma que o usuário possa acessar facilmente a informação adicional indicada por ele. Badges é um novo recurso na interface de usuários, que visa ajuda-los a descobrir uma informação adicional relevante. Sua concepção e utilização é, portanto, um fator importante para a experiência geral do usuário.

![Exemplo de badge do MDL](http://i.imgur.com/v3RUUim.png)

*Imagem 6: Exemplo de badge do MDL*

### Card

O componente Card do MDL é um elemento de interface que representa um pedaço de papel virtual que contém dados relacionados - como foto, texto e link - e são todos sobre um único assunto.

Os cartões são recursos convenientes para uma exibição coerente de conteúdos relacionados compostos por objetos diferentes. Eles também são adequados para a apresentação de objetos semelhantes, cujo os tamanhos podem ser variados. Os cartões possuem largura constante e altura variável, dependendo do seu conteúdo.

![Exemplo de card do MDL](http://i.imgur.com/f0xmkab.png)

*Imagem 7: Exemplo de cartão do MDL*

### Chips

O componente Chip do MDL é um elementos pequeno e interativo. São comumente usados para contatos, textos, regras, ícones e fotos.

![Exemplo de chip em MDL](http://i.imgur.com/RvVkz4i.png)

*Imagem 8: Exemplo de chip em MDL*

Um chip pode ser adicionado à uma página HTML, conforme a imagem acima, de acordo com o código de exemplo a seguir: 

````html
<!-- Contact Chip -->
<span class="mdl-chip mdl-chip--contact">
    <span class="mdl-chip__contact mdl-color--teal mdl-color-text--white">A</span>
    <span class="mdl-chip__text">Contact Chip</span>
</span>
<!-- Deletable Contact Chip -->
<span class="mdl-chip mdl-chip--contact mdl-chip--deletable">
    <img class="mdl-chip__contact" src="/templates/dashboard/images/user.jpg"></img>
    <span class="mdl-chip__text">Deletable Contact Chip</span>
    <a href="#" class="mdl-chip__action"><i class="material-icons">cancel</i></a>
</span>
````
### Dialogs

O componente Dialog do MDL permite a verificação das ações do usuário, entrada de dados simples e alertas para fornecer informações adicionais para eles.

Para usar esse componente é necessário que você esteja usando um browser que suporta o dialog. Apenas os browsers Chrome e Opera tem suporte nativo para escrita. Para os outros navegadores você terá que incluir o  *dialog polyfill* ou criar o seu próprio.

A partir do código abaixo é possível incluir um diolog no HTML, conforme no link [CodePen](http://codepen.io/Garbee/full/EPoaMj/).

````html
<body>
  <button id="show-dialog" type="button" class="mdl-button">Show Dialog</button>
  <dialog class="mdl-dialog">
    <h4 class="mdl-dialog__title">Allow data collection?</h4>
    <div class="mdl-dialog__content">
      <p>
        Allowing us to collect data will let us get you the information you want faster.
      </p>
    </div>
    <div class="mdl-dialog__actions">
      <button type="button" class="mdl-button">Agree</button>
      <button type="button" class="mdl-button close">Disagree</button>
    </div>
  </dialog>
  <script>
    var dialog = document.querySelector('dialog');
    var showDialogButton = document.querySelector('#show-dialog');
    if (! dialog.showModal) {
      dialogPolyfill.registerDialog(dialog);
    }
    showDialogButton.addEventListener('click', function() {
      dialog.showModal();
    });
    dialog.querySelector('.close').addEventListener('click', function() {
      dialog.close();
    });
  </script>
</body>
````

### Lists

As listas apresentam vários itens em linha vertical como um único elemento contínuo. Elas podem ser representadas de forma simples, com ícones, com avatares e ações, com avatares e controles, com duas linhas, com três linhas, entre outras opções.

![Exemplo de lsitas em MDL](http://i.imgur.com/sKibfp3.png)

*Imagem 9: Exemplo de lista com avatar e controles em MDL*

A lista representada no exemplo pode ser adicionada à página HTML a partir do código de exemplo a seguir:

````html
<!-- List with avatar and controls -->
<style>
.demo-list-control {
  width: 300px;
}

.demo-list-radio {
  display: inline;
}
</style>

<ul class="demo-list-control mdl-list">
  <li class="mdl-list__item">
    <span class="mdl-list__item-primary-content">
      <i class="material-icons  mdl-list__item-avatar">person</i>
      Bryan Cranston
    </span>
    <span class="mdl-list__item-secondary-action">
      <label class="mdl-checkbox mdl-js-checkbox mdl-js-ripple-effect" for="list-checkbox-1">
        <input type="checkbox" id="list-checkbox-1" class="mdl-checkbox__input" checked />
      </label>
    </span>
  </li>
  <li class="mdl-list__item">
    <span class="mdl-list__item-primary-content">
      <i class="material-icons  mdl-list__item-avatar">person</i>
      Aaron Paul
    </span>
      <span class="mdl-list__item-secondary-action">
        <label class="demo-list-radio mdl-radio mdl-js-radio mdl-js-ripple-effect" for="list-option-1">
          <input type="radio" id="list-option-1" class="mdl-radio__button" name="options" value="1" checked />
        </label>
    </span>
  </li>
  <li class="mdl-list__item">
    <span class="mdl-list__item-primary-content">
      <i class="material-icons  mdl-list__item-avatar">person</i>
      Bob Odenkirk
    </span>
      <span class="mdl-list__item-secondary-action">
        <label class="mdl-switch mdl-js-switch mdl-js-ripple-effect" for="list-switch-1">
          <input type="checkbox" id="list-switch-1" class="mdl-switch__input" checked />
        </label>
    </span>
  </li>
</ul>
````

### Progress

O componente Progress do MDL é um indicador visual da atividade de fundo de uma página web ou aplicativo. Um indicador de progresso consiste - tipicamente - em uma barra horizontal que contém uma animação que transmite uma sensação de movimento. Enquanto alguns dispositivos de progresso indicam um percentual aproximado ou específico de conclusão, o componente do MDL simplesmente comunica o fato de que uma atividade está em curso e ainda não está completa.

![Exemplo de progress em MDL](http://i.imgur.com/63zSHXE.png)

*Imagem 10: Exemplo de progress em MDL*

### Menu

O componente Menu do MDL é um elemento da interface do usuário que permite a seleção de um item, a partir de uma série de opções. A seleção normalmente resulta em uma ação, uma alteração na configuração ou outro efeito observável.

As opções de menu são sempre apresentadas em conjuntos de dois ou mais e podem ser programaticamente ativadas ou desativadas, conforme necessário. O menu aparece quando o usuário é convidado a escolher entre uma séria de opções, e, geralmente, é dispensado após a escolha do item.

![Exemplo de Menu em MDL](http://i.imgur.com/6dMTpAk.png)

*Imagem 11: Exemplo de Menu em MDL*

### Slider

O componente Slider do MDL é uma versão melhorada do elemento ```` <input type="range"> ```` do novo HTML5. Um slider consiste em uma linha horizontal sobre a qual tem um pequeno disco móvel e, tipicamente, comunica o valor que vai ser definido quando o usuário o move.

Slider é um recurso novo na interface de usuários, e permite que eles escolham um valor de um intervalo pré-determinado, movendo o polegar através do intervalo. 

![Exemplo de slider em MDL](http://i.imgur.com/poJ5W5P.png)

*Imagem 12: Exemplo de Slider em MDL*

### Snackbar

O componente Snackbar em MDL é um container usado para notificar o usuário sobre o status de uma operação. Ele é apresentado no botão da tela. Um snackbar pode conter um botão de ação para executar um comando para o usuário. As ações comprometidas devem ser desfeitas ou repetidas, se elas tiverem falhado, por exemplo. Se o snackbar não fornecer uma ação, então ele é um componente de brinde.

![Exemplo de Snackbar](http://i.imgur.com/OV5ouje.png)

*Imagem 13: Exemplo de Snackbar em MDL*

### Checkbox

O componente Checkbox do MDL é uma versão melhorada do padrão HTML ```` <input type="checkbox"> ````. Uma caixa de seleção consiste de um pequeno quadrado e, normalmente, o texto que comunica uma condição binária que será ativada ou desativada quando o usuário clica. As caixas de seleção, geralmente, aparecem em grupos e podem ser selecionadas ou desativadas individualmente. O componente permite que você adicione display e efeitos de clique.

![Exemplo de Checkbox em MDL](http://i.imgur.com/WBXYrWe.png)

*Imagem 14: Exemplo de Checkbox em MDL*

### Radio Button

O componente Radio do MDL é uma versão aprimorada do padrão HTML ````  <input type = "radio"> ````. Um radio button consiste em um pequeno círculo e, tipicamente, o texto que comunica uma condição que será definida quando o usuário clicar. Radios buttons sempre aparecem em grupos de dois ou mais, e, quando eles podem ser selecionados individualmente, só podem ser desativados selecionando um botão de opção diferente no mesmo grupo.

![Exemplo de Radio Button em MDL](http://i.imgur.com/ZCCIDN3.png)

*Imagem 15: Exemplo de Radio Button em MDL*

### Icon-togle

O componente icon-togle do MDL é uma versão aprimorada do padrão HTML ````<input type="checkbox">````. Um icon-togle consiste em um ícone definido pelo usuário que indica, por destaque visual, uma condição binária que será ativada ou desativada quando o usuário clicar. Assim como os componentes anteriores, eles podem aparecer individualmente ou em grupo.

![Exemplo de Icon-togle em MDL](http://i.imgur.com/gjI1rZm.png)

*Imagem 16: Exemplo de Icon-togle em MDL*

### Switch

O componente Switch do MDL é uma versão aprimorada do padrão HTML ````<input type="checkbox">````, assim como o componente anterior. O switch consiste de uma "faixa" horizontal com um indicador de estado circular em destaque e, normalmente, o texto que comunica um condição binária que será ativada ou desativada quando o usuário clicar.

![Exemplo de Switch em MDL](http://i.imgur.com/gRtBi3q.png)

*Imagem 17: Exemplo de Switch em MDL*

### Text Field

O componente Text Field do MDL é uma versão aprimorada do HTML padrão ````<input type="text">```` e ````<input type="textarea">````. Um campo de texto consiste em uma linha horizontal que indica onde a entrada do teclado pode ocorrer e, normalmente, o texto que comunica o conteúdo previsto no text field.

![Exemplo de Text Field em MDL](http://i.imgur.com/meobvvO.png)

*Imagem 18: Exemplo de Text Field em MDL*

### Tooltip

O componente Tooltip é uma versão melhorada do padrão HTML produzido pelo atributo ```` title ````. Uma tooltip consiste em texto e/ou imagem que comunica informações adicionais sobre um elemento quando o usuário passa por cima dele ou clica nele. O componente é pré-determinado para fornecer um elemento visual atraente que exibe conteúdo relacionado.

![Exemplo de Tooltip em MDL](http://i.imgur.com/jV25kLJ.png)

*Imagem 19: Exemplo de Tooltip em MDL*

## Templates
O MDL não é uma biblioteca apenas de componentes individuais. Também existe embutido nele os templates completos de sites, para guiar a criação de forma rápida e simples de alguns tipos de sites mais comuns utilizando o visual do Material Design.

Esses templates são utilizados, inclusive, em sites comerciais da própria Google. Os templates estão disponíveis para download e são 100% construídos com o MDL. 

Os modelos disponíveis são: 

**1.Blog:** Um modelo focado no mobile, ágil e que mostra como base uma imagem ou o texto do blog. Possui subscrição CTA, pesquisar e compartilhar links, e uma página de artigo expandível com comentários, contadores e capacidade de bookmarking built-in.

**2. Skin MDL do Android.com:** Versão atual do site do android.com construído com MDL. Conteúdo com uma navegação horizontal, recurso carrossel e longo formulário com rolagem sub páginas.

**3. Dashboard:** Um template responsivo e modular, construído para a visualização de dados e informações com uma navegação limpa e vertical, com perfil de usuário, busca e espaço dedicado para atualizações e filtros.

**4. Portfolio:** Um template moderno e limpo construído com o MDL para ser usado como portfolio ou blog. Inclui uma navegação no topo que utiliza o waterfall header como componente, cartões para exibir diferentes tipos de conteúdo e um rodapé.

**5. Text-heavy webpage:** Construído para apresentar informações densas, facilmente atualizável e otimizado para a legibilidade. Este template possui uma barra de navegação horizontal e fixa, além de textos explicativos, cartões e um mapa do site no rodapé profundamente vinculado ao conteúdo.

**6. Stand-alone article:** Um layout limpo otimizado para a apresentação de um conteúdo baseado apenas em textos. Possui navegação breadcrumb ("caminho de pão"), pesquisa, cabeçalhos claros e um rodapé que utiliza uma estrutura de cards para mostrar o conteúdo.

## Contexto
Material Design Lite é uma implementação "vanilla" em CSS, HTML e JavaScript do Material Design também desenvolvido pela Google. O termo "vanilla" não se refere a nenhum framework ou algo "concreto" utilizado no desenvolvimento e sim ao estilo de desenvolvimento. Vanilla, do inglês baunilha, quer dizer que é algo simples, plano e sem adornos, como um sorvete de baunilha. O termo indica que é uma interface web simples.

### Desenvolvimento

MDL foi escrito utilizando [BEM](https://en.bem.info): Block, Element, Modifier. É um método utilizado para construir os nomes das classes. Dessa forma as classes possuem nomes consistentes, isolados e expressivos.
A utilização da metodologia BEM para criação de arquivos CSS pode ser melhor entendida nesse post do [CSSWizardry](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/).

Componentes do MDL foram projetados a partir do zero, com melhora progressiva em mente. Tentamos construir sobre elementos HTML nativo, tanto quanto possível, com base em JavaScript quando é absolutamente necessário para "melhorias".

Um exemplo disso é o "Text only", que funciona somente com CSS sem nenhum uso de JavaScript (pode ser testado desligando o JavaScript pelo DevTools do Chrome, por exemplo).

Esse comportamento no-JavaScript pode ser problemático em navegadores mais antigos, como o IE9, que não implementa de forma completa funções mais recentes do HTML5. Por outro lado, existem templates do MDL, como o Component page, que utilizam mais JavaScript que os demais componentes.

MDL é implementado utilizando SASS, que é uma linguagem baseada em CSS que depois de compilada gera o CSS. Possui duas sintaxes diferentes, o SASS e o SCSS.
A partir do SASS, é possível criar variáveis para que seja usada em blocos em que se repete, reaproveitar código (que não seja copiando e colando), funções de cor, extend, aninhamento de seletores CSS e operações matemáticas. 

### Guia de Código
O desenvolvimento do MDL seguiu os guias do Google, que é seu principal stakeholder, em todo o desenvolvimento e também um [stylelint config](https://github.com/google/material-design-lite/blob/master/.eslintrc.yaml) próprio do MDL.
É essencial seguir esses guias nas implementações próprias que incorporam o MDL e, principalmente, nas extensões do MDL.
* [Guia de Estilo de Código HTML e CSS](https://google.github.io/styleguide/htmlcssguide.xml)
* [Guia de Estilo de Código JavaScript](https://google.github.io/styleguide/javascriptguide.xml)

Além dos guias, existem algumas regras que devem ser seguidas no desenvolvimento CSS. A terminologia para nomeação das classes em CCS deve seguir as seguintes orientações:
1. Comece cada classname com ````mdl-````. Isto fornece um namespace sólido de quaisquer classes fornecidas para que eles tenham a menor chance de colidir com outros projetos.
2. Pegue o nome do componente, converter para minúsculas e hyphenate. Por exemplo: Data Table, torna-se data-table. Este será o seu bloco.
3. Quebrar o elemento em partes lógicas. Normalmente, isso pode ser feito a partir da especificação e ver como ele quebra as partes comuns.
4. Uma vez que as partes estão quebradas, nomeá-los com valores mais próximos aos da especificação. Estes tornam-se seus elementos.
5. Por último, acrescente quaisquer modificadores onde a especificação permite múltiplas formas de um item.

### Time de Desenvolvimento
O MDL é desenvolvido e mantido pela Google. Pelo GitHub, a lista de contribuidores é enorme e nem chega a ser carregada completamente.

Atualmente a empresa trabalha na versão 2 do MDL e por isso possui uma equipe dedicada a essa versão e na correção de bugs da versão corrente.

É possível verificar a contribuição atual dos principais desenvolvedores:

![Contribuição por desenvolvedor](https://i.imgur.com/NZ3O22s.png)
*Imagem 20: Contribuição por desenvolvedor*

### Evolução do Sistema
![Adições e Deleções do MDL](https://i.imgur.com/ziHMXVV.png)
*Imagem: 21 Adições e Deleções do MDL*

Pelo GitHub, é possível verificar que, até o momento, o repositório do MDL teve dois grandes volumes de entrada de arquivos fontes: no início do projeto, em meados de Junho de 2014 e um ano depois, no lançamento do produto para utilização.

Durante o último ano, os commits no repositório não foram muito intesos. Mas ocorreram semanalmente, pois correspondem às correções e pequenas melhorias no código-fonte.

![Commits do último ano](https://i.imgur.com/jnFRXCn.png)
*Imagem 22: Commits do último ano*


## Problemas

Inúmeras questões UX existem com o Material Design e, naturalmente o Material Design Lite herda todos eles. Por exemplo, um dos elementos mais marcantes do MD, o botão flutuante, é frequentemente posicionado de forma inconsistente, e no celular, muitas vezes requer um esforço extra em seu polegar para tocar nele.
Em termos gerais, o MDL é bem construído, no entanto, existem algumas abordagens questionáveis; que é, por exemplo, mais uma estrutura que conta com o JavaScript para layout.
MDL, inclui um pacote tipografia, que é onde as coisas ficam realmente "acorrentadas". A fonte padrão é Roboto, e embora você possa mudar isso, a maioria dos usuários não vai fazê-lo.
CSS frameworks como Bootstrap, e Foundation, sempre incluíram elementos visuais. Eles não têm, porém, sido tão distintas como MDL. MDL dá um passo mais longe do que a maioria dos frameworks, que entrega um estilo visual completo.

### Problemas comuns relatados
Os problemas encontrados no MDL podem ser reportados por qualquer desenvolvedor pelo [GitHub Repo](https://github.com/google/material-design-lite/issues).

Muitos problemas abertos são solicitações dos usuários ou demandas que não fazem parte da especificação do MDL.

Atualmente, o produto está na versão 1.2.1 e está sendo desenvolvida a versão 2, onde diversas melhorias estão sendo incluídas.

O andamento do último mês da equipe de desenvolvimento na resolução dos problemas (que pode ser bugs no código ou não) está representada pelos gráficos abaixo, extraídos do [GitHub](https://github.com/google/material-design-lite/pulse):

![Issues tracker](https://i.imgur.com/eE5LJQn.png)
*Imagem 23: Gráficos de andamento das resoluções de problemas no MDL*

### Melhorias
Existe um roadmap já lançado para a versão 2 com diversas melhorias. Algumas delas:
* Criar o drawer persistent que existe no Material Design;
* Diminuir a quantidade de uso de JavaScript;
* Refazer todo o componente Layout;
* Criar botões com ícones;
* Implementar os componentes: Date Picker, Chips, Data Table, Grid List, Bottom Navigation, etc.

Extensões do MDL podem ser feitas locais por projeto, de acordo com a necessidade do desenvolvedor. Lembrando que é necessário utilizar os guias de desenvolvimento e ferramentas citadas para que o código esteja alinhado com o MDL.

## Conclusão
O Material Design Lite pode ser considerado como uma biblioteca poderosa para o desenvolvimento web, uma vez que facilita o desenvolvimento, já que questões de usabilidade, como sites responsivos e adaptáveis, deixam de ser uma preocupação. Também aproxima o layout web do padrão mobile de aplicativos Android, assim criando uma identidade visual única e até desbancando outros produtos de Smartphones, como a Apple, que propõe o Flat Design somente no Mobile e "afastando" todo o mundo web.

O MDL não pretende substituir outros frameworks já existentes, como o Bootstrap, como dito na própria página oficial do MDL:
> Material Desing Lite pode substituir muitas partes do Bootstrap. No entanto, ele não pretende ofertar todas as funcionalidades do Bootstrap. Em vez disso MDL pretende implementar os componentes especificados pela especificação do Material Design. Isso permite que ele para fornecer a solução mais abrangente e precisa disponível.

Já existe implementações diferentes do MDL e que não foram feitos pela Google, que implementam para Web os conceitos do Material Design (Materialize, Material Bootstrap, etc). A Google reconhece que a comunidade fez um ótimo trabalho na implememntação dessas bibliotecas CSS.

Porém, essas implementações já disponíveis interpretaram de sua forma a especificação do Material Design e não estabeleceu um padrão correto. Assim, a Google desenvolveu o MDL bem próximo de quem desenvolveu o Material Desing e o Chrome UX, para assegurar que esses conceitos fossem seguidos e determinados de forma mais próxima do que já existe. Quando existe alguma definição que não está totalmente concretizada, o MDL é capaz de oferecer opiniões e avaliação sobre a forma como estes devem ser resolvidos de uma maneira que tenta permanecer fiel ao Material Design.

O avanço de bibliotecas como o MDL são uma necessidade do mercado atual, que cada vez mais produz para a web e mobile, e consequetemente, atinge grande parte da população mundial que está cada vez mais conectada. Além disso, contribui ainda mais para o surgimento de novas ferramentas para desenvolvimento web (como Sass, BEM, etc) e até novas linguagens. Como foi o caso do HTML5 que permitiu um avanço significativo na Web.

## Referências
1. [Site oficial do Material Design Lite](https://getmdl.io)
2. [Site oficial do Material Design](material.google.com)
3. [Repositório GitHub do Material Design Lite](https://github.com/google/material-design-lite)
4. Serpa, Flávio. "Google lança ferramenta para criar websites em Material Design", http://www.b9.com.br/59213/design/google-lanca-ferramenta-para-criar-websites-em-material-design/
5. Rendle, Robin. "BEM 101", https://css-tricks.com/bem-101/
6. As imagens de 1 a 19 foram retiradas do [Site oficial do Material Design Lite](https://getmdl.io)
7. As imagens 20 a 23 foram retiradas do [Repositório GitHub do Material Design Lite](https://github.com/google/material-design-lite)
