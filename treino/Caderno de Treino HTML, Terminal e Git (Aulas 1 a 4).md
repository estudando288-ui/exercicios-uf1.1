# Caderno de Treino: HTML, Terminal e Git

*Exercícios práticos de reforço sobre o que já aprendeu nas aulas 1 a 4*

---

## Como usar este caderno

Os exercícios usam **apenas** o que já foi ensinado: terminal, estrutura HTML, títulos, `strong`, `em`, `br`, comentários, entidades, imagens, `abbr`, `span`, `blockquote`, `div`, elementos semânticos, validador do W3C e o ciclo do Git. **Não** usam listas, links nem CSS, porque ainda não foram dados.

**Regras de ouro**

1. Escreva o código **à mão**, sem copiar e colar de soluções. É assim que se aprende.
2. Nomes de ficheiros e pastas: **sem espaços, sem acentos e em minúsculas**.
3. Depois de cada página, **valide no W3C** (https://validator.w3.org/#validate\_by\_input) e só avance com zero erros.
4. No fim de cada exercício, faça o ciclo de trabalho: `git add .` → `git commit -m "mensagem clara"` → `git push`.
5. Se ficar preso, leia a mensagem de erro, volte ao guia da aula e só depois consulte o gabarito no fim.

**Pasta de trabalho**

Todos os exercícios ficam numa pasta nova dentro do seu repositório:

```
exercicios-uf1.1/
├── sessao-01/ ... sessao-04/
└── treino/
    ├── ex-01/
    ├── ex-02/
    └── ...
```

**Níveis**

| Nível | Tema | Exercícios |
| --- | --- | --- |
| 1 | Terminal e esqueleto HTML | 1, 2 |
| 2 | Texto, títulos e erros | 3, 4 |
| 3 | Imagens e atributos | 5, 6 |
| 4 | Semântica | 7, 8 |
| 5 | Git e projeto final | 9, 10 |

---

## Nível 1: Terminal e esqueleto HTML

### Exercício 1: Montar o ambiente só com o terminal

**Objetivo:** criar toda a estrutura de pastas e ficheiros sem usar o rato.

1. Abra o VS Code na pasta `exercicios-uf1.1` e um terminal novo (**Ctrl + \`**).
2. Confirme onde está com `pwd`.
3. Crie a pasta `treino` e entre nela:
   - `mkdir treino`
   - `cd treino`
4. Crie as pastas `ex-01`, `ex-02`, `ex-03` e `ex-04` com **um único** comando `mkdir`.
5. Entre em `ex-01` e crie os ficheiros `index.html` e `notas.txt` com **um único** comando `New-Item`.
6. Use `ls` para confirmar que os dois ficheiros existem.
7. Volte à pasta anterior com `cd ..` e depois à raiz do repositório com outro `cd ..`.
8. Corra `git status`. O que o Git diz?

**Critérios de sucesso**

- [ ] A estrutura `treino/ex-01 ... ex-04` existe.
- [ ] `ex-01` tem `index.html` e `notas.txt`.
- [ ] Usou `mkdir` e `New-Item` com vários nomes de uma só vez.
- [ ] Sabe explicar o que faz `cd ..`.

**Pergunta de relatório:** o que significa a palavra `untracked` que aparece no `git status`?

### Exercício 2: O esqueleto de memória

**Objetivo:** escrever a estrutura completa de uma página sem olhar para apontamentos.

1. Em `treino/ex-01`, abra o `index.html`.
2. Escreva, **de memória**, a estrutura completa:
   - `<!doctype html>`;
   - `html` com `lang="pt-PT"`;
   - `head` com `meta charset="UTF-8"` e `title`;
   - `body`.
3. O `title` deve ser **"Sobre mim"**.
4. No `body`, escreva:
   - um `h1` com o seu nome;
   - três `h2`: **Quem sou**, **O que estudo** e **O que quero ser**;
   - pelo menos um parágrafo debaixo de cada `h2`.
5. Use pelo menos um `<strong>` e um `<em>`.
6. Acrescente um comentário antes de cada `h2`.
7. Termine com `<hr />` e um parágrafo com `&copy; 2026` e o seu nome.
8. Abra com o **Live Server**, valide no W3C e faça o ciclo do Git com a mensagem `Exercício 2: sobre mim`.

**Critérios de sucesso**

- [ ] O separador do browser mostra "Sobre mim".
- [ ] Só há **um** `h1`; os `h2` não saltam níveis.
- [ ] O © aparece corretamente (escrito com `&copy;`).
- [ ] O validador não mostra erros.

**Desafio bónus:** escreva no `notas.txt` os 5 elementos da estrutura base por ordem (do mais exterior ao mais interior) e porque é que o `meta charset` é importante.

---

## Nível 2: Texto, títulos e erros

### Exercício 3: Caça aos erros, versão 2

**Objetivo:** encontrar e corrigir erros, um de cada vez, como na aula 2.

1. Em `treino/ex-02`, crie `erros2.html` e copie **exatamente** este código (com os erros!):

```
<html>
  <head>
    <title>Feira do Livro</title>
  </head>
  <body>
    <h1>Feira do Livro de Lisboa</h1>
    <h1>Programa</h1>
    <p>Há <strong>mais de 100 <em>editoras</strong></em> presentes.</p>
    <h4>Dia 1</h4>
    <p>Crianças com idade < 12 anos entram grátis.
    <!-- Sessão de autógrafos -->
    <p>Os autores assinam livros às 18h.</p>
    <img src="feira.jpg" width="240" height="160" />
    <hr />
    <p>&copy; 2026 Feira do Livro</p>
  </body>
</html>
```

2. Abra com o Live Server e depois no validador do W3C.
3. O ficheiro tem **8 erros** (alguns o validador aponta; outros só se percebem a ler com atenção). Corrija-os **um de cada vez**, guardando e vendo o que muda.
4. No fim, o validador não deve mostrar erros. (A imagem `feira.jpg` não existe, por isso não aparece; isso é normal.)
5. Escreva em `notas.txt` a lista dos 8 erros: linha, o que estava mal e o que fez.
6. Ciclo do Git com a mensagem `Exercício 3: correção de erros`.

**Perguntas de relatório**

1. Qual dos erros não foi apontado pelo validador mas ainda assim está errado? Porquê?
2. Porque é que a ordem de fecho das tags `strong` e `em` importa?

### Exercício 4: Do texto simples ao HTML

**Objetivo:** transformar um texto sem tags numa página bem organizada.

1. Em `treino/ex-03`, crie o ficheiro `bolo-de-bolacha.txt` com este texto:

```
Bolo de Bolacha da Tia Rosa

O bolo de bolacha é a sobremesa que nunca falta nos aniversários lá de casa. Não precisa de forno e fica sempre perfeito.

Ingredientes

1 pacote de bolacha Maria
250 g de manteiga
200 g de açúcar
4 gemas de ovo
1 chávena de café forte

Preparação

Passo 1
Bata a manteiga com o açúcar até ficar cremosa.

Passo 2
Junte as gemas, uma a uma, sem parar de bater.

Passo 3
Molhe as bolachas no café e faça camadas alternadas com o creme.

Passo 4
Leve ao frigorífico durante 6 horas.

Dicas

IMPORTANTE: use café frio, senão as bolachas desfazem-se.
Fica ainda melhor no dia seguinte.

© 2026 Receitas da Tia Rosa
```

2. Crie `bolo-de-bolacha.html` com a estrutura completa. O `title` é o nome da receita.
3. Escolha o elemento certo para cada parte:
   - nome da receita → `h1`;
   - Ingredientes, Preparação, Dicas → `h2`;
   - cada Passo → `h3`;
   - ingredientes num só parágrafo, um por linha, com `<br />`.
4. `<strong>` no aviso **IMPORTANTE**; `<em>` em pelo menos uma palavra à sua escolha.
5. Um comentário antes de cada capítulo.
6. Rodapé com `<hr />` e `&copy;`.
7. Valide e faça o ciclo do Git com a mensagem `Exercício 4: bolo de bolacha`.

**Critérios de sucesso**

- [ ] Um só `h1`, três `h2` e quatro `h3`.
- [ ] Os ingredientes aparecem um por linha.
- [ ] O código está indentado e o validador não mostra erros.

**Desafio bónus:** escreva a frase `Use a tag <br /> para mudar de linha` num parágrafo da página, de modo a que as tags apareçam como **texto** no browser.

---

## Nível 3: Imagens e atributos

### Exercício 5: A ficha de um lugar

**Objetivo:** usar `img`, `alt`, `width`, `height`, `abbr`, `span`, `blockquote` e `div`.

1. Em `treino/ex-04`, crie a pasta `imagens` e ponha lá uma fotografia sua (ou qualquer imagem) com nome simples, por exemplo `lugar.jpg`.
2. Crie `lugar.html` com a estrutura completa. Escolha **um lugar** de que goste (praia, monumento, café, bairro).
3. Escreva:
   - um `h1` com o nome do lugar;
   - a imagem **antes** do `h1`, com `src`, um bom `alt`, `width="240"` e `height="160"`;
   - três `h2` com parágrafos: **Onde fica**, **Porque gosto** e **Quando ir**;
   - uma abreviatura marcada com `<abbr title="...">` (por exemplo, UNESCO, EUA, CV);
   - uma palavra noutra língua com `<span lang="...">` (por exemplo, `lang="en"` em *sunset*);
   - uma frase de alguém sobre o lugar num `blockquote`, com o nome de quem a disse num parágrafo a seguir, **os dois dentro de uma `div`**.
4. Use `<strong>`, `<em>`, comentários antes de cada `h2` e rodapé com `<hr />` e `&copy;`.
5. Valide e faça o ciclo do Git com a mensagem `Exercício 5: ficha de um lugar`.

**Critérios de sucesso**

- [ ] A imagem aparece e o `alt` descreve **o que se vê**.
- [ ] Ao passar o rato na abreviatura, aparece o significado.
- [ ] O `blockquote` e o nome do autor estão dentro da mesma `div`.
- [ ] O validador não mostra erros.

**Pergunta de relatório:** para que serve o atributo `lang` num `span`? Quem beneficia?

### Exercício 6: Oficina de texto alternativo

**Objetivo:** aprender a escrever bons `alt`. Este exercício é de escrita, sem código novo.

Em `treino/ex-04`, crie `alt.txt`. Para cada situação, escreva o `alt` que usaria e explique em **uma frase** porquê.

1. Fotografia de uma sardinha assada num prato, com pimentos e pão.
2. O logótipo do seu curso (um livro aberto azul com o texto "DAWFS").
3. Uma imagem puramente decorativa: uma linha ondulada que só serve de enfeite.
4. Um gráfico que mostra que as vendas subiram de 100 para 250 entre janeiro e junho.
5. Uma fotografia de uma criança a rir ao lado de uma barraca de doces numa feira.

**Critérios de sucesso**

- [ ] Nenhum `alt` começa por "imagem de" ou "foto de" (o leitor de ecrã já diz que é uma imagem).
- [ ] O `alt` descreve o **conteúdo e a função**, não o nome do ficheiro.
- [ ] Para a imagem decorativa, sabe qual é o valor correto do `alt` (pense: o que é que um leitor de ecrã deve fazer com ela?).

---

## Nível 4: Semântica

### Exercício 7: Qual é o elemento certo?

**Objetivo:** escolher entre `header`, `nav`, `main`, `section`, `article`, `aside`, `footer` e `div`. Exercício de escrita.

Em `treino/ex-04`, crie `semantica.txt` e responda:

**Parte A.** Para cada conteúdo, escreva o elemento mais adequado:

1. O logótipo e o título principal no topo da página.
2. O menu com as secções do site.
3. A caixa lateral com uma curiosidade que não é essencial ao texto.
4. Um comentário de um leitor num blog, que faria sentido sozinho.
5. O capítulo "Programa" de uma página de evento, com o seu título `h2`.
6. A linha final com os direitos de autor.
7. Um bloco que só serve para agrupar duas coisas, sem significado especial.

**Parte B.** Verdadeiro ou falso (e corrija se for falso):

1. Uma página pode ter vários `main`.
2. Cada `section` deve ter um título.
3. O `header` só pode aparecer uma vez na página.
4. O `aside` pode ficar dentro do `main`.
5. `head` e `header` são a mesma coisa.

### Exercício 8: A Feira do Livro, construída do zero

**Objetivo:** construir uma página inteira já com a estrutura semântica certa, como no Festival da Sardinha.

1. Em `treino/ex-04`, crie `feira-do-livro.txt` com este texto:

```
Feira do Livro de Lisboa

Todos os anos, entre maio e junho, o Parque Eduardo VII enche-se de livros, autores e leitores. É a maior feira de livros do país.

Programa

A feira dura duas semanas. Há lançamentos de livros ao final da tarde, sessões de autógrafos ao fim de semana e atividades para crianças todas as manhãs. A entrada é gratuita.

Autores

Passam pela feira escritores portugueses e estrangeiros. Muitos aproveitam para conversar com os leitores e assinar os seus livros nas barracas das editoras.

Primeiro testemunho

"Vou todos os anos e volto sempre com mais livros do que planeei."
— Inês Carvalho, leitora de Almada

Segundo testemunho

"Conhecer quem escreveu o livro muda a forma como o lemos."
— Tiago Mendes, professor de Português

Curiosidade

Sabiam que a primeira Feira do Livro de Lisboa se realizou em 1930? Na altura, tinha apenas algumas dezenas de barracas.

Informações práticas

Local: Parque Eduardo VII, Lisboa.
Horário: das 12h às 22h.
Preço: entrada gratuita.

© 2026 Feira do Livro de Lisboa
```

2. Crie `feira-do-livro.html` com a estrutura completa. O título do separador é "Feira do Livro de Lisboa".
3. Organize com os elementos semânticos certos:
   - `header` com o `h1` e a frase de abertura;
   - `nav` com o texto `Programa · Autores · Testemunhos · Informações`;
   - `main` com todo o conteúdo;
   - uma `section` com `h2` para **Programa**, **Autores** e **Informações práticas**;
   - uma `section` **Testemunhos** com **dois** `article` seguidos, cada um com `blockquote` e o nome do autor;
   - a curiosidade num `aside` dentro do `main`;
   - `footer` com `&copy; 2026 Feira do Livro de Lisboa`.
4. Use `<strong>`, `<em>` e um comentário antes de cada secção.
5. Valide e faça o ciclo do Git com a mensagem `Exercício 8: feira do livro`.

**Critérios de sucesso**

- [ ] Existem `header`, `nav`, `main`, 4 `section`, 2 `article`, `aside` e `footer`.
- [ ] Só há **um** `main`.
- [ ] Cada `section` tem `h2`.
- [ ] Os dois testemunhos aparecem um a seguir ao outro.
- [ ] O validador não mostra erros.

**Desafio bónus:** abra a página nas DevTools (botão direito → **Inspecionar**), vá ao separador **Accessibility** e conte os *landmarks* reais que o browser encontra. Escreva quais são.

---

## Nível 5: Git e projeto final

### Exercício 9: O ciclo do Git em modo treino

**Objetivo:** ganhar rotina com `git status`, `git add`, `git commit`, `git log` e `git push`.

1. Na raiz do repositório, corra `git log --oneline` e leia as mensagens dos seus commits.
2. Em `treino/ex-01/index.html`, mude o texto de um parágrafo. **Antes** de fazer `git add`, corra `git status` e anote o que vê.
3. Faça `git add .` e corra `git status` outra vez. O que mudou na cor e na descrição?
4. Faça `git commit -m "Atualiza parágrafo da página Sobre mim"`.
5. Repita o ciclo **três vezes**, cada vez com uma pequena alteração diferente (um título, um comentário, um `alt`) e uma mensagem **clara** de cada vez.
6. Corra `git log --oneline`. Deve ver pelo menos 3 novos commits.
7. Faça `git push` e confirme no GitHub que os commits aparecem.

**Critérios de sucesso**

- [ ] Cada commit tem uma mensagem que explica **o que mudou**.
- [ ] Nenhuma mensagem é do tipo "teste", "asdf" ou "alterações".
- [ ] Sabe explicar porque `add`, `commit` e `push` são três passos separados.

**Perguntas de relatório**

1. Qual é a diferença entre ver um ficheiro com `git status` antes e depois do `git add`?
2. Escolha a sua mensagem de commit menos clara de **todo o histórico** e escreva uma versão melhorada.

### Exercício 10: Mini-projeto final: o meu mini-site

**Objetivo:** juntar tudo numa pequena entrega.

1. Crie `treino/mini-site/` com a pasta `imagens` lá dentro.
2. Crie **três** páginas, todas com estrutura completa e semântica:
   - `index.html`: página inicial, com `header` (nome + imagem), `nav`, `main` e `footer`.
   - `sobre.html`: sobre si, com pelo menos três `section`.
   - `projeto.html`: uma página sobre um tema à sua escolha (um desporto, um filme, uma banda, uma comida), com pelo menos um `article`, um `aside`, um `abbr`, um `span lang` e uma imagem com bom `alt`.
3. Em cada página, o `nav` pode ser **só texto** (`Início · Sobre · Projeto`), porque ainda não aprendemos links.
4. Use em todas: `<strong>`, `<em>`, comentários, `&copy;` e `<hr />` ou `footer`.
5. Valide **as três** no W3C. Zero erros.
6. Faça o ciclo do Git, com **um commit por página**:
   - `Página inicial do mini-site`
   - `Página sobre do mini-site`
   - `Página do projeto do mini-site`
7. Faça `git push` e escreva em `mini-site/notas.txt` o endereço do repositório.

**Critérios de sucesso**

- [ ] Três páginas, três commits, validador a zero.
- [ ] Cada página tem **um** `h1` e **um** `main`.
- [ ] Todas as imagens têm `alt`, `width` e `height`.
- [ ] A estrutura de pastas está arrumada e sem acentos nem espaços.

**Desafio bónus:** peça a um colega para abrir o seu código e dizer, **só pela leitura**, o que cada zona da página faz. Se ele perceber sem perguntar, a sua semântica está boa.

---

## Quiz relâmpago (sem consultar)

Responda a todas e só depois consulte o gabarito.

1. O que faz o comando `pwd`?
2. Que comando cria **três** ficheiros de uma vez no PowerShell?
3. O que fazem as tags `<!doctype html>` e `<html lang="pt-PT">`?
4. Porque é que não se devem saltar níveis de títulos (de `h2` para `h4`)?
5. Como se escreve o símbolo © em HTML?
6. Como se escreve, num parágrafo, o texto `<h1>` para aparecer no ecrã e não ser interpretado?
7. Qual é a diferença entre `<strong>` e `<em>`?
8. O que acontece se uma `<title>` ficar sem a tag de fecho?
9. Qual é a diferença entre `git add`, `git commit` e `git push`?
10. Quando é correto usar uma `div` em vez de um elemento semântico?

---

## Gabarito

> Só consulte depois de tentar. Há muitas formas corretas de responder; use isto para **conferir**, não para copiar.

### Exercício 1

- Comandos possíveis: `mkdir ex-01, ex-02, ex-03, ex-04` e `New-Item index.html, notas.txt`.
- `untracked` quer dizer que o Git vê os ficheiros, mas ainda **não os está a acompanhar**: nunca foram adicionados com `git add`.

### Exercício 3 (os 8 erros)

| # | Linha | Erro | Correção |
| --- | --- | --- | --- |
| 1 | 1 | Falta `<!doctype html>` | Acrescentar na primeira linha |
| 2 | 1 | `<html>` sem `lang` | `<html lang="pt-PT">` |
| 3 | 2 a 4 | Falta `meta charset` no `head` | `<meta charset="UTF-8" />` |
| 4 | 7 | Dois `h1` na mesma página | Mudar "Programa" para `h2` |
| 5 | 8 | `strong` e `em` fechados em ordem errada | `<strong>mais de 100 <em>editoras</em></strong>` |
| 6 | 9 | Salto de `h2` para `h4` (neste caso, `h1` para `h4`, depois da correção do erro 4 fica `h2` para `h4`) | Mudar para `h3` |
| 7 | 10 | `<` solto no texto | `&lt;` |
| 8 | 10 | Parágrafo sem `</p>` | Acrescentar `</p>` no fim da linha |

- **Erro não apontado pelo validador:** o salto de nível de título (`h2` para `h4`) costuma ser só um aviso, mas quebra a hierarquia e prejudica a navegação por leitores de ecrã.
- **Ordem de fecho:** as tags devem fechar na ordem inversa da abertura, como caixas dentro de caixas. Se não, o navegador adivinha e o resultado pode ser inesperado.

### Exercício 4 (pistas)

- Estrutura esperada: `h1` → 3 × `h2` → 4 × `h3` (dentro de Preparação).
- Para mostrar a tag como texto: `Use a tag &lt;br /&gt; para mudar de linha`.

### Exercício 5 (pista)

- `<span lang="en">sunset</span>`.
- O `lang` ajuda os leitores de ecrã a pronunciar a palavra com a voz certa e os motores de pesquisa a perceberem o idioma.

### Exercício 6 (exemplos de resposta)

1. `alt="Sardinha assada num prato, com pimentos e pão"`: descreve o que se vê.
2. `alt="DAWFS"` ou `alt="Logótipo do curso DAWFS"`: um logótipo é descrito pela sua função/nome.
3. `alt=""` (vazio): uma imagem puramente decorativa deve ter alt vazio, para o leitor de ecrã a ignorar.
4. `alt="Gráfico: as vendas subiram de 100 para 250 entre janeiro e junho"`: transmite a informação importante do gráfico.
5. `alt="Criança a rir junto a uma barraca de doces numa feira"`.

### Exercício 7

**Parte A:** 1 `header`; 2 `nav`; 3 `aside`; 4 `article`; 5 `section`; 6 `footer`; 7 `div`.

**Parte B:**

1. **Falso.** Só pode haver um `main` por página.
2. **Verdadeiro.** Uma `section` sem título normalmente devia ser uma `div`.
3. **Falso.** Pode haver vários `header` (por exemplo, o da página e o de um `article`), embora o principal seja um só.
4. **Verdadeiro.** É o que fez no Festival da Sardinha.
5. **Falso.** O `head` tem metadados invisíveis; o `header` é o cabeçalho visível do conteúdo.

### Exercício 9

- Antes do `git add`, os ficheiros alterados aparecem em **vermelho** ("Changes not staged for commit"); depois, em **verde** ("Changes to be committed").
- Exemplo de melhoria de mensagem: `teste` → `Corrige título da página Sobre mim`.

### Quiz relâmpago

1. Mostra o caminho completo da pasta onde está.
2. `New-Item a.html, b.css, c.js`.
3. A primeira diz ao browser que o documento é HTML5; a segunda marca o elemento raiz e indica o idioma (português de Portugal).
4. Porque os títulos formam uma hierarquia, como um índice: saltar níveis confunde leitores e leitores de ecrã.
5. `&copy;`.
6. `&lt;h1&gt;`.
7. `<strong>` indica **importância** (normalmente a negrito); `<em>` indica **ênfase** (normalmente a itálico).
8. O navegador trata todo o conteúdo seguinte como parte do título, e a página aparece em branco.
9. `add` escolhe as alterações a guardar; `commit` guarda-as no histórico local com uma mensagem; `push` envia o histórico para o GitHub.
10. Quando precisa apenas de agrupar elementos e nenhum elemento semântico descreve aquele bloco.

---

## Folha de progresso

Marque ao concluir cada exercício.

| Exercício | Feito | Validado no W3C | Commit feito |
| --- | --- | --- | --- |
| 1. Terminal | ☐ | n/a | ☐ |
| 2. Sobre mim | ☐ | ☐ | ☐ |
| 3. Caça aos erros 2 | ☐ | ☐ | ☐ |
| 4. Bolo de bolacha | ☐ | ☐ | ☐ |
| 5. Ficha de um lugar | ☐ | ☐ | ☐ |
| 6. Texto alternativo | ☐ | n/a | ☐ |
| 7. Elemento certo | ☐ | n/a | ☐ |
| 8. Feira do Livro | ☐ | ☐ | ☐ |
| 9. Ciclo do Git | ☐ | n/a | ☐ |
| 10. Mini-site | ☐ | ☐ | ☐ |

Bom treino!
