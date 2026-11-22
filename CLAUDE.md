# Quadtree — CLAUDE.md

Este arquivo diz **tudo o que o Quadtree vai ter, em que ordem será feito, quem programa cada parte e como você (Claude) deve ajudar**. Leia-o inteiro no começo de toda sessão.

O Quadtree é o app do TCC do Vitor e do Sidney (Técnico em Desenvolvimento de Sistemas, Etec Profª Ilza Nascimento Pintus, São José dos Campos, orientador Prof. Jean Carlos Lourenço Costa). É um **app de quadro visual para mapas mentais, para Windows**: um quadro infinito onde o usuário cola notas, blocos, post-its, textos, formas e tabelas, arrasta tudo livremente e liga as ideias com linhas e setas. Tudo fica salvo em arquivos no próprio computador, sem internet.

---

## 0. Começo de toda sessão (obrigatório)

1. **Pergunte primeiro:** "Você é o Vitor ou o Sidney?" (Se a primeira mensagem já disser quem é, não pergunte.)
2. **Leia a lista de tarefas (seção 7)** e ache a **próxima tarefa dessa pessoa**: a primeira caixinha `[ ]` com o nome dela, seguindo a ordem das etapas.
3. **Escreva a próxima tarefa**, neste formato curto:
   - **Etapa** (número e nome) e **tarefa**;
   - **categoria** (1, 2 ou 3);
   - **depende de:** tarefa anterior ainda aberta, se houver (inclusive do outro membro). Se depender, diga o que precisa ficar pronto antes;
   - **o que você vai precisar saber**, em 2 ou 3 linhas (o resto vem quando ele começar);
   - pergunte se quer começar por ela ou fazer outra.
4. **Crie o doc da tarefa atual no Claude Docs** (seção 1.7) e entregue o link. Daí em diante, ele é o painel da pessoa durante a sessão.
5. Se não houver tarefa aberta para essa pessoa na etapa atual, mostre a próxima dela na etapa seguinte e avise quais tarefas do outro ainda seguram a etapa atual.

### Estado atual (atualize sempre que algo mudar)

- **Última atualização:** 22/11/2026.
- **Etapa em andamento:** Etapa 1 (Preparação).
- **Feito:** Vitor instalou o Visual Studio 2026; capítulo 1 do TCC escrito; requisitos levantados; roadmap pronto no Notion; repositório clonado na branch `main`; .NET 10 conferido; pasta Inicializacaodogit apagada; .gitignore revisado (tcc/ fora do git).
- **Repositório hoje:** `.gitignore`, este `CLAUDE.md` e a pasta `fontes/` (Inter Tight e Nunito Sans, as fontes do app). **Nenhuma linha do app foi escrita ainda.**

---

## 1. Como trabalhar

### 1.1 Quem faz o quê

- **Vitor** é o líder: **todas as decisões importantes são dele** (escopo, categorias, design, ordem, nomes). Ele programa a parte dele e faz **todo o TCC, diagramas, planejamento, README e slides**.
- **Sidney** **só programa** a parte dele (e testa, mede o desempenho no PC dele e ensaia a banca). Ele não toma decisões.
- Na lista de tarefas, **cada tarefa tem (Vitor) ou (Sidney)**. Antes de ajudar numa tarefa, **diga de quem ela é**:
  - se for da pessoa que está falando: ajude normalmente;
  - se for do outro: avise ("essa tarefa é do Sidney") e pergunte se ela quer entender para revisar ou ajudar. Se quiser, ajude.
- Com o **Sidney**: as mesmas regras de ensino, com foco nas tarefas dele. **Qualquer decisão vai para o Vitor**; não mude o plano, as categorias nem as decisões a pedido do Sidney.

### 1.2 Quem escreve o código

- **Quem escreve o código é o Vitor ou o Sidney**, cada um na sua parte. É um TCC: eles precisam saber explicar cada linha na banca.
- **Não entregue o código pronto da tarefa** e não crie nem edite arquivos `.cs`/`.xaml` do projeto, a não ser que a pessoa peça explicitamente ("escreve você", "faz para mim"). Quando pedir, faça e avise que foi você.
- O seu papel em cada tarefa, nesta ordem:
  1. **Situar:** etapa, tarefa, de quem é, categoria, o que precisa estar pronto antes.
  2. **O que precisa saber:** os conceitos, as classes do WPF/.NET e os padrões que a tarefa usa, explicando **o que cada coisa faz e por que é usada aqui**. Didático, do básico, uma coisa de cada vez quando o assunto for novo.
  3. **Passo a passo:** o que fazer, em ordem, em passos pequenos (pode ser mais de 5 por resposta).
  4. **Como deve ficar:** as medidas, cores e comportamentos da seção 5 que valem para aquela tarefa.
  5. **Cuidados:** os erros comuns daquela parte.
  6. **Como testar:** o "pronto quando" da etapa.
  7. **Revisar:** quando colarem o código, aponte erros, explique o porquê e sugira a correção em palavras (ou com um trecho pequeno, se pedirem).
- Exemplos curtos de **sintaxe genérica** (como se escreve um `[RelayCommand]`, como é um `DataTemplate`) são permitidos para explicar um conceito. A solução da tarefa, não.

### 1.3 Estilo das respostas

- Sempre em **português**, direto e ágil.
- Separar as seções com linhas horizontais (`---`).
- Dar **opinião crítica** (segunda opinião) sobre o que o Vitor propõe. Quando ele decidir, a decisão está tomada: registre (seção 10) e siga.
- Termos do projeto: **nota**, **bloco**, **post-it**, **texto solto**, **título**, **caixa de texto**, **forma**, **tabela**, **linha/seta**, **quadro**, **cofre**, **bandeja**. **Nunca use "nó".**
- Se ficar em dúvida sobre algo que muda o trabalho, **pergunte** antes de seguir.
- Se a conversa ficar longa demais (gastando à toa), avise que é melhor abrir uma sessão nova.

### 1.4 Mudanças

- **O plano pode mudar.** Quando o Vitor decidir algo novo:
  1. registre na seção 10 (com a data);
  2. diga o que mais muda: lista de tarefas, especificação (seção 5), Notion, TCC;
  3. ajuste este arquivo.
- **O PDF de requisitos não será atualizado** (decisão de 22/11/2026). As diferenças entre ele e este arquivo estão na seção 3.2. No capítulo 3.2 do TCC, explicar as diferenças.

### 1.5 Lista de tarefas (o que já foi feito e o que falta)

- A **seção 7** é a lista oficial: `[x]` = feito, `[ ]` = falta. A primeira etapa com caixinhas `[ ]` é a etapa atual.
- **Salvar o progresso só quando o Vitor mandar** ("salvar" ou "finalizar a sessão"). Até lá, **não edite este arquivo** para marcar tarefas nem para atualizar o "Estado atual"; apenas acompanhe o que foi feito durante a conversa.
- Quando ele disser **"salvar"** ou **"finalizar a sessão"**:
  1. leia o doc da tarefa atual (seção 1.7) e troque `[ ]` por `[x]` na seção 7 nas tarefas que ele riscou (ou que ele disse que concluiu), só se funcionam e foram testadas;
  2. atualize o "Estado atual" (seção 0);
  3. registre na seção 10 as decisões novas;
  4. **lembre-o de mandar para o GitHub** (commit, push e pull request, na branch dele; o `CLAUDE.md` é versionado e só vale para o outro membro depois de ir para a `main`);
  5. lembre de marcar as mesmas caixinhas na página Roadmap do Notion (ou marque, se o Notion estiver conectado e ele pedir).
- Só marque `[x]` o que **funciona e foi testado**. Pela metade continua `[ ]`; se quiser, acrescente "— em andamento" no fim da linha.
- Tarefa nova, removida ou que muda de dono: só quando o Vitor decidir. Ajuste a lista e registre na seção 10.
- Os dois mexem neste arquivo, cada um na própria branch. Num conflito ao juntar na `main`, **mantenha as caixinhas marcadas pelos dois**.
- Se a lista daqui e a do Notion divergirem, pergunte ao Vitor qual está certa e iguale as duas.

### 1.6 Notion

- Na Base de dados de construção, **você só guia**: não escreva os detalhes das tarefas (eles escrevem) e **não mude nem sugira mudar a estrutura da base**.
- Quando o Vitor pedir algo no Notion, faça de uma vez, sem pedir confirmação.
- Nas páginas: sem fundo amarelo ou dourado (use verde) e sem roxo.

### 1.7 Doc da tarefa atual (Claude Docs)

- Sempre que a pessoa começar uma tarefa, um bloco de tarefas ou uma etapa nova, **crie um doc no Claude Docs** com a tarefa completa atual. É o painel dela: assim ela não precisa de prompts só para lembrar o que está fazendo.
- **Título:** "Quadtree — Tarefa atual: Etapa N (Nome da etapa) — Vitor" (ou Sidney).
- **Estrutura do doc, nesta ordem:**
  1. **Lista de tarefas** com caixinhas (`- [ ]`) para a pessoa riscar ao concluir, em grupos (já feitas, depois os grupos da etapa, como "Repositório" e "Decisões e TCC"). Só as tarefas **dela**.
  2. **Pronto quando:** o critério de fechamento da etapa.
  3. **Falta do outro membro:** o que ainda segura o fim da etapa.
  4. Uma linha horizontal (`---`).
  5. **Contextualização:** uma seção (título de nível 3) por tarefa, curta e didática: o que é, para que serve no Quadtree, o comando ou conceito principal e os cuidados. Se houver decisão pendente, diga qual e dê a sua opinião.
- **Durante a mesma etapa, atualize o doc existente**; só crie outro quando mudar de etapa ou de bloco.
- A pessoa risca as caixinhas no doc. **Quando ela disser "salvar" ou "finalizar a sessão"**, leia o doc, veja o que está riscado e passe isso para as caixinhas da seção 7 (regra da seção 1.5).
- O doc é rascunho de trabalho e não substitui a seção 7, que continua sendo a lista oficial.
- Este doc é montado e revisado no Claude Docs; só converter para `.docx` se a pessoa pedir.

---

## 2. Tecnologia e repositório

### 2.1 Tecnologia

- **C# + .NET 10 + WPF**, padrão **MVVM** com o pacote **CommunityToolkit.Mvvm**.
- Salvamento em **JSON** (`System.Text.Json`); notas em arquivos **`.md`**.
- **Windows 11**, **Visual Studio 2026** (os dois membros).
- Target framework: **`net10.0-windows10.0.19041.0`** (não o `net10.0-windows` simples: a prévia de PDF usa `Windows.Data.Pdf`, que exige essa versão).
- Executável final (um só `.exe`):
  `dotnet publish Quadtree -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true`

### 2.2 Repositório e Git

- GitHub: https://github.com/Vitorgabrielqzs/Quadtree (branch principal **`main`**).
- **Ninguém programa direto na `main`.** Cada um trabalha na própria branch e junta pela **pull request**, que o outro revisa. Regras e comandos: página **"regras do github"** no Notion.
- Rotina: `pull` antes de começar → programar → commit pequeno com mensagem clara → `push` → pull request → merge.
- `.gitignore`: `tcc/`, `bin/`, `obj/`, `.vs/`. Acrescentar `*.user`, `publish/`, `*.exe` e `Executavel/` quando o projeto existir.

### 2.3 Estrutura de pastas planejada

```
quadtree/
  CLAUDE.md                    este arquivo
  Quadtree.slnx
  Quadtree/                    código do app
    App.xaml(.cs)              recursos globais, início do app
    MainWindow.xaml(.cs)       janela, barra de cima, atalhos
    Models/                    BoardItem, Board, Camera, AppState, Palette
    ViewModels/                MainViewModel, BoardItemViewModel, LibraryViewModel
    Views/                     quadro (BoardView), itens, bandeja, menus, lateral, editor de notas
    Services/                  StorageService, ThemeService, ExportService, MediaService
    Rendering/                 câmera, quadtree, fundos, animações, formas
    Behaviors/                 comportamentos anexados (edição, brilho do vidro)
    Themes/                    Light.xaml, Dark.xaml
    Assets/                    Fonts/, texturas, ícone
  Scripts/publicar.bat         publica e copia o .exe
  tcc/                         documentos do TCC (fora do git)
```

### 2.4 Onde está cada coisa

| O quê | Onde |
|---|---|
| Página do projeto | Notion → **quadtree** (https://app.notion.com/p/41e6955d74e580a09f50f8ce74f2db64) |
| Roadmap com caixinhas | Notion → quadtree → **Roadmap** (https://app.notion.com/p/4206955d74e58022be15c65417d381d5) |
| Tarefas da equipe | Notion → quadtree → Gestão de trabalho → **Base de dados de construção** |
| Requisitos | Notion → **Requisitos funcionais do sistema** e **Requisitos não funcionais do sistema**; PDF "RF e RNF" na pasta `tcc/` |
| Regras do Git | Notion → quadtree → **regras do github** |
| Estudos de C# do Vitor | Notion → quadtree → **C#** (cobre do básico até POO, interfaces, enums, arquivos e exceções; WPF e MVVM ainda não) |
| Rascunhos de documentos | Claude Docs |
| Doc da tarefa atual (lista para riscar + contexto) | Claude Docs (seção 1.7) |

---

## 3. Categorias de importância

### 3.1 O que cada categoria significa

| Categoria | Significado | Regra |
|---|---|---|
| **1** | Necessário para o app rodar | Vem primeiro. Sem ela não existe app. |
| **2** | Novas funções que o app ganha | Só depois da Categoria 1 pronta e testada. |
| **3** | Design e extras | Só depois da Categoria 2. Se o prazo apertar, é aqui que se corta. |

- Ao explicar uma tarefa, diga a categoria dela.
- Não comece uma tarefa de categoria maior enquanto a menor da mesma área não estiver pronta.
- Se o Vitor quiser adiantar algo, avise as dependências; a decisão é dele.

### 3.2 Diferenças entre este arquivo e o PDF de requisitos

O PDF de requisitos (82 RF + 15 RNF) fica como está. Este arquivo mudou em relação a ele:

- **Entraram na Categoria 1 (não estão no PDF):** título grande do quadro, editor de notas (abrir, Ler/Editar, salvar no `.md`) e Ajustes.
- **Foram para a Categoria 3 (no PDF estão na 2):** modelos de quadro além do Pontilhado, agrupar, alinhar e distribuir, seleção com o botão direito, imagens e vídeos, anexos no cofre.
- **Entraram na Categoria 3 (não estão no PDF):** Designs (mapas prontos), links entre notas (`[[Nota]]`, "Mencionado em"), modelo Cortiça, quadro de exemplo, página Cofre na lateral.
- **Salvamento** (Categoria 2 no PDF) é feito antes da v0.1, porque o editor de notas e os Ajustes dependem dele.

---

## 4. Padrões de código

- **MVVM:** Model (dados, como vão para o arquivo) · ViewModel (estado e lógica, nada de tela) · View (XAML e código só de tela) · Service (arquivos, tema, exportação, mídia).
- As telas leem do ViewModel por **binding** e chamam **comandos** (`[RelayCommand]`). O ViewModel nunca acessa controles da tela. Código que é só de tela (mouse, arraste, câmera) pode ficar na View, alterando o ViewModel.
- **Uma classe por arquivo**, nome do arquivo igual ao da classe.
- Comentário no topo de cada classe, em português, dizendo para que ela serve ("Aqui usamos a classe X para..."). Ajuda a explicar o código na banca.
- **Toda gravação de arquivo passa pelo `StorageService`** e é atômica (grava num `.tmp`, depois troca).
- **Toda mudança no quadro chama o Checkpoint** (foto para o desfazer) e agenda o salvamento automático, a partir da Etapa 8.
- Erros de arquivo vão para `erros.log` e **nunca impedem o app de fechar**.
- Interface: **nunca fundo amarelo ou dourado** (post-it amarelo pode, é cor de conteúdo).
- Nomes em português ou inglês: **pendente** (decidir na Etapa 4). Sugestão: classes e métodos em inglês, propriedades salvas no JSON em português (viram as chaves do arquivo).

---

## 5. Especificação do app (como tudo deve ficar)

Esta é a referência de visual e de comportamento. Ao guiar uma tarefa, use a parte correspondente. A coluna "Etapa" diz quando cada coisa é construída.

### 5.1 Cores da interface (tema claro e escuro)

Cores com transparência no formato `#AARRGGBB`.

| Token | Claro | Escuro | Uso |
|---|---|---|---|
| `Bg` | `#EEF0F4` | `#0D0E12` | fundo da janela |
| `Blob1` | `#FFDDE8` | `#3A1C36` | mancha 640×520 no canto superior esquerdo |
| `Blob2` | `#D4E4FF` | `#162852` | mancha 760×620 no canto superior direito |
| `Blob3` | `#D7F4E7` | `#0E3226` | mancha 700×520 embaixo, a 35% da largura |
| `Ink` | `#0F1115` | `#F2F3F7` | texto principal |
| `Ink2` | `#4F5563` | `#B3B8C6` | texto secundário, ícones |
| `Ink3` | `#646A79` | `#959AAA` | rótulos, placeholders |
| `Glass` | `#C7E4ECFA` | `#8C1E202A` | painéis de vidro |
| `Glass2` | `#E8E9EFFB` | `#E0282A36` | vidro mais denso |
| `MenuGlass` | `#F7EEF3FC` | `#F2282A36` | menus e bandejas por cima do quadro (quase opacos) |
| `Rim` | `#F2FFFFFF` | `#6BFFFFFF` | brilho da borda (canto superior esquerdo) |
| `Rim2` | `#80FFFFFF` | `#1AFFFFFF` | brilho da borda (canto inferior direito) |
| `Fill` | `#1F767C91` | `#14FFFFFF` | fundo de botões no hover, campos |
| `Fill2` | `#33767C91` | `#26FFFFFF` | hover de menu, item ativo da lateral |
| `Sep` | `#173C425A` | `#14FFFFFF` | separadores |
| `Accent` | `#0A84FF` | `#0A84FF` | destaque (azul) |
| `Danger` | `#E5312B` | `#FF5A52` | "Excluir" |
| `Success` | `#34C759` | `#34C759` | ponto do "Salvo" |
| `Canvas` | `#FFFFFF` | `#0F1013` | superfície do quadro Liso |
| `CanvasDot` | `#E6E8ED` | `#26272C` | grade do quadro Liso |
| `CardBg` | `#FFFFFF` | `#26272B` | fundo da caixa de texto |
| `CardBorder` | `#D9DCE3` | `#45464D` | borda cinza da caixa de texto |
| `CardText` | `#1F2229` | `#E6E7EB` | texto da caixa de texto |
| `GlowAlpha` | 0,34 | 0,16 | força do brilho interno do vidro |

- Fundo da janela: `Bg` com as três manchas em gradiente radial que somem a 62% do raio.
- Sombra do vidro: claro `0 14 36` `#1A1E243C` + `0 1 3` `#0F1E243C`; escuro `0 16 40` `#6B000000` + `0 1 3` `#4D000000`.
- **Tema:** na primeira abertura segue o Windows; depois vale a escolha do botão de tema (salva no `estado.json`). A troca anima as cores em 0,3 s. (Etapa 15; até lá, só o tema claro.)

### 5.2 Cores dos itens

Cada cor tem o **papel** (fundo) e a **tinta** (detalhes, texto solto, rodapé).

| Chave | Nome | Papel | Tinta |
|---|---|---|---|
| amarelo | Amarelo | `#FFE27A` | `#8A6400` |
| laranja | Laranja | `#FFBE8C` | `#A4470E` |
| rosa | Rosa | `#FFB1C6` | `#A61F4C` |
| roxo | Roxo | `#D2BBFF` | `#5A2DB5` |
| azul | Azul | `#A6D3FF` | `#1B5DA8` |
| menta | Menta | `#A2EDD8` | `#0B7658` |
| verde | Verde | `#C6EC9E` | `#3B770F` |
| branco | Branco | `#FBFAF5` | `#2A2E39` |
| vermelho | Vermelho | `#FF9E99` | `#B3261E` |
| pessego | Pêssego | `#FFD3B6` | `#A35A2A` |
| areia | Areia | `#F3DFB8` | `#7A5A1E` |
| lima | Lima | `#E2F27A` | `#6B7A00` |
| turquesa | Turquesa | `#8FE3EF` | `#0A6E7C` |
| indigo | Índigo | `#B8C3FF` | `#2F3FA8` |
| lilas | Lilás | `#F2C4F0` | `#8E2C87` |
| cinza | Cinza | `#DADDE3` | `#4B5263` |
| coral | Coral | `#FFB59E` | `#B23C17` |
| framboesa | Framboesa | `#F7A8C8` | `#9C1452` |
| lavanda | Lavanda | `#DCD3FF` | `#4F3E99` |
| ceu | Céu | `#CFEAFF` | `#1D6FB8` |
| petroleo | Petróleo | `#A9D8D2` | `#1F5E58` |
| salvia | Sálvia | `#CFE3CF` | `#3E6B45` |
| oliva | Oliva | `#D5DDA8` | `#55611D` |
| chocolate | Chocolate | `#E3C7B0` | `#6B3F22` |

- **10 cores fortes** (só na paleta completa): vermelho `#FF0000`, laranja `#FF6D00`, amarelo `#FFD600`, verde `#00A83E`, azul `#0050FF`, roxo `#7B00E0`, rosa `#FF0080`, marrom `#5D3200`, preto `#000000`, branco puro `#FFFFFF`. Nelas a tinta sai do contraste.
- **Em cor escura, o texto daquele item fica branco** (calcular a luminância da cor).
- **Cores dos alfinetes e fitas** (pela posição `id % 5`): `#FF453A`, `#0A84FF`, `#30D158`, `#FF9F0A`, `#BF5AF2`.
- **Cores de linha:** 18 cores, incluindo juta; padrão `#8A8F98`.
- **Menu de cor:** três linhas de 8 bolinhas (as 24 cores), "Últimas cores utilizadas" (as 8 últimas, salvas no `estado.json`) e o botão "Paleta de cores", que abre todas (24 + 10 fortes).

### 5.3 Fontes

- **Inter Tight** (interface): pesos 400, 500, 600, 700, 800. **Nunito Sans** (conteúdo do quadro): 700, 800, 900. Gratuitas (licença OFL), embutidas no app. Decisão de 22/11/2026: no lugar de Inter e Nunito, valem **Inter Tight** e **Nunito Sans** (nomes de família no XAML: `Inter Tight` e `Nunito Sans`). Os arquivos são variáveis; conferir na Etapa 4 se os pesos 800 e 900 saem certos, e se o espaçamento de −0,04em do título não fica apertado demais na Inter Tight (ela já é mais apertada).
- **Caligrafias** (título, texto solto, formas e tabelas): Inter Tight + Caveat, Patrick Hand, Permanent Marker, Amatic SC, Dancing Script, Pacifico, Lobster, Bebas Neue, Abril Fatface, Playfair Display, DM Serif Display, Fredoka e Space Mono (14 no total, do Google Fonts, embutidas). No menu, cada nome aparece na própria letra; passar o mouse já mostra o item com ela; fechar sem escolher volta à anterior.

| Elemento | Fonte | Tamanho | Peso | Detalhes |
|---|---|---|---|---|
| Título grande do quadro | Inter Tight | 42 | 800 | espaçamento −0,04em |
| Subtítulo do quadro | Inter Tight | 15 | 500 | `Ink2`, "Editado agora" (sem contagem de itens) |
| Linha da lateral | Inter Tight | 15 | 500 | |
| Rótulo de seção da lateral | Inter Tight | 12,5 | 600 | `Ink3` |
| Linhas do menu | Inter Tight | 15 | 500 | cabeçalho 12,5 / 600 / `Ink3` |
| Status, dica, balões | Inter Tight | 13 | 500–600 | `Ink2` |
| Texto do post-it | Nunito Sans | 19 | 900 | MAIÚSCULAS, entrelinha 1,26, cor `#1C1812` a 88% |
| Rodapé do post-it | Nunito Sans | 10 | 800 | espaçamento 0,12em, tinta a 85% |
| Título do pautado | Nunito Sans | 13 | 900 | MAIÚSCULAS, cor da tinta |
| Itens do pautado | Nunito Sans | 15 | 700 | entrelinha 27 |
| Título da nota | Nunito Sans | 18 | 900 | entrelinha 22 |
| Corpo da nota | Nunito Sans | 14 | 700 | entrelinha 28, cor `#33374A` |
| Título do bloco | Inter Tight | 16,5 | 700 | espaçamento −0,02em |
| Corpo do bloco | Inter Tight | 14 | 400 | entrelinha 1,7 |
| Texto solto | Nunito Sans | 50 | 900 | cor da tinta |
| Título (item) | conforme a caligrafia | 64 | — | tamanho escolhido de 8 a 400 px |

### 5.4 Formas, espaços e movimento

- Margem da janela e espaço entre lateral e quadro: **14**.
- Cantos: lateral 32, menu 24, bandeja 34, bloco 24, caixa de texto 10, linhas da lateral 10, linhas do menu 14; cápsulas e pílulas totalmente redondas.
- Ícones: traço de 1,9, cantos arredondados, 19×19, sem preenchimento.

| Movimento | Duração | Curva | Uso |
|---|---|---|---|
| Mola de toque | 0,5 s | cubic-bezier(.25, 1.7, .45, 1) | botão afunda a 93% ao clicar e volta |
| Mola de painel | 0,55 s | cubic-bezier(.3, 1.4, .5, 1) | abrir a bandeja |
| Pop do menu | 0,4 s | cubic-bezier(.3, 1.45, .5, 1) | menu cresce de 86% a 100% a partir de onde abriu |
| Título recolhendo | 0,5 s | cubic-bezier(.3, 1, .4, 1) | altura, opacidade e deslocamento |
| Item novo | — | mola | surge com fade, de 85% a 100% |

No WPF, as curvas que "passam do ponto" se fazem com `BackEase` (EaseOut, amplitude 0,4–0,6) ou com uma curva cubic-bezier própria.

### 5.5 Vidro (Etapa 15)

Lateral, cápsulas da barra de cima, bandeja, menus, status e balões são **painéis de vidro** com quatro camadas:

1. **Fundo:** cor `Glass`/`Glass2` sobre o que está atrás, desfocado (desfoque 26, saturação 190%). Plano B, se pesar: fundo quase opaco sem desfoque.
2. **Sombra:** a sombra do vidro (5.1).
3. **Borda de luz (1,3 px):** gradiente fixo a 150° (`Rim` no canto superior esquerdo → transparente em 28% → transparente em 66% → `Rim2` no inferior direito) + brilho radial de raio 190 px centrado no mouse, com opacidade `0,2 + 0,8 × proximidade`.
4. **Brilho interno:** gradiente radial branco de raio 300 px no mouse, opacidade `GlowAlpha × proximidade`.

- **Proximidade** = `max(0, 1 − distância/170)`, com a distância do mouse até a borda do painel (0 quando está dentro). A borda brilha antes do mouse encostar.
- Atualizar no máximo uma vez por quadro; pausar enquanto a câmera se move.
- A sombra dos painéis nunca recebe cliques.

### 5.6 Janela e layout

```
┌──────────────────────────────────────────────────────────────────┐
│ ┌──────────┐  [⌃ título]                       […]  [– □ ✕]       │
│ │ LATERAL  │  Meu quadro                                          │
│ │ (vidro)  │  Editado agora                                       │
│ │          │  ┌ moldura ───────────────────────────────────────┐  │
│ │          │  │ [dica ou nome do quadro]                       │  │
│ │          │  │              QUADRO                            │  │
│ │          │  │ [zoom %]        [ Bandeja ]          [● Salvo] │  │
│ └──────────┘  └────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────────────────┘
```

- Tamanho inicial 1440×920; mínimo 1100×720. Janela sem a moldura do Windows (barra própria).
- **Barra de cima:** só a seta do título · "…" · minimizar, maximizar, fechar, em cápsulas de 42 de altura (botões de 34, ícones de 15), sem sombra. **Nunca se esconde.** Sem desfazer/refazer na tela (ficam no "…" e no Ctrl+Z). O ✕ fecha o app sempre.
  - **Seta do título:** mostra/oculta o título grande; gira 180° quando ele está oculto.
  - **"…":** desfazer, refazer, ajustar à tela, buscar no quadro, grade, cenas, apresentar, tela cheia, somente visualização, exportar, abrir a pasta do cofre.
  - Botões que abrem algo fecham no segundo clique.
- **Título grande** (Categoria 1): "Meu quadro" (42/800) e "Editado agora" embaixo; dois cliques editam. Ocultar recolhe com animação (altura e opacidade → 0, sobe 14 px) e o quadro cresce. **Com o título oculto, o nome do quadro aparece numa pílula no canto superior esquerdo do quadro.** Com o título à mostra, esse canto mostra a **dica** "Botão direito para adicionar · 2 cliques para editar" (Categoria 3).
- **Status** (canto inferior direito, a 30/32 px): pílula com ponto verde e "Salvando…" / "Salvo" (sem contagem de itens).
- **Balão de zoom** (canto inferior esquerdo): a porcentagem aparece quando o zoom muda e some 1,2 s depois.
- **Bandeja:** botão "Bandeja" sempre à mostra, no centro de baixo (seção 5.10).
- **Lateral** (292 de largura, vidro, raio 32), no estilo de lista limpa (linhas de 34, raio 10, hover `Fill`):
  1. topo: recolher a lateral, voltar e avançar (histórico de quadros);
  2. ações: Novo quadro (Ctrl+N) · Designs · Nova pasta · Procurar (Ctrl+K) · Apagados recentemente (com contador);
  3. pastas no topo, com os quadros dentro; depois os quadros soltos, pelo último aberto (até 8 e "Ver todos");
  4. o quadro aberto fica numa pílula `Fill2`; ao passar o mouse: fixar, importante (estrela laranja) e "…" (abrir, renomear, duplicar, fixar, importante, excluir); botão direito abre o mesmo menu; dois cliques ou F2 renomeiam;
  5. a setinha ao lado de cada quadro abre os itens dele; clicar num item leva a câmera até ele;
  6. seções **Fixados** e **Importantes** (só quando houver algo marcado);
  7. rodapé: botão de tema, **Cofre** (página com a árvore da pasta do cofre; Categoria 3) e **Ajustes**.
  - Escondida, a lateral some por inteiro; um botão no canto esquerdo da barra de cima a traz de volta.
- **Ajustes** (Categoria 1): seguir o tema do Windows, faíscas ao clicar, contador de FPS, abrir a pasta do cofre (cada opção entra quando o recurso dela existir).

### 5.7 Quadro, câmera e modelos

- **Quadro infinito:** coordenadas do mundo em `double`, também negativas. Uma **câmera** = ponto do mundo no centro da tela + zoom. Nada de `ScrollViewer`.
  - `tela = (mundo − centro) × zoom + metade da tela`; `mundo = centro + (tela − metade da tela) / zoom`.
- **Zoom de 10% a 400%**, suave e centrado no cursor: rodinha (com ou sem Ctrl) e pinça do touchpad. Ctrl + / Ctrl − a partir do centro (×1,25); Ctrl 0 volta a 100%; Ctrl+1 ajusta à tela.
- **Mover a câmera:** arrastar no vazio com o botão esquerdo, botão do meio, Espaço + arrastar, Shift + rodinha, rolagem horizontal do touchpad. Ao soltar, o quadro desliza um pouco e para (inércia, Categoria 3).
- **Ajustar:** enquadra todos os itens com margem de 80 px (no máximo 100%).
- **"Ir para o conteúdo":** pílula no topo central quando nenhum item está na tela.
- Ao abrir, a câmera volta para onde estava; na primeira vez, "Ajustar". Quadro vazio abre centrado em (0, 0). Redimensionar a janela mantém o centro.
- **Grade opcional** (menu "…"): quadrados a cada 32 px que acompanham a câmera.

**Modelos do quadro** (cada um com moldura própria):

| Modelo | Categoria | Moldura | Superfície |
|---|---|---|---|
| **Pontilhado (padrão)** | 2 | degradê `#F6F6F2 → #DCDCD4 → #EDEDE7 → #CFCFC6` | `#FBFBF8` com pontos `#C2C2B8` de raio 1,3 a cada 26 px |
| Liso | 3 | 10 px, degradê suave azulado (clara ou grafite conforme o tema), raio 26 | `Canvas` (branca no claro, preta no escuro) com grade `CanvasDot` a cada 32 px |
| Cortiça | 3 | madeira clara `#EAD1A6 → #D3AD75 → #E3C597 → #C0965C` com veios | textura de cortiça (imagem 384×384 que se repete sem emenda) |
| Branco | 3 | alumínio `#F5F6F8 → #D2D6DD → #EEF0F3 → #BBC1CA` | `#F9FAFB` com reflexo diagonal |
| Escuro | 3 | grafite | `#0F1013`, sem grade, em qualquer tema |
| Lousa | 3 | madeira escura `#9A6C43 → #6B4628 → #8A623B → #54361D` | verde `#2C4838` com manchas de giz; o texto solto usa a cor do papel (giz) |

- A escolha do modelo fica na seção **"Quadro"**, a primeira da bandeja.
- **Sombras dos itens no tom do fundo** (Categoria 3): marrom na cortiça; cinza-azulado suave nos claros; preta nos escuros.

### 5.8 Itens do quadro

**Regras comuns**
- **Nada inclinado:** todos os itens ficam retos. Passar o mouse ou arrastar não inclina nem cresce.
- **Selecionado:** contorno de 2,5 px na cor `Accent`, afastado 7 px do item, cantos de raio 6.
- **Arrastar** qualquer item move ele (ou todos os selecionados) e o traz para a frente. Não precisa selecionar antes.
- **Editando:** o texto vira campo editável com a mesma fonte e tamanho, com anel de 2 px `Accent`.
- **Fora da busca (Ctrl+F):** opacidade 16%.
- **Item bloqueado** não se move; arrastar nele move a câmera.
- **2 cliques num item com texto** entram em edição. **Enter sai** da edição; **Shift+Enter quebra a linha**; **Esc termina**; **Tab alterna entre título e texto** (nota, bloco, pautado; nos itens sem título, Tab termina).

| Item | Etapa | Como é |
|---|---|---|
| **Nota** | 5 | Folha branca lisa (sem pautas, margem, furos ou orelha), 236 de largura e 300 de altura mínima. Título Nunito Sans 18/900 e corpo Nunito Sans 14/700. Nasce já escrevendo o título. O texto fica num arquivo `.md` (Etapa 6); mudar o título renomeia o arquivo. **Espiral** de caderno opcional (botão direito → "Pôr a espiral"/"Tirar a espiral"; Categoria 3). |
| **Bloco** | 5 | Cartão de vidro com **cor forte (75% da cor)** e **texto preto `#000`**, raio 24, 290 de largura. Título Inter Tight 16,5/700 (vazio mostra "Título" clarinho) e parágrafo Inter Tight 14. Sem bolinha antes do título. |
| **Post-it** | 9 (visual completo na 15) | 172×172, papel liso na cor. Texto Nunito Sans 19/900 em MAIÚSCULAS, centralizado. Estilos: **alfinete** (bolinha de 20 px no topo), **fita** (86×27, listras diagonais, pontas em zigue-zague), **solto** e **pautado** (linhas na cor da tinta a 28%, a cada 27 px a partir de 34; título + lista à esquerda). Visual completo: faixa adesiva nos 26 px de cima, canto levantado (triângulo de 36 px), sombra dupla nos cantos de baixo, rodapé com a data ("28 OUT") e o número ("#01": posição entre os post-its deste quadro). Novo post-it usa a última cor e estilo. |
| **Texto solto** | 9 | Só o texto, Nunito Sans 50/900 na cor da tinta. As alças mudam o tamanho da letra. Edição numa linha. |
| **Título** | 9 | Texto solto de 64 px que já nasce escrevendo. Botão direito → "Tamanho em pixels" (8 a 400, muda ao digitar) e "Caligrafia". |
| **Caixa de texto** | 9 | Cartão de raio 10, borda de 2 px na cor (cinza `CardBorder` quando branco), fundo `CardBg` com 10% da cor. |
| **Forma** | 9 | Escolhida numa biblioteca com busca e 5 categorias (abaixo). Desenhada numa grade 100×100 e esticada para o tamanho do item. Aceita texto dentro. Barra "Transparência do fundo" de 0 a 100% (Categoria 3). |
| **Tabela** | 9 | Linhas e colunas sem limite. Com o mouse na borda direita (coluna) ou de baixo (linha) aparece um +: clicar põe uma; arrastar para fora põe e para dentro tira. Tab passa de célula; na última, cria outra linha. |
| **Linha / seta** | 9 | Ver 5.9. |
| **Imagem / vídeo** | 15 | Arrastar do Windows ou Ctrl+V (inclusive print). O arquivo é copiado para o cofre. Vídeo toca no quadro. |
| **Arquivo** | 15 | Cartão com o tipo e o nome; PDF mostra a 1ª página. Dois cliques abrem no programa padrão. |
| **Link** | 15 | Cartão com título, site e imagem da página (lidos uma vez e guardados no cofre). Dois cliques abrem no navegador. Sem internet, mostra só o endereço. |
| **Desenho à mão** | 15 | Caneta, lápis, marcador, borracha e laço, com cores e 3 espessuras, numa paleta flutuante ("Pronto" volta à seleção). |

**Biblioteca de formas (43)**
- Básicas: retângulo, retângulo arredondado, círculo, triângulo, triângulo retângulo, losango, pentágono, hexágono, octógono, paralelogramo, trapézio, balão de fala.
- Setas: para a direita, para a esquerda, para cima, para baixo, dupla, divisa, seta curva.
- Símbolos: pincelada, estrela, coração, mais, X, visto, raio, interrogação, alerta.
- Objetos: casa, livro, lâmpada, documento, pasta, mensagem, bandeira.
- Natureza: sol, lua, nuvem, gota, folha, flor, árvore, montanha.

**Anexar um item a outro** (Categoria 3): arrastar um item até 40 px da borda de cima ou de baixo de outro (nota, post-it, bloco ou caixa de texto) mostra "Anexar" com um + numa bolinha. Soltar prende o item **dentro** do principal, com margem de 14 px; o principal cresce para caber; vários por lado, empilhados. Mover o principal leva os anexos; arrastar o anexo para fora solta e ele volta ao tamanho de antes. Ctrl não anexa; linhas, desenhos e texto solto não anexam.

### 5.9 Linhas e setas (Etapa 9)

- Ligam **qualquer item, inclusive outra linha**: cada linha tem um **ponto fixo no meio** (aparece ao passar o mouse) onde outra seta pode chegar ou de onde pode sair. As presas no meio acompanham quando a linha muda; ligações em círculo são recusadas.
- **Nascem sem seta.** Direção pelo botão direito: sem seta · uma · duas · inverter.
- Traçado: **reta**, **curva** ou **ângulo**. A linha selecionada mostra uma **alça azul no meio**; arrastá-la muda a dobra (trocar o traçado volta à dobra automática).
- **Uma linha ligada nunca se solta** ao mexer nos itens. Soltar a ponta no vazio volta ao item; soltar em outro item troca a ligação.
- **Apagar um item apaga as linhas ligadas a ele** (Ctrl+Z traz tudo de volta).
- Botão direito na linha: **cor** (18 cores, padrão `#8A8F98`), **traço** sólido ou **barbante** (corda torcida na cor escolhida), direção e traçado.
- **Barbante:** clicar na linha "belisca" a corda: o meio balança e vai parando (~1,6 s).
- Formas de criar: elementos "Linha" e "Seta" da bandeja, ou **segurar o botão direito num item e arrastar até outro** (soltar no vazio não cria nada).

### 5.10 Bandeja e menus (Etapa 10)

- **Bandeja:** o botão "Bandeja" abre um painel de vidro (`MenuGlass`, até 620 de largura, raio 34) que surge de baixo com a mola de painel.
  - Conteúdo: **"Quadro"** (modelos) primeiro; depois os elementos: Nota, Bloco, Post-it, Texto, Título, Caixa de texto, Forma (abre a biblioteca de formas), Tabela, Linha, Seta (e, na Categoria 3: Desenhar, Imagem, Arquivo, Link).
  - **Clicar** num elemento cria no centro da área visível, com um pequeno desvio. **Arrastar** até o quadro cria onde soltar.
- **Botão direito no vazio:** abre a bandeja junto ao cursor; o item nasce no ponto clicado. Um segundo clique direito fecha.
- **Dois cliques no vazio** (esquerdo ou direito): cria outro item igual ao último criado (tipo, cor, estilo, tamanho), no ponto clicado. Sem nada criado ainda: uma nota.
- **Menus** (próprios, não o menu padrão do Windows): vidro `MenuGlass`, largura 266, raio 24, padding 6; abrem onde o mouse clicou com o pop; **nunca saem da janela** (quando não cabem na altura, abrem em duas colunas); fecham ao clicar fora, ao escolher ou com Esc. Grupos separados por uma faixa de 7 px `Sep`; linhas de 42 de altura, raio 14; bolinhas de cor de 24 px; chips de 30 de altura.
- **Menu do item:** cor (5.2) · estilo (só post-it: Alfinete, Fita, Solto, Pautado) · editar · duplicar · bloquear · trazer para frente / enviar para trás · "Mais opções" (topo, fundo; agrupar, alinhar, distribuir, desagrupar na Categoria 3) · **Excluir** em `Danger`. Linhas, formas e tabelas têm opções próprias (5.8 e 5.9).
- **Seleção com o botão direito** (Categoria 3): segurar o botão direito no vazio e arrastar desenha a caixa de seleção; ao soltar, abre o menu da seleção: "Excluir N itens", Duplicar, Copiar, "Agrupar itens" (ou "Desagrupar itens") e Tirar a seleção. Um clique direito simples continua abrindo a bandeja.

### 5.11 Edição e atalhos

| Ação | Resultado | Etapa |
|---|---|---|
| Arrastar um item | move (e todos os selecionados); vem para a frente | 5 |
| Clicar no vazio | tira a seleção e fecha o menu | 5 |
| 2 cliques num item | edita o texto clicado | 5 |
| Delete | exclui o selecionado | 5 |
| Arrastar no vazio / botão do meio / Espaço + arrastar | move a câmera | 7 |
| Rodinha, Ctrl + rodinha, pinça | zoom no cursor | 7 |
| Ctrl + / Ctrl − / Ctrl 0 / Ctrl+1 | zoom no centro / 100% / ajustar | 7 |
| Ctrl+Z, Ctrl+Shift+Z, Ctrl+Y | desfazer e refazer, por foto do quadro | 8 |
| 8 alças no selecionado | redimensionar (Shift mantém a proporção) | 8 |
| Ctrl+C / X / V / D, Alt + arrastar | copiar, recortar, colar, duplicar (30 px abaixo e à direita), arrastar uma cópia | 8 |
| Ctrl+] / Ctrl+[ (com Shift: topo/fundo) | camadas | 8 |
| Ctrl+L | bloquear | 8 |
| Guias ao arrastar | bordas e centros encaixam a 6 px; linhas-guia cinza `#6E737C`; Ctrl desliga | 8 |
| Ctrl+N · F2 · Ctrl+K · Ctrl+F · Alt+← / Alt+→ | novo quadro, renomear, procurar, buscar no quadro, voltar/avançar | 11 |
| Ctrl+B / I / U | negrito, itálico, sublinhado | 12 |
| F11 · Esc | tela cheia · sai de menus, edição, apresentação | 13 |
| Ctrl+Shift+F | contador de FPS | 14 |
| Shift + clique, Shift + arrastar, Ctrl+A | seleção múltipla | 15 |
| Ctrl+G / Ctrl+Shift+G | agrupar / desagrupar | 15 |

### 5.12 Texto formatado e listas (Etapa 12)

- O texto dos itens fica guardado como **Markdown simples**: `**negrito**`, `*itálico*`, `~~riscado~~`, `` `código` ``, `<u>sublinhado</u>`, `<span style="color:#hex">`, `<mark style="background:#hex">`; listas com `-`, `*` ou `1.`.
- Fora da edição, aparece formatado. **Editando, nenhuma marca aparece** (campo já formatado).
- Ao selecionar uma palavra ou frase, surge uma **barra de formatação**: cor do texto, cor do fundo, B, I, U, riscado, código, marca-texto, limpar.
- **Listas em todos os itens com texto:** "- " no começo da linha vira "•" (no arquivo continua "- "); "5. " começa uma lista numerada. Numa linha de lista, **Shift+Enter abre o próximo item** (renumerando os de baixo); **Shift+Enter duas vezes** tira a marca; Backspace logo depois da marca a apaga.

### 5.13 Quadros, notas e recursos de navegação

- **Vários quadros** (Etapa 11): criar, renomear, duplicar, excluir. O quadro aberto é salvo antes de trocar. Sem nenhum quadro: "Nenhum quadro" com o botão "Criar novo quadro".
- **Pastas:** "Nova pasta"; arrastar quadros para uma pasta; arrastar entre quadros da pasta muda a ordem (linha azul); soltar num quadro solto tira da pasta. Botão direito na pasta: novo quadro aqui, renomear, mostrar no Explorador, excluir (quadros vão para a lixeira).
- **Galeria:** grade com a miniatura de cada quadro, ordem por data ou nome; também para Fixados, Importantes e Apagados recentemente.
- **Lixeira:** apagar um quadro manda ele **e as notas dele** para a lixeira **por 3 dias**; dá para restaurar ou apagar de vez. Apagar uma nota sozinha apaga o `.md` de vez (Ctrl+Z o recria na mesma sessão).
- **Procurar** (Ctrl+K): caixa no centro que busca em nomes de quadros, notas e textos dos itens; Enter abre e leva a câmera até o item.
- **Buscar no quadro** (Ctrl+F): destaca os resultados e apaga o resto; Enter e Shift+Enter vão ao próximo e ao anterior.
- **Editor de notas** (Etapa 6, Categoria 1): painel ao lado do quadro, aberto pelo botão direito na nota → "Abrir no editor". Modo **Editar** (texto puro) e modo **Ler** (Markdown desenhado: títulos, listas, negrito). Salva no `.md`. Na Categoria 3: links `[[Nota]]` com autocompletar, Ctrl+clique segue o link, rodapé "Mencionado em" e links atualizados ao renomear a nota.
- **Cenas** (Etapa 13): salvar a vista atual com um nome e ir até ela com a câmera animada. **Apresentar:** tela cheia passando pelas cenas com → / ← ou Espaço; Esc sai.
- **Tela cheia** (F11): cobre a barra de tarefas (fica por cima só enquanto o app está ativo); o quadro vai de borda a borda, com a moldura e os cantos arredondados; a lateral continua (fixa ou escondida) e a barra de cima continua à mostra.
- **Somente visualização** ("…" → Somente visualização; salvo no quadro): arrastar só move a câmera; 2 cliques só abrem links, arquivos e vídeos; sem menus, bandeja, colar, soltar arquivos, repetir item, desfazer e atalhos de edição. O status mostra "somente visualização".
- **Exportar** (Etapa 15): "…" → Exportar abre uma mini janela de vidro no centro com dois cartões, **Imagem (PNG)** e **PDF**; com seleção, chips "Quadro inteiro" / "Só a seleção". Enquadra tudo o que tem conteúdo numa página de no máximo 4:3 ou 3:4, com o fundo do quadro (sem a moldura). PNG em 4× (até 100 megapixels); PDF em 3× (até 32 megapixels), numa só imagem JPEG de qualidade 95.
- **Designs** (Etapa 15): "Designs" na lateral abre uma galeria com 14 mapas prontos, cada um com miniatura: Mapa pastel, Caderno de estudos, Teia orgânica, Teia de conceitos, Mapa mental radial, Espinha de peixe, Linha do tempo neon, Bolha dupla, Árvore na lousa, Fluxograma de decisão, Kanban, Matriz de Eisenhower, Ikigai e Mural de sonhos. "Visualizar design" (ou Espaço) mostra o design no quadro sem criar arquivo, com os botões "Adicionar quadro" e ✕; "Importar como novo quadro" (ou 2 cliques, ou Enter) cria o quadro e abre.
- **Tela inicial e tutorial** (Etapa 15): na primeira vez que o app abre (cofre novo), aparece um quadro de exemplo com a nota "Tela inicial", que ensina a criar, mover e editar itens e a usar a câmera e o zoom. O usuário pode apagá-la.
- **Balões de ajuda** (Etapa 15): com o mouse parado 3 s num botão, aparece uma frase do que ele faz e o atalho (apagado, em `Ink3`).
- **Faíscas** (Etapa 15): a cada clique, 8 a 12 tracinhos coloridos saem do ponteiro e somem em ~0,4 s (no máximo 3 explosões ao mesmo tempo; liga/desliga em Ajustes).
- **Ponteiro próprio** (Etapa 15): seta branca com contorno preto arredondado e sombra suave, desenhada na escala da tela; mãos, texto e redimensionar no mesmo estilo.

### 5.14 Dados: cofre e arquivos (Etapa 6)

- **Cofre:** uma pasta em **Documentos** (nome a decidir na Etapa 3) com **tudo** do app, visível no Explorador:
  - `Quadros\` — um arquivo JSON por quadro, com subpastas (as pastas do app);
  - `Notas\` — cada nota é um `.md` de verdade;
  - `Anexos\Imagens`, `Anexos\Vídeos`, `Anexos\Arquivos`, `Anexos\Prévias` (Categoria 3);
  - `Lixeira\` — apagados (somem depois de 3 dias);
  - `Sistema\` — `estado.json`, `Miniaturas\`, `Registros\erros.log`, `Temporários\`.
- **Salvamento automático** ~1 s depois da última mudança, com gravação atômica. O status mostra "Salvando…" e depois "Salvo".
- **`estado.json`:** quadro aberto, recentes, fixados, importantes, seções abertas da lateral, tela cheia, lateral aberta, tema, faíscas, última cor e estilo de post-it, últimas cores, molde do último item criado, ordem das pastas.
- **Formato do quadro** (extensão a decidir na Etapa 3):

```json
{
  "versao": 1,
  "titulo": "Meu quadro",
  "modelo": "pontilhado",
  "camera": { "x": 0, "y": 0, "zoom": 1 },
  "tituloOculto": false,
  "grade": false,
  "somenteLeitura": false,
  "cenas": [],
  "itens": [
    { "id": 1, "tipo": "nota", "cor": "branco", "x": 40, "y": 40, "z": 1,
      "largura": null, "altura": null, "titulo": "Ideias", "arquivo": "Notas\\Ideias.md" },
    { "id": 2, "tipo": "bloco", "cor": "azul", "x": 420, "y": 40, "z": 2,
      "titulo": "Tarefas", "texto": "- Revisar o quadro" }
  ]
}
```

- `tipo`: `nota` | `bloco` | `postit` | `texto` | `titulo` | `caixa` | `forma` | `tabela` | `linha` | `imagem` | `video` | `arquivo` | `link` | `desenho`.
- Outros campos que entram com as etapas: `fixacao` (alfinete | fita | nenhuma), `pautado`, `semEspiral`, `bloqueado`, `grupo`, `criado` (data), `estilo` (preenchimento, borda, espessura, opacidade, fonte, tamanho, corTexto, alinhamento), `forma`, `linha` (de/para com item e lado, ponta, tipo reta/curva/angulo, traco solido/barbante, dobraX/dobraY), `tabela` (células por linha), `tracos` (desenho), `url`/`site`/`imagem` (link), `anexadoA`/`anexoLado`.
- Caminhos dentro do JSON são **relativos ao cofre**.

---

## 6. Requisitos não funcionais que guiam o código

| Requisito | Meta | Etapa |
|---|---|---|
| Rodar no Windows 11 / funcionar offline | sem internet, dados só no PC (só a prévia de links usa internet) | 5 |
| Não perder dados | gravação atômica + salvamento automático | 6 |
| Arquivos legíveis | quadros em JSON, notas em `.md` | 6 |
| Registro de erros | `erros.log`, nunca impede fechar | 6 |
| Cofre visível | pastas abertas no Explorador | 6 |
| Código em MVVM | Model · ViewModel · View · Service | sempre |
| Abrir rápido | até 5 s | 14 |
| Fluidez | 60 fps com 500 itens, usando a placa de vídeo | 14 |
| Desenhar só o visível | quadtree + reaproveitar itens | 14 |
| Uso de memória | devolver memória só fora de uso (minimizado ou 15 s em segundo plano) | 14 |
| Executável único | um `.exe` | 14 |
| Atalhos de teclado | Ctrl+Z, Ctrl+C, Delete, F2, F11... | 14 |
| Nitidez | de 100% a 200% de escala | 15 |
| Respeitar as animações do Windows | desligadas no Windows = desligadas no app | 15 |

---

## 7. Roadmap e lista de tarefas

Ordem do mais simples (fazer o código rodar) até o polimento. Cada etapa tem a **lista de tarefas** com o responsável (`[x]` feito, `[ ]` falta), **o que precisa saber** para programar e o **pronto quando**. O TCC entra no meio, quando já tem material. Para manter a lista em dia, siga a seção 1.5.

---

### Etapa 1 — Preparação

**Tarefas**

*Ambiente*
- [x] Instalar o Visual Studio 2026 com a carga de desktop .NET (Vitor)
- [ ] Instalar o Visual Studio 2026 com a carga de desktop .NET (Sidney)
- [x] Conferir o .NET 10 instalado (Vitor)
- [ ] Conferir o .NET 10 instalado (Sidney)
- [ ] Instalar e configurar o Git (Vitor)
- [ ] Instalar e configurar o Git (Sidney)
- [ ] Clonar o repositório Quadtree (Sidney)
- [x] Baixar as fontes Inter Tight e Nunito Sans (Vitor) — estão na pasta `fontes/` do repositório (Sidney pode usar)

*Repositório*
- [x] Apagar a pasta Inicializacaodogit (Vitor)
- [x] Revisar o .gitignore (Vitor)
- [x] Decidir o nome da branch principal (Vitor) — é a `main`
- [ ] Criar a branch do Vitor (Vitor)
- [ ] Criar a branch do Sidney (Sidney)
- [ ] Combinar a rotina de pull, commit e pull request (Vitor)
- [ ] Proteger a branch principal no GitHub (Vitor)
- [ ] Fazer um commit de teste e um pull request (Vitor)
- [ ] Fazer um commit de teste e um pull request (Sidney)
- [ ] Enviar este CLAUDE.md para o GitHub (Vitor)

*Decisões*
- [ ] Passar este roadmap para a Base de dados de construção (Vitor)

*TCC*
- [ ] Revisar o capítulo 1: trocar "tamanho definido" por quadro infinito (Vitor)

**O que precisa saber:** `dotnet --version`; `git config`, `clone`, `switch -c`, `add`, `commit`, `push`, `pull`, pull request e conflito (página "regras do github"). Proteger a branch: GitHub → Settings → Branches → regra para `main` exigindo pull request.

**Pronto quando:** os dois fizeram um commit na própria branch e juntaram na `main` por pull request.

---

### Etapa 2 — Estudos e fundamentação

**Tarefas**

*Estudos de base*
- [ ] Estudar C# orientado a objetos (Vitor)
- [ ] Estudar C# orientado a objetos (Sidney)
- [ ] Estudar XAML e layout do WPF (Grid, Canvas, Border) (Vitor)
- [ ] Estudar XAML e layout do WPF (Grid, Canvas, Border) (Sidney)
- [ ] Estudar data binding, INotifyPropertyChanged e ObservableCollection (Vitor)
- [ ] Estudar data binding, INotifyPropertyChanged e ObservableCollection (Sidney)
- [ ] Estudar MVVM, ICommand e CommunityToolkit.Mvvm (Vitor)
- [ ] Estudar MVVM, ICommand e CommunityToolkit.Mvvm (Sidney)

*Estudos específicos*
- [ ] Estudar eventos de mouse e CaptureMouse (Vitor)
- [ ] Estudar RenderTransform e MatrixTransform (Vitor)
- [ ] Estudar eventos de teclado e InputBindings (Sidney)
- [ ] Estudar Styles, Triggers e ResourceDictionary (Sidney)
- [ ] Estudar System.Text.Json e leitura/escrita de arquivos (Sidney)
- [ ] Mini-app: arrastar um retângulo num Canvas (Vitor)
- [ ] Mini-app: botão que adiciona itens e salva em JSON (Sidney)

*TCC — Capítulo 2 (escrever enquanto estuda)*
- [ ] Seção: mapa mental (Vitor)
- [ ] Seção: ferramentas de quadro visual (Vitor)
- [ ] Seção: WPF e XAML (Vitor)
- [ ] Seção: padrão MVVM (Vitor)
- [ ] Seção: estrutura quadtree (Vitor)
- [ ] Seção: requisitos funcionais e não funcionais (Vitor)
- [ ] Seção: C# e .NET (Vitor)
- [ ] Seção: JSON e Markdown (Vitor)
- [ ] Seção: Git e GitHub (Vitor)
- [ ] Seção: Kanban e Notion (Vitor)

**Para que serve cada estudo no Quadtree**
- **POO:** cada item do quadro é um objeto; o quadro é uma lista de objetos.
- **Layout:** a janela é um `Grid` (lateral, barra, quadro); o quadro é um `Canvas`, onde cada item tem posição X/Y.
- **Binding + `INotifyPropertyChanged`:** mudar `X` no ViewModel move o item na tela sozinho.
- **`ObservableCollection`:** adicionar um item na lista faz ele aparecer no quadro.
- **`ICommand`/`[RelayCommand]`:** botões (Criar nota) chamam a lógica sem código na tela.
- **Mouse + `CaptureMouse`:** selecionar e arrastar itens; o "capture" garante que o arraste não se perde se o mouse sair do item.
- **`MatrixTransform`:** é a câmera (zoom e deslocamento do quadro inteiro) da Etapa 7.
- **Teclado/`InputBindings`:** Delete, Enter, Esc, Tab e os atalhos.
- **Styles/ResourceDictionary:** cores e fontes num lugar só; depois, tema claro/escuro.
- **JSON e arquivos:** salvar e abrir os quadros.

Ao guiar os estudos: diga o que estudar, para que serve no Quadtree e o que fazer (o conteúdo eles estudam por conta, a não ser que peçam explicação). No TCC, **não dizer que WPF, MVVM, JSON e POO foram vistos no curso** (só o básico de C# foi).

**Pronto quando:** cada um explica com as próprias palavras binding, comando e `ObservableCollection`, e os dois mini-apps funcionam.

---

### Etapa 3 — Modelagem

**Tarefas**

*Diagramas*
- [ ] Diagrama de casos de uso da Categoria 1 (Vitor)
- [ ] Diagrama de casos de uso geral (Vitor)
- [ ] Diagrama de classes (Vitor)
- [ ] Definir a extensão do arquivo e o nome do cofre (Vitor)
- [ ] Escrever o JSON de exemplo do quadro (Vitor)
- [ ] Desenhar o protótipo da primeira tela (Vitor)
- [ ] Desenhar o fluxo do salvamento automático (Vitor)

*TCC — Capítulo 3 (início)*
- [ ] 3.1 Método (gestão de trabalho e branches) (Vitor)
- [ ] 3.2 Requisitos (tabelas das 3 categorias, explicando as diferenças da seção 3.2) (Vitor)
- [ ] 3.3 Modelagem (diagramas, JSON, fluxo) (Vitor)

**O que precisa saber:** ator, caso de uso, include/extend; classe, atributo, método, herança e associação em UML (draw.io ou Astah). O diagrama de classes separado por camadas: `Board` e `BoardItem` (Model), `MainViewModel` e `BoardItemViewModel` (ViewModel), `StorageService` (Service). JSON de exemplo: seção 5.14. Protótipo: seções 5.6 e 5.8.

**Pronto quando:** cada caso de uso corresponde a um requisito e todo dado da primeira tela tem lugar numa classe.

---

### Etapa 4 — Esqueleto do projeto

**Tarefas**
- [ ] Criar o projeto WPF Quadtree (net10.0-windows10.0.19041.0) e a solução Quadtree.slnx na raiz (Vitor)
- [ ] Rodar o projeto vazio e fazer o pull request (Vitor)
- [ ] Baixar o projeto e rodar (Sidney)
- [ ] Criar as pastas Models, ViewModels, Views, Services, Themes, Assets (Vitor)
- [ ] Instalar o CommunityToolkit.Mvvm (Vitor)
- [ ] Criar o MainViewModel e ligar à janela (Vitor)
- [ ] Criar o Themes/Light.xaml com as cores (Sidney)
- [ ] Embutir as fontes Inter Tight e Nunito Sans (Sidney)
- [ ] Escrever os padrões de nomes e commits no README (Vitor)

**O que precisa saber**
- No `.csproj`: `OutputType` WinExe, `TargetFramework`, `UseWPF`, `Nullable`, `PackageReference` do CommunityToolkit.Mvvm.
- `DataContext`: o objeto de onde a tela tira os dados do binding.
- `ResourceDictionary` mesclado no `App.xaml` (`MergedDictionaries`); cores como `SolidColorBrush` com `x:Key`, usando os tokens da seção 5.1 (por enquanto só o claro). Usar `DynamicResource` nas telas, para o tema escuro funcionar depois.
- Fontes embutidas: `.ttf` com Build Action **Resource** e `FontFamily="pack://application:,,,/Assets/Fonts/#Inter Tight"`.

**Pronto quando:** F5 abre a janela nos dois PCs e um texto aparece por binding, em Inter Tight.

---

### Etapa 5 — Categoria 1: o app rodando

**Tarefas**

*Base dos itens*
- [ ] Criar a janela com o quadro (Vitor)
- [ ] Criar as classes BoardItem e Board (Vitor)
- [ ] Criar o BoardItemViewModel (Vitor)
- [ ] Criar a lista de itens no MainViewModel (Vitor)
- [ ] Mostrar os itens no Canvas (Vitor)

*Nota e bloco*
- [ ] Fazer o visual da nota (Sidney)
- [ ] Criar o botão e o comando de criar nota (Sidney)
- [ ] Fazer o visual do bloco (Sidney)
- [ ] Criar o botão e o comando de criar bloco (Sidney)

*Interação*
- [ ] Selecionar item com um clique (Vitor)
- [ ] Tirar a seleção ao clicar no vazio (Vitor)
- [ ] Arrastar item e trazer para a frente (Vitor)
- [ ] Editar texto com dois cliques (Sidney)
- [ ] Enter, Shift+Enter, Esc e Tab na edição (Sidney)
- [ ] Excluir item com Delete (Sidney)

*Título do quadro*
- [ ] Título grande acima do quadro (Vitor)
- [ ] Editar o título com dois cliques (Vitor)
- [ ] Botão de ocultar e mostrar o título (Vitor)
- [ ] Pílula com o nome do quadro quando o título está oculto (Vitor)

*Fechamento*
- [ ] Testar no Windows 11 e sem internet (Vitor)
- [ ] Testar no Windows 11 e sem internet (Sidney)

**O que precisa saber**
- **Mostrar itens num `Canvas`:** `ItemsControl` com `ItemsSource` ligado à `ObservableCollection`, `ItemsPanel` = `Canvas`, `ItemContainerStyle` ligando `Canvas.Left`, `Canvas.Top` e `Panel.ZIndex` a `X`, `Y` e `Z`. Um `DataTemplate` por tipo, escolhido com `DataType` ou com um `DataTemplateSelector`.
- **ViewModel do item:** `ObservableObject` + `[ObservableProperty]` para `X`, `Y`, `Z`, `Titulo`, `Texto`, `EstaSelecionado`, `EstaEditando`. O ViewModel "embrulha" o `BoardItem` do Model.
- **Criar no centro:** por enquanto, o centro da área do quadro com um pequeno desvio aleatório (para não empilhar); depois da Etapa 7, vira o centro da área visível.
- **Visual da nota e do bloco (Sidney):** seção 5.8 (medidas, fontes e cores) e 5.3.
- **Selecionar:** `MouseLeftButtonDown` no item → marca `EstaSelecionado` e desmarca os outros; o contorno (seção 5.8) aparece por `Trigger` ou `BooleanToVisibilityConverter`.
- **Arrastar:** guardar a posição do mouse ao apertar (`e.GetPosition(canvas)`), `CaptureMouse()`, somar a diferença em `X`/`Y` no `MouseMove`, `ReleaseMouseCapture()` ao soltar; o item arrastado recebe `Z` = maior Z + 1.
- **Editar:** `e.ClickCount == 2` detecta dois cliques; troca o `TextBlock` por um `TextBox` (mesma fonte e tamanho) e dá foco (`Focus()`). Teclas no `PreviewKeyDown`: Enter sai; Shift+Enter quebra a linha (`Keyboard.Modifiers`); Esc termina; Tab alterna título ↔ texto. Durante a edição, o arraste e o Delete ficam bloqueados. Clicar fora termina a edição.
- **Excluir:** `KeyBinding` de Delete na janela ligado a um comando que remove o selecionado da coleção; não excluir se o foco estiver num `TextBox`.
- **Título do quadro:** mesmo padrão de edição; dados em `Board.Titulo` e `Board.TituloOculto`; visual na seção 5.6.

**Pronto quando:** dá para criar notas e blocos, selecionar, arrastar, editar com as quatro teclas e excluir.

---

### Etapa 6 — Salvamento, notas e ajustes (v0.1)

**Tarefas**

*Arquivos*
- [ ] Criar a pasta do cofre e as subpastas (Sidney)
- [ ] Criar o StorageService (Sidney)
- [ ] Salvar o quadro em JSON (Sidney)
- [ ] Abrir o quadro do JSON (Sidney)
- [ ] Salvar automaticamente 1 s após cada mudança (Sidney)
- [ ] Fazer a gravação atômica (.tmp) (Sidney)
- [ ] Criar o registro de erros (erros.log) (Sidney)

*Estado e notas*
- [ ] Criar o estado.json (Vitor)
- [ ] Abrir o último quadro ao iniciar (Vitor)
- [ ] Salvar cada nota como arquivo .md (Vitor)
- [ ] Renomear o .md ao mudar o título (Vitor)
- [ ] Mostrar o status "Salvando…" / "Salvo" (Vitor)

*Editor de notas*
- [ ] Abrir a nota no editor ao lado (botão direito → Abrir no editor) (Sidney)
- [ ] Modo Editar (texto puro) (Sidney)
- [ ] Modo Ler com Markdown básico (títulos, listas, negrito) (Sidney)
- [ ] Salvar o que foi escrito no .md (Sidney)

*Ajustes*
- [ ] Botão Ajustes (Sidney)
- [ ] Painel de Ajustes (Sidney)
- [ ] Guardar os ajustes no estado.json (Sidney)
- [ ] Opção de abrir a pasta do cofre (Sidney)

*Fechamento*
- [ ] Testar fechar pelo Gerenciador de Tarefas e reabrir (Vitor)
- [ ] Testar os RF da Categoria 1 (Vitor)
- [ ] Corrigir os erros encontrados (Sidney)
- [ ] Criar a tag v0.1 (Vitor)

*TCC*
- [ ] 3.4 Implementação: Categoria 1, com prints e trechos de código (Vitor)

**O que precisa saber**
- **Cofre:** `Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments)`, `Path.Combine`, `Directory.CreateDirectory`. Pastas na seção 5.14.
- **JSON:** `JsonSerializer.Serialize`/`Deserialize` com `JsonSerializerOptions` (`WriteIndented`, nomes em camelCase, ignorar nulos). Converter ViewModels → `Board` antes de salvar e `Board` → ViewModels ao abrir.
- **Salvar automaticamente:** `DispatcherTimer` de 1 s reiniciado a cada mudança ("debounce": só salva quando a pessoa para de mexer); salvar também ao fechar a janela.
- **Gravação atômica:** grava em `arquivo.tmp` e depois `File.Move(tmp, destino, overwrite: true)`: o arquivo real nunca fica pela metade, mesmo se o app fechar no meio.
- **`estado.json`:** uma classe `AppState` com os campos da seção 5.14 (por enquanto: quadro aberto e ajustes).
- **Nota em `.md`:** primeira linha `# Título`, depois o texto; o quadro guarda só o caminho relativo ao cofre. Nome do arquivo sem caracteres proibidos (`Path.GetInvalidFileNameChars()`), com número se repetir; mudar o título renomeia (`File.Move`).
- **Erros:** `try/catch` em salvar e abrir; `File.AppendAllText` no `erros.log` com data e hora. Arquivo de quadro estragado: guardar uma cópia com outro nome e abrir vazio, sem travar.
- **Editor de notas:** painel numa coluna do `Grid` ao lado do quadro. Editar = `TextBox` com várias linhas (`AcceptsReturn`); Ler = Markdown simples desenhado (linhas que começam com `#` viram títulos, `- ` vira "•", `**texto**` vira negrito), montando `TextBlock.Inlines` (`Run`, `Bold`).
- **Ajustes:** painel com `CheckBox`/botões ligados ao `AppState`.

**Pronto quando:** fechar à força e reabrir traz tudo de volta; as notas abrem no Bloco de Notas; os RF da Categoria 1 passam.

---

### Etapa 7 — Câmera e quadro

**Tarefas**

*Câmera*
- [ ] Trocar a lista de itens por uma camada própria (BoardView) (Vitor)
- [ ] Criar a classe Camera (Vitor)
- [ ] Aplicar a MatrixTransform na camada dos itens (Vitor)
- [ ] Ajustar o arraste dos itens ao zoom (Vitor)
- [ ] Mover a câmera arrastando no vazio (Vitor)
- [ ] Mover a câmera com botão do meio, Espaço e Shift + rodinha (Vitor)
- [ ] Zoom pela rodinha e pela pinça, centrado no cursor (Vitor)
- [ ] Zoom por Ctrl + / Ctrl − / Ctrl 0, de 10% a 400% (Vitor)
- [ ] Ajustar à tela (Ctrl+1) (Vitor)
- [ ] Botão "Ir para o conteúdo" (Vitor)
- [ ] Salvar e restaurar a câmera no JSON (Vitor)

*Fundo*
- [ ] Permitir posições negativas e repetir o fundo (Sidney)
- [ ] Criar o fundo Pontilhado (padrão) (Sidney)
- [ ] Salvar o modelo no JSON (Sidney)
- [ ] Criar a grade opcional (Sidney)
- [ ] Testar com 200 itens (Sidney)

**O que precisa saber**
- **Mundo × tela:** os itens guardam coordenadas do mundo; a câmera converte (fórmulas na seção 5.7). A classe `Camera` guarda o centro (X, Y), o zoom e o tamanho da tela, e tem `ToWorld`/`ToScreen`.
- **Camada própria (BoardView):** em vez do `ItemsControl`, um controle com um `Canvas` em que o código põe e tira as telas dos itens. Dá mais controle para a câmera agora e para "desenhar só o visível" na Etapa 14.
- **Uma só `MatrixTransform`** no `RenderTransform` da camada dos itens (escala = zoom, translação = centro). Nunca mudar `Canvas.Left/Top` de todos os itens a cada movimento.
- **Zoom no cursor:** guardar o ponto do mundo sob o mouse, mudar o zoom e recalcular o centro para aquele ponto continuar sob o mouse. Rodinha: evento `MouseWheel` (`e.Delta`); a pinça do touchpad chega como Ctrl + rodinha.
- **Arraste com zoom:** a diferença do mouse na tela é dividida pelo zoom para virar diferença no mundo.
- **Ajustar:** `Rect.Union` das caixas de todos os itens, margem de 80 px, zoom no máximo 100%.
- **Pontilhado e grade (Sidney):** `DrawingBrush` com `TileMode="Tile"` e `ViewportUnits="Absolute"`, um ponto (ou quadrado) por bloco; o `Viewport` do pincel acompanha a câmera para o fundo andar junto e se repetir sem fim. Medidas na seção 5.7.

**Pronto quando:** 200 itens, zoom de 10% a 400% e arraste sem travar; reabrir volta com a câmera no lugar.

---

### Etapa 8 — Edição

**Tarefas**

*Desfazer e tamanho*
- [ ] Criar o Checkpoint (foto do quadro antes de cada mudança) (Vitor)
- [ ] Criar as listas de desfazer e refazer, com limite de tamanho (Vitor)
- [ ] Ctrl+Z, Ctrl+Shift+Z e Ctrl+Y (Vitor)
- [ ] Redimensionar com 8 alças (Vitor)

*Ferramentas*
- [ ] Copiar, recortar e colar (Ctrl+C/X/V) (Sidney)
- [ ] Duplicar (Ctrl+D) e Alt + arrastar (Sidney)
- [ ] Camadas (frente, trás, topo, fundo) (Sidney)
- [ ] Bloquear e desbloquear item (Sidney)
- [ ] Guias e encaixe a 6 px ao arrastar (Sidney)

*Cores*
- [ ] Criar a lista das 24 cores (Sidney)
- [ ] Trocar a cor do item (Sidney)
- [ ] Últimas cores usadas e paleta completa (Sidney)

**O que precisa saber**
- **Desfazer por foto (Checkpoint):** antes de cada mudança, transforma o quadro inteiro em JSON (pode comprimir com `GZipStream`) e guarda numa lista. Desfazer troca o estado atual pela última foto e guarda o atual na lista de refazer; refazer faz o contrário; uma mudança nova limpa o refazer. Mudanças seguidas e rápidas (digitação) viram um passo só. Limite total de tamanho (por exemplo 32 MB), apagando as fotos mais antigas. Vantagem: qualquer recurso novo já entra no desfazer, sem código extra.
- **Redimensionar:** `Thumb` (evento `DragDelta`) ou `Adorner` nas 8 posições; Shift mantém a proporção; tamanho mínimo por tipo.
- **Copiar/colar:** os itens viram JSON na área de transferência (`Clipboard`); colar cria ids novos (nota copiada ganha outro `.md`).
- **Camadas:** reordenar o `Z`. **Bloquear:** propriedade `Bloqueado`; arrastar um item bloqueado move a câmera.
- **Guias:** ao arrastar, comparar bordas e centros com os outros itens; a menos de 6 px (dividido pelo zoom), encaixa e desenha a linha-guia numa camada por cima.
- **Cores:** uma classe com a tabela da seção 5.2 (chave, nome, papel, tinta); texto branco em cor escura (luminância = 0,299·R + 0,587·G + 0,114·B, abaixo de ~140 é escura). Últimas cores no `estado.json`.

**Pronto quando:** criar, mover, editar e excluir dez vezes e desfazer tudo de volta.

---

### Etapa 9 — Novos itens

**Tarefas**

*Itens de texto*
- [ ] Post-it com cor e estilos (alfinete, fita, solto, pautado) (Sidney)
- [ ] Lembrar a última cor e estilo do post-it (Sidney)
- [ ] Texto solto (Sidney)
- [ ] Título de 64 px com tamanho em pixels (Sidney)
- [ ] Caixa de texto (Sidney)
- [ ] Tabela (Sidney)
- [ ] Adicionar e remover linhas e colunas da tabela (Sidney)

*Formas*
- [ ] Biblioteca de formas (Vitor)
- [ ] Painel de formas com busca e categorias (Vitor)

*Linhas e setas*
- [ ] Linha solta com duas pontas (Vitor)
- [ ] Prender as pontas nos itens (Vitor)
- [ ] Linha reta, curva e ângulo (Vitor)
- [ ] Direção da seta (sem, uma, duas, inverter) (Vitor)
- [ ] Ponto no meio da linha para ligar outra linha (Vitor)
- [ ] Alça para dobrar a linha (Vitor)
- [ ] Traço barbante e cores das linhas (Sidney)
- [ ] Apagar as linhas junto com o item (Vitor)

**O que precisa saber**
- **Receita de um tipo novo:** valor novo no tipo, campos novos no `BoardItem` (JSON, seção 5.14), tela própria (`DataTemplate` ou controle), comando de criar; ele já entra no desfazer e na cópia.
- **Post-it, texto solto, título, caixa de texto e tabela:** medidas na seção 5.8. Alfinete e fita podem ser desenhados em código (`OnRender` com `DrawingContext`: círculos, gradientes, polígono em zigue-zague).
- **Formas:** `Path` com geometria no formato de caminho SVG (`Geometry.Parse("M 0 0 L 100 0 ...")`), desenhada numa grade 100×100 e esticada (`Stretch="Fill"`). A biblioteca é uma lista (chave, nome, categoria, geometria); busca e filtro com LINQ. Lista na seção 5.8.
- **Tabela:** dados como `List<List<string>>`; tela com um `Grid` cujas linhas e colunas são criadas em código; Tab passa de célula e, na última, cria uma linha.
- **Linhas:** `Path` com segmento reto, curva de Bézier ou polilinha (ângulo). Cada ponta guarda o id do item e o lado (cima, baixo, esquerda, direita); quando o item se move, recalcular o ponto no meio daquele lado. Seta = pequeno triângulo no fim, girado na direção da linha. Regras na seção 5.9.
- **Barbante (Sidney):** desenhar a corda como duas linhas finas trançadas na cor escolhida; o "beliscão" é uma mola amortecida que mexe o ponto do meio.

**Pronto quando:** ligar três itens, mover todos, e as linhas seguem sem soltar.

---

### Etapa 10 — Bandeja e menus

**Tarefas**

*Bandeja*
- [ ] Criar o painel base dos menus (Vitor)
- [ ] Criar o botão e o painel da bandeja (Vitor)
- [ ] Clicar na bandeja cria no centro (Vitor)
- [ ] Arrastar da bandeja cria onde soltar (Vitor)
- [ ] Botão direito no vazio abre a bandeja no cursor (Vitor)
- [ ] Dois cliques no vazio repetem o último item (Vitor)
- [ ] Tirar os botões temporários (Vitor)

*Menus*
- [ ] Menu do item (cor, estilo, editar, duplicar, bloquear, camadas, excluir) (Sidney)
- [ ] Menus da linha, da forma e da tabela (Sidney)
- [ ] Menu em duas colunas quando não cabe (Sidney)
- [ ] Ligar itens segurando o botão direito (Sidney)
- [ ] Testar um mapa mental só com o mouse (Sidney)

**O que precisa saber**
- **Menus dentro da janela:** uma camada por cima do quadro (não `ContextMenu` nem `Popup`), que se posiciona onde o mouse clicou e nunca sai da janela. Regras na seção 5.10.
- **Animações:** `Storyboard` e `DoubleAnimation` (opacidade, escala, deslocamento), com as curvas da seção 5.4.
- **Arrastar da bandeja:** `DragDrop.DoDragDrop` com um `DataObject` (tipo, cor, estilo) e o evento `Drop` no quadro, convertendo o ponto da tela para o mundo.
- **Último item:** "molde" (tipo, cor, estilo, tamanho) guardado no `estado.json`.
- **Ligar com botão direito:** separar clique de arraste pela distância percorrida; ao soltar, descobrir o item embaixo do mouse (`InputHitTest`).

**Pronto quando:** um mapa mental de 10 itens e 8 linhas é feito só com o mouse.

---

### Etapa 11 — Vários quadros e lateral

**Tarefas**

*Quadros*
- [ ] Criar o serviço de biblioteca de quadros (Sidney)
- [ ] Criar quadro (Ctrl+N) (Sidney)
- [ ] Renomear, duplicar e excluir quadro (Sidney)
- [ ] Tela "Nenhum quadro" (Sidney)
- [ ] Lixeira: mover, restaurar e apagar de vez (Sidney)
- [ ] Limpar a lixeira depois de 3 dias (Sidney)
- [ ] Gerar miniaturas e criar a galeria (Sidney)

*Lateral e busca*
- [ ] Criar a barra lateral com a lista de quadros (Vitor)
- [ ] Recolher e mostrar a lateral (Vitor)
- [ ] Pastas de quadros (Vitor)
- [ ] Arrastar quadro para pasta (Vitor)
- [ ] Fixar e marcar como importante (Vitor)
- [ ] Itens do quadro na lateral (Vitor)
- [ ] Procurar (Ctrl+K) (Vitor)
- [ ] Buscar no quadro (Ctrl+F) (Vitor)
- [ ] Voltar e avançar (Alt+← / Alt+→) (Vitor)

**O que precisa saber**
- Listar arquivos (`Directory.EnumerateFiles`), mover e renomear (`File.Move`); salvar o quadro atual antes de trocar. Um `LibraryViewModel` para tudo o que a lateral e a galeria mostram.
- **Lixeira:** mover o quadro (e as notas dele) para `Lixeira` guardando a data; ao abrir o app, apagar o que passou de 3 dias.
- **Miniaturas:** `RenderTargetBitmap` + `PngBitmapEncoder`, guardadas em `Sistema\Miniaturas`.
- **Busca:** LINQ sobre nomes de quadros, textos das notas e dos itens.
- **Voltar/avançar:** duas pilhas (`Stack<T>`) de quadros abertos.
- Visual e regras: seções 5.6 e 5.13.

**Pronto quando:** 20 quadros em 3 pastas; excluir e restaurar; achar um texto pelo Ctrl+K.

---

### Etapa 12 — Texto formatado e caligrafia

**Tarefas**

*Formatação*
- [ ] Criar o leitor de texto formatado (Markdown) (Vitor)
- [ ] Criar o campo de edição formatada (Vitor)
- [ ] Ctrl+B, Ctrl+I e Ctrl+U (Vitor)
- [ ] Barra de formatação ao selecionar texto (Vitor)

*Listas e caligrafia*
- [ ] Listas com bolinha e numeradas digitando (Sidney)
- [ ] Embutir as fontes de caligrafia (Sidney)
- [ ] Opção de caligrafia com prévia (Sidney)

**O que precisa saber**
- Regras na seção 5.12.
- **Mostrar:** `Regex` para achar as marcas e montar `TextBlock.Inlines` (`Run` com `FontWeight`, `FontStyle`, `TextDecorations`, `Foreground`, `Background`).
- **Editar sem ver as marcas:** `RichTextBox` + `FlowDocument`, convertendo Markdown → documento ao entrar e documento → Markdown ao sair. A barra usa a seleção do `RichTextBox` e `TextRange.ApplyPropertyValue`.
- **Listas:** regras no `PreviewKeyDown` do campo.
- **Caligrafia:** fontes da seção 5.3 embutidas como Resource; nome da família guardado no JSON (`estilo.fonte`).

**Pronto quando:** formatar, fechar, reabrir, e a formatação continua igual.

---

### Etapa 13 — Navegação e modos (v0.5)

**Tarefas**

*Código*
- [ ] Cenas com câmera animada (Sidney)
- [ ] Modo apresentar (Sidney)
- [ ] Tela cheia (F11) (Vitor)
- [ ] Modo somente visualização (Vitor)
- [ ] Barra de cima com título, "…" e botões da janela (Vitor)

*Fechamento da Categoria 2*
- [ ] Testar os RF da Categoria 2, metade 1 (Vitor)
- [ ] Testar os RF da Categoria 2, metade 2 (Sidney)
- [ ] Corrigir os erros encontrados (Vitor)
- [ ] Corrigir os erros encontrados (Sidney)
- [ ] Criar a tag v0.5 (Vitor)

*TCC*
- [ ] 3.4 Implementação: salvamento, câmera e edição (Vitor)
- [ ] 3.4 Implementação: itens, menus e quadros (Vitor)

**O que precisa saber**
- **Animar a câmera:** `CompositionTarget.Rendering` (roda uma vez por quadro da tela), interpolando centro e zoom com uma curva de suavização.
- **Tela cheia:** `WindowStyle="None"`, `WindowState="Maximized"`, `Topmost` só com o app ativo (eventos `Activated`/`Deactivated`).
- **Somente visualização:** um `bool` no `MainViewModel` checado no `CanExecute` de todo comando de edição e no início das ações de mouse.
- **Barra própria:** `WindowChrome` (tira a moldura do Windows) e `DragMove()` para arrastar a janela.
- Regras nas seções 5.6 e 5.13.

**Pronto quando:** os RF da Categoria 2 passam.

---

### Etapa 14 — Desempenho

**Tarefas**

*Fluidez*
- [ ] Criar o contador de FPS (Ctrl+Shift+F) (Vitor)
- [ ] Criar o botão de teste com 500 itens (Vitor)
- [ ] Arraste pelo TranslateTransform, gravando X/Y ao soltar (Vitor)
- [ ] BitmapCache nos itens parados (Vitor)
- [ ] Desenhar só os itens visíveis (quadtree) (Vitor)
- [ ] Reaproveitar os itens que saem da tela (Vitor)
- [ ] Medir 60 fps com 500 itens (Vitor)

*Abertura, memória e publicação*
- [ ] Medir a abertura em até 5 s (Sidney)
- [ ] Devolver memória só fora de uso (Sidney)
- [ ] Revisar todos os atalhos de teclado (Sidney)
- [ ] Revisar a separação do MVVM (Sidney)
- [ ] Publicar o executável único (Sidney)
- [ ] Criar o publicar.bat e o ícone do app (Sidney)
- [ ] Testar o .exe num PC sem .NET (Sidney)

**O que precisa saber**
- **FPS:** medir o tempo entre quadros no `CompositionTarget.Rendering`; mostrar fps, pior quadro e itens na tela/total. `RenderCapability.Tier == 2` = usando a placa de vídeo.
- **Arraste rápido:** durante o arraste, mexer só num `TranslateTransform`; gravar `X`/`Y` uma vez, ao soltar. Câmera e arraste aplicados uma vez por quadro.
- **Quadtree:** estrutura que divide o mundo em quatro quadrantes, e cada quadrante em mais quatro, para responder rápido "que itens estão nesta área?". A tela só cria os itens perto da área visível (margem de meia tela); os que saem são guardados e reaproveitados; criar no máximo alguns por quadro (~3 ms). Bom para o capítulo 2 do TCC: liga o nome do app à técnica.
- **`BitmapCache`:** itens parados viram imagem na placa de vídeo (escala 2× a da tela); refazer quando a câmera para.
- **Abertura:** `Stopwatch`; carregar lateral e miniaturas depois que a janela aparece (`async`).
- **Memória:** quando o app está minimizado ou 15 s em segundo plano, pedir ao Windows para liberar a memória parada; **nunca** com a janela ativa (trava o próximo movimento).
- **Publicar:** comando da seção 2.1; `publicar.bat` que fecha se o app estiver aberto, publica e copia o `.exe`.

**Pronto quando:** 60 fps com 500 itens nos dois PCs (anotar a configuração de cada um para o TCC) e o `.exe` roda sem o .NET instalado.

---

### Etapa 15 — Design e polimento (Categoria 3)

**Tarefas**

*Interface*
- [ ] Tema escuro e troca pelo botão (Vitor)
- [ ] Seguir o tema do Windows (Vitor)
- [ ] Vidro com desfoque (Vitor)
- [ ] Borda de luz que segue o mouse (Vitor)
- [ ] Animações com mola (Vitor)
- [ ] Ponteiro próprio (Vitor)
- [ ] Faíscas ao clicar (Vitor)
- [ ] Nitidez de 100% a 200% (Vitor)
- [ ] Respeitar as animações do Windows (Vitor)

*Visual dos itens*
- [ ] Visual completo do post-it (Sidney)
- [ ] Nota branca e espiral (Sidney)
- [ ] Bloco de vidro com cor forte (Sidney)
- [ ] Modelos Liso, Cortiça, Branco, Escuro e Lousa, com molduras (Sidney)
- [ ] Sombras no tom do fundo (Sidney)
- [ ] Transparência do fundo das formas (Sidney)

*Ajuda*
- [ ] Tela inicial e tutorial (Sidney)
- [ ] Balões de ajuda (Sidney)
- [ ] Dica na tela (Sidney)
- [ ] Balão de zoom (Sidney)
- [ ] Inércia da câmera (Vitor)

*Extras*
- [ ] Exportar PNG e PDF (Vitor)
- [ ] Desenho à mão (Vitor)
- [ ] Anexar um item a outro (Vitor)
- [ ] Cartão de arquivo com prévia de PDF (Sidney)
- [ ] Cartão de link (Sidney)
- [ ] Galeria de Designs prontos (Sidney)
- [ ] Quadro de exemplo no cofre novo (Sidney)
- [ ] Página Cofre na lateral (árvore da pasta) (Sidney)

*Seleção múltipla e organização*
- [ ] Seleção com Shift + clique (Vitor)
- [ ] Caixa de seleção com Shift + arrastar (Vitor)
- [ ] Ctrl+A, mover e excluir vários itens (Vitor)
- [ ] Seleção com o botão direito e menu da seleção (Sidney)
- [ ] Agrupar e desagrupar (Sidney)
- [ ] Alinhar e distribuir (Sidney)

*Imagens, vídeos e links entre notas*
- [ ] Colar e arrastar imagens para o quadro (Vitor)
- [ ] Arrastar vídeos e tocar no quadro (Vitor)
- [ ] Copiar os anexos para o cofre (Vitor)
- [ ] Links [[Nota]] com autocompletar (Sidney)
- [ ] Seguir o link com Ctrl+clique (Sidney)
- [ ] Rodapé "Mencionado em" (Sidney)
- [ ] Atualizar os links ao renomear a nota (Sidney)

*TCC*
- [ ] 3.4 Implementação: desempenho (Vitor)
- [ ] 3.4 Implementação: design e extras (Vitor)

**O que precisa saber (por assunto)**
- **Tema:** dois `ResourceDictionary` (Light/Dark) trocados em tempo real; as telas usam `DynamicResource`. Tema do Windows pelo registro (`HKCU\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize`, valor `AppsUseLightTheme`). Cores na seção 5.1.
- **Vidro:** `VisualBrush` do que está atrás + `BlurEffect` + cor translúcida, com `BitmapCache`; brilho que segue o mouse com `RadialGradientBrush` (`MappingMode="Absolute"`, centro no mouse). Regras na seção 5.5.
- **Animações:** curvas da seção 5.4. **Ponteiro:** desenhado em código no tamanho da escala da tela (`VisualTreeHelper.GetDpi`). **Faíscas:** camada transparente por cima de tudo, `IsHitTestVisible="False"`.
- **Nitidez:** `UseLayoutRounding="True"`; cache dos itens em 2× a escala da tela. **Animações do Windows:** `SystemParameters.ClientAreaAnimation`.
- **Visual dos itens:** desenho em código (`OnRender`/`DrawingContext`) para faixa adesiva, canto levantado, sombras e espiral; medidas nas seções 5.7 e 5.8. A Cortiça precisa de uma textura de cortiça 384×384 que se repete sem emenda.
- **Exportar:** `RenderTargetBitmap` em alta resolução; PDF com uma só imagem (pesquisar uma biblioteca gratuita, como PdfSharp). Regras na seção 5.13.
- **Imagens, arquivos e links:** `Clipboard.GetImage`, `DataFormats.FileDrop`, `MediaElement` (vídeo); prévia de PDF com `Windows.Data.Pdf`; links com `HttpClient` lendo `og:title` e `og:image` da página. Tudo copiado para `Anexos\`.
- **Desenho à mão:** cada traço é uma lista de pontos com ferramenta, cor e espessura, desenhado como `Polyline`/`Path`.
- **Seleção múltipla:** trocar "item selecionado" por uma lista de selecionados; caixa de seleção azul a 12% com borda de 1 px.
- **Links entre notas:** `Regex` para `[[...]]`; autocompletar com uma lista filtrada das notas; "Mencionado em" = notas que têm um link para esta.
- **Designs, tela inicial e quadro de exemplo:** cada design é um quadro montado em código (lista de itens). Regras na seção 5.13.

**Pronto quando:** o app fica igual à especificação da seção 5 nos dois temas, e cada extra funciona.

---

### Etapa 16 — Testes

**Tarefas**

*Testes do app*
- [ ] Montar o plano de testes (Vitor)
- [ ] Testar os RF das Categorias 1 e 2 (Vitor)
- [ ] Testar os RF da Categoria 3 (Sidney)
- [ ] Testar os RNF (Sidney)
- [ ] Medir o desempenho no PC do Vitor (Vitor)
- [ ] Medir o desempenho no PC do Sidney (Sidney)
- [ ] Teste de confiabilidade (fechar forçado, JSON corrompido) (Vitor)
- [ ] Preparar o teste com colegas e o questionário (Vitor)
- [ ] Aplicar o teste com colegas (Vitor)
- [ ] Corrigir os erros encontrados (Vitor)
- [ ] Corrigir os erros encontrados (Sidney)

*TCC*
- [ ] 3.5 Testes (Vitor)
- [ ] 4 Resultados: testes funcionais (Vitor)
- [ ] 4 Resultados: desempenho (Vitor)
- [ ] 4 Resultados: teste com colegas (Vitor)
- [ ] 4 Discussão (Vitor)

**O que precisa saber:** tabela de testes com requisito · passos · resultado esperado · resultado obtido · passou/falhou. Medidas: abertura (média de 10), fps com 100, 300 e 500 itens, memória aberto e minimizado, tempo de salvar um quadro grande.

---

### Etapa 17 — Entrega e banca

**Tarefas**

*App*
- [ ] Publicar o .exe final (Vitor)
- [ ] Escrever o README (Vitor)
- [ ] Criar a tag v1.0 e o Release no GitHub (Vitor)

*TCC*
- [ ] 5 Conclusão: resposta à questão de pesquisa (Vitor)
- [ ] 5 Conclusão: objetivos atingidos (Vitor)
- [ ] 5 Conclusão: trabalhos futuros (Vitor)
- [ ] Completar o resumo (Vitor)
- [ ] Sumário, lista de figuras e lista de tabelas (Vitor)
- [ ] Revisar as referências na ABNT (Vitor)
- [ ] Revisão do orientador e ajustes (Vitor)
- [ ] Gerar a versão final do .docx (Vitor)

*Banca*
- [ ] Fazer os slides (Vitor)
- [ ] Escrever o roteiro da demonstração (Vitor)
- [ ] Gravar o vídeo de demonstração (plano B) (Vitor)
- [ ] Ensaiar a apresentação (Vitor)
- [ ] Ensaiar a apresentação (Sidney)
- [ ] Testar o app no computador da apresentação (Sidney)

---

## 8. TCC

- Título: **QUADTREE: aplicativo de quadro visual para criação de mapas mentais**. Autores: Sidney Campos e Vitor Gabriel Costa Moreira.
- Estrutura (seção 1.8 do capítulo 1): 1 Introdução · 2 Fundamentação teórica · 3 Desenvolvimento (3.1 Método, 3.2 Requisitos, 3.3 Modelagem, 3.4 Implementação, 3.5 Testes) · 4 Resultados e discussão · 5 Conclusão.
- **Pronto:** capítulo 1 (falta trocar "quadro de tamanho definido" por quadro infinito). O resumo tem colchetes a completar depois dos capítulos 4 e 5.
- Cada capítulo é escrito na etapa indicada na lista: o 4 e o 5 só com o app pronto.
- Os documentos do TCC são montados e revisados no **Claude Docs**; só gerar o `.docx` quando o Vitor disser **"finalize"**. Ao mexer num documento, atualizar o existente, não criar outro.
- Método de gestão: inspirado no Kanban, na base "Gestão de trabalho" do Notion (não é o Kanban em si).
- **Não dizer que WPF, MVVM, JSON, Markdown, modelagem e POO foram vistos no curso** (só o básico de C#).
- Os arquivos do TCC ficam na pasta `tcc/`, fora do git.

---

## 9. Ideias para o TCC que vêm do código

- **Quadtree:** a estrutura de dados que dá nome ao app (Etapa 14) merece uma seção no capítulo 2 e uma explicação com figura no 3.4.
- **Desfazer por foto:** decisão de projeto simples de explicar (troca memória por simplicidade).
- **Gravação atômica:** mostra o cuidado com o RNF "Não perder dados".

---

## 10. Decisões registradas

| Data | Decisão |
|---|---|
| 20/11/2026 | Itens chamados de "nota" e "bloco" (nunca "nó"). |
| 20/11/2026 | Requisitos em 3 categorias: 1 = necessário para rodar, 2 = novas funções, 3 = design e extras. |
| 20/11/2026 | Equipe: Vitor e Sidney; Visual Studio 2026 (.NET 10). |
| 21/11/2026 | Uma branch para cada membro; tudo se junta na `main` por pull request. |
| 22/11/2026 | Quadro infinito. |
| 22/11/2026 | Lixeira guarda por 3 dias. |
| 22/11/2026 | Modelo padrão Pontilhado; os outros modelos (Liso, Cortiça, Branco, Escuro, Lousa) na Categoria 3. |
| 22/11/2026 | Título grande, editor de notas (sem links) e Ajustes são Categoria 1. |
| 22/11/2026 | Seleção múltipla, agrupar, alinhar, seleção pelo botão direito, imagens, vídeos, anexos e links entre notas são Categoria 3. |
| 22/11/2026 | Desfazer por foto do quadro (Checkpoint); camada própria para os itens a partir da Etapa 7. |
| 22/11/2026 | Todas as decisões importantes são do Vitor; o Sidney só programa. TCC, diagramas, planejamento, README e slides são do Vitor. |
| 22/11/2026 | O PDF de requisitos não será atualizado; este arquivo vale para a ordem de construção e a especificação. |
| 22/11/2026 | O Vitor e o Sidney escrevem o código; o Claude guia, explica e revisa. |
| 22/11/2026 | Este CLAUDE.md vai para o GitHub, tem a lista de tarefas e toda a especificação do app; não faz referência a nenhum outro projeto. |
| 22/11/2026 | No começo de toda sessão, o Claude pergunta se é o Vitor ou o Sidney e mostra a próxima tarefa daquela pessoa. |
| 22/11/2026 | Dois cliques na nota editam no quadro; o editor de notas ao lado abre pelo botão direito → "Abrir no editor". |
| 22/11/2026 | Fontes do app: **Inter Tight** (interface) e **Nunito Sans** (conteúdo do quadro), no lugar de Inter e Nunito. Pasta `fontes/` no GitHub. |
| 22/11/2026 | O Claude só atualiza o `CLAUDE.md` (tarefas, estado, decisões) quando o Vitor disser "salvar" ou "finalizar a sessão", e então lembra de mandar para o GitHub. |
| 22/11/2026 | Em cada tarefa, bloco ou etapa, o Claude cria um doc no Claude Docs com a lista de tarefas para o Vitor riscar e a contextualização embaixo (seção 1.7); no "salvar", o Claude lê o doc para atualizar as caixinhas. |

---

## 11. Pendências e perguntas em aberto

- [ ] Nomes no código: português ou inglês (decidir na Etapa 4).
- [ ] Nome das branches: `vitor`/`sidney` ou uma por tarefa, como `feat/minha-tarefa` (página "regras do github").
- [ ] Extensão do arquivo do quadro e nome da pasta do cofre (Etapa 3).
- [ ] Onde está a pasta `tcc/` (não está mais na pasta do repositório depois do clone de 22/11/2026).
