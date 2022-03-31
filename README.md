# Boas vindas ao repositório do projeto Lista de Tarefas!

Projeto desenvolvido em novembro de 2020 por @brunacamposxx e avaliado pela @trybe
---

## Instruções para entregar seu projeto:

### 🗒ANTES DE COMEÇAR A DESENVOLVER:

1. Clone o repositório
  * `git clone https://github.com/brunacamposxx/to-do-list`.
  * Entre na pasta do repositório que você acabou de clonar:
    * `cd project-to-do-list`

---

### 👀Observações importantes:

* Os requisitos do seu projeto são avaliados automaticamente, sendo utilizada a resolução de tela de `1366 x 768` (1366 pixels de largura por 768 pixels de altura).

  * #### ⚠️ Logo, recomenda-se desenvolver seu projeto usando a mesma resolução, via instalação [deste plugin](https://chrome.google.com/webstore/detail/window-resizer/kkelicaakdanhinjdeammmilcgefonfh?hl=en) do `Chrome` para facilitar a configuração da resolução. ⚠️

* Atente-se para o tamanho das imagens que você utilizará neste projeto. **Não utilize imagens com um tamanho maior que _500Kb_.**
  * #### ⚠️ Utilize uma ferramenta [como esta](https://picresize.com/pt) para redimensionar as imagens. ⚠️

  * Caso a avaliação falhe com alguma mensagem de erro parecida com `[409:0326/130838.878602:FATAL:memory.cc(22)] Out of memory. size=4194304`, provavelmente as imagens que você está utilizando estão muito grandes. Tente redimensiona-las para um tamanho menor.

* Para verificar se a sua avaliação foi computada com sucesso, você pode verificar os **detalhes da execução do avaliador**.

  * Na página do seu _Pull Request_, acima do "botão de merge", procure por _**"Evaluator job"**_ e clique no link _**"Details"**_;

  * Na página que se abrirá, procure pela linha _**"Cypress evaluator step"**_ e clique nela;

  * Analise os resultados a partir da mensagem _**"(Run Starting)"**_;

  * Caso tenha dúvidas, consulte [este vídeo](https://vimeo.com/420861252) ou procure a monitoria.


* Você tem liberdade para adicionar novos comportamentos ao seu projeto, seja na forma de aperfeiçoamentos em requisitos propostos ou novas funcionalidades, **desde que tais comportamentos adicionais não conflitem com os requisitos propostos**.

  * Em outras palavras, você pode fazer mais do que for pedido, mas nunca menos.

* Contudo, tenha em mente que **nada além do que for pedido nos requisitos será avaliado**. _Esta é uma oportunidade de você exercitar sua criatividade e experimentar com os conhecimentos adquiridos._

---

## Requisitos Obrigatórios:

### 1 - Sua lista deve possuir o título "Minha Lista de Tarefas" em uma tag `<header>`. Esse título não varia de acordo com o conteúdo da lista. _Não confunda esse título com o título da página, que deve aparecer dentro da tag `head`_.
##### As seguintes verificações serão feitas:

- Será verificado se sua página possui uma tag `header` com o conteúdo `Minha Lista de Tarefas`

### 2 - Abaixo do título deve haver um pequeno e discreto parágrafo com `id="funcionamento"` e com o texto "Clique duas vezes em um item para marcá-lo como completo" explicando o funcionamento da lista para o usuário.
##### As seguintes verificações serão feitas:

- Será verificado que existe na sua página um elemento com o id `funcionamento` com o conteúdo `Clique duas vezes em um item para marcá-lo como completo`

### 3 - Deve haver um `input` com o `id="texto-tarefa"` onde o usuário poderá digitar o nome do item que deseja adicionar à lista.
##### As seguintes verificações serão feitas:

- Será verificada a existência de um elemento do tipo `input` com o id `texto-tarefa`.

### 4 - Deve haver uma lista ordenada de tarefas com o `id="lista-tarefas"`.
##### As seguintes verificações serão feitas:

- Será verificada a existência de um elemento `ol` com o id `lista-tarefas`.

### 5 - Deve haver um botão com `id="criar-tarefa"` e ao clicar nesse botão, um novo item deverá ser criado ao final da lista e o texto do input deve ser limpo.
##### As seguintes verificações serão feitas:

- Será verificada a existência de um elemento do tipo `button` com o id `criar-tarefa`
- No campo de input será digitado o texto de uma tarefa qualquer e, em seguida, clicar-se-á no botão de criar tarefa. Será verificado que, após o clique, o texto digitado aparece na lista e desaparece do input.
- A adição de elementos na lista será feita algumas vezes, e será checado se todos os itens criados permanecem na lista na medida em que novos são adicionados.

### 6 - Os itens da lista de tarefas devem ser ordenados por ordem de criação.
##### As seguintes verificações serão feitas:

- Três itens serão criados na lista e será checado se eles estão ordenados por ordem de criação - ou seja, primeiro o primeiro item criado, depois o segundo, e assim por diante.

### 7 - Ao clicar em um item da lista, altere a cor de fundo do item para cinza rgb(128,128,128).
##### As seguintes verificações serão feitas:

- Será verificado que, ao se carregar a página, os itens da lista **não tem** o estilo CSS `background-color: rgb(128, 128, 128)`
- Será verificado que, ao se clicar em um item da lista, ele passa a ter o estilo CSS `background-color: rgb(128, 128, 128)`

### 8 - Não deve ser possível selecionar mais de um elemento da lista ao mesmo tempo.
##### As seguintes verificações serão feitas:

- Será verificado que, quando um elemento da lista é selecionado, o elemento selecionado previamente deixa de sê-lo. Isso é verificado através da presença ou não do estilo `background-color: rgb(128, 128, 128)` no elemento.

### 9 - Ao clicar duas vezes em um item, ele deverá ser riscado, indicando que foi completo. Deve ser possível desfazer essa ação clicando novamente duas vezes no item.

    Pontos importantes sobre este requisito:

    * Crie uma classe CSS com o nome "completed" e defina a propriedade "text-decoration" com o valor "line-through".

    * Utilize a classe CSS "completed" para adicionar o efeito de letra tachada (riscada) às tarefas finalizadas.

##### As seguintes verificações serão feitas:

- Será verificado que, antes da ação ser disparada, o elemento adicionado à lista não tem nem a classe `completed` nem o estilo `line-through solid rgb(0, 0, 0)`.
- Será verificado que a ação pedida é disparada mediante duplo clique no elemento da lista e que os elementos da lista completos tem em si a classe `completed` e a propriedade `text-decoration` com o valor `line-through solid rgb(0, 0, 0)`
- Será verificado que, com um segundo duplo clique, um elemento completo deixa de sê-lo

### 10 - Deve haver um botão com `id="apaga-tudo"` que quando clicado deve apagar todos os items da lista.
##### As seguintes verificações serão feitas:

- Será verificado que existe um elemento `button` com o id `apaga-tudo`
- Será verificado que, dado que uma lista possui tarefas, um clique no botão a deixa vazia

### 11 - Deve haver um botão com `id="remover-finalizados"` que quando clicado remove **somente** os elementos finalizados da sua lista.
##### As seguintes verificações serão feitas:

- Será verificado que existe um elemento `button` com o id `remover-finalizados`
- Será verificado que, ao clicar no botão, todos os elementos marcados como feitos são removidos da lista

## BÔNUS

### 12 - Adicione um botão com `id="salvar-tarefas"` que salve o conteúdo da lista. Se você fechar e reabrir a página, a lista deve continuar no estado em que estava.
##### As seguintes verificações serão feitas:

- Será verificado que existe um elemento `button` com o id `salvar-tarefas`
- Será verificado que, quando a lista tem vários elementos, alguns dos quais marcados como finalizados, um recarregamento da página mantém a lista exatamente como está.

### 13 - Adicione dois botões, um com `id="mover-cima"` e outro com `id="mover-baixo"`, que permitam mover o item selecionado para cima ou para baixo na lista de tarefas.

    Pontos importantes sobre este requisito bônus:

    * Antes de começar a desenvolver essa funcionalidade, pare e pense. O que significa mover um item de uma lista para cima ou para baixo no **_DOM_**? Você já possui todas as habilidades necessárias para fazer isso.

    * Habitue-se a pensar nos casos especiais ao construir programas. O que acontece se o usuário tentar mover o primeiro item para cima ou o último para baixo?

##### As seguintes verificações serão feitas:

- Será verificada a existência de dois elementos `button`, um com o id `mover-cima` e o outro com o id `mover-baixo`
- Será verificado que, dado que diversos elementos foram acrescentados à lista, movimentá-los de formas diversas os deixa nas posições esperadas
- Será verificado que, caso algum elemento esteja finalizado, este status deve persistir ainda que se mova o elemento
- Será verificado que, caso nenhum elemento esteja selecionado, clicar nos botões não altera a lista
- Será verificado que um elemento que esteja selecionado deve se manter selecionado mesmo depois de movido
- _Caso especial!_ Será verificado que, caso se tente subir o elemento no topo da lista ou, caso se tente descer o último elemento da lista, esta não deve ser alterada

### 14 - Adicione um botão com `id="remover-selecionado"` que, quando clicado, remove o item selecionado.
##### As seguintes verificações serão feitas:

- Será verificada a presença de um elemento `button` com um id `remover-selecionado`
- Será verificado que, no clicar no botão, somente o elemento selecionado é removido

---


#VQV 🚀
