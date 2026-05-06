# Portfólio de Grupo — Design de Produto IV

Este repositório é a **entrega final do vosso grupo**. Cada commit no `main` atualiza automaticamente a galeria pública do site da disciplina (~1-2 minutos depois do push).

---

## 0. Setup (uma vez por grupo)

### Ferramentas a instalar

- **GitHub Desktop** — <https://desktop.github.com> (interface gráfica para git, sem terminal)
- **Obsidian** — <https://obsidian.md> (editor de markdown, gratuito)

### Conta GitHub

Cada elemento do grupo precisa de uma conta GitHub: <https://github.com/signup>. Usem o vosso e-mail de aluno.

---

## 1. Aceitar a tarefa e clonar o repositório

**Apenas um elemento do grupo faz isto** (o "líder técnico" — quem ficará responsável por commits/pushes):

1. Abre o link da tarefa enviado pelo professor (Classroom invite).
2. Cria uma equipa nova com um nome curto (ex.: `grupo-A`, `o-quadrado`). Os colegas juntam-se a esta equipa.
3. Aceita a tarefa → o GitHub cria automaticamente um repositório para o grupo.
4. Abre o **GitHub Desktop** → menu *File* → *Clone repository* → escolhe o repositório recém-criado → escolhe uma pasta no teu computador.

Os outros elementos do grupo:

- Aceitam o mesmo link e juntam-se à equipa criada (não criam equipa nova).
- **Não precisam de clonar o repositório** se seguirem o fluxo recomendado (ver secção 3).

---

## 2. Abrir como Obsidian Vault

1. Abre o **Obsidian**.
2. Botão *Open another vault* (ou no primeiro arranque, *Open folder as vault*) → seleciona a pasta do repositório clonado.
3. Pronto. O Obsidian já está pré-configurado:
   - Imagens arrastadas para um documento são guardadas automaticamente numa subpasta `attachments/` ao lado desse documento.
   - Os links são em formato Markdown padrão (`![](attachments/foto.jpg)`), não em formato Wiki (`![[foto.jpg]]`). Isto é **essencial** — o site não consegue mostrar imagens com formato Wiki.

> **Não alterem** as definições do vault em *Settings → Files & Links*. A configuração do template depende delas.

---

## 3. Como dividir trabalho sem conflitos de git

Não precisam de saber git. Recomendamos este fluxo:

**O líder técnico** é o único que faz commits/pushes. Os outros elementos:

1. Editam os ficheiros `.md` na sua própria máquina (Obsidian local) ou pedem ao líder o template em texto.
2. Entregam o texto/imagens ao líder (email, drive, pen, o que preferirem).
3. O líder copia o conteúdo para os ficheiros corretos do repositório clonado, faz commit e push.

Este fluxo é **mais lento mas evita conflitos de git** (que são complicados de resolver para quem nunca usou). Se o grupo se sentir confortável, podem todos clonar e editar — mas leiam sobre `git pull` antes de cada `push`.

---

## 4. Estrutura do repositório

```text
.
├── index.md                              # Página de grupo (Home)
├── contexto.md                           # A. Contexto de Design (resumo, referências, moodboard)
├── produtos/
│   └── _modelo/                          # Template — DUPLICAR para cada elemento
│       ├── index.md                      # Página do produto individual
│       ├── processo.md                   # Sub-página de processo
│       └── attachments/                  # Imagens/ficheiros do produto
├── attachments/                          # Imagens partilhadas do grupo
└── README.md                             # Este ficheiro
```

### O que preencher

#### A. Página de grupo (`index.md`)

Atualizem o frontmatter (linhas no topo entre `---`):

```yaml
group_name: "Nome do Grupo"
group_number: "G01"
course: "DesignDeProdutoIV"
members:
  - number: "20231234"
    name: "Aluno A"
  - number: "20235678"
    name: "Aluno B"
```

Substituam a `attachments/hero.jpg` por uma **fotografia de conjunto** dos trabalhos (mais conceptual, que espelhe a estratégia do grupo). Atualizem a tabela de elementos e os cards da Galeria de Produtos (um por membro).

#### B. Contexto (`contexto.md`)

Resumo (PT+EN, máx. 500 palavras), recolha de objetos a redesenhar e moodboard.

#### C. Páginas individuais (`produtos/`)

Para cada elemento:

1. No Obsidian, **duplicar** a pasta `produtos/_modelo/` e renomear para `produtos/<numero>-<nome>/` (ex.: `produtos/20231234-maria/`).
2. Atualizar o frontmatter do `index.md` (`title`, `hero_title`, `hero_subtitle`, `student_name`, `student_number`).
3. Preencher as secções de `index.md` (Conceito, Enquadramento, Tecnologia, Função, Apresentação) — é a **prancha-resumo digital** seguindo o esquema-base C-E-T-F.
4. Preencher `processo.md` com as 9 secções, do **mais recente** para o **mais antigo**:
   1. Protótipo(s) — fotografias de estúdio, fundo branco
   2. Processo de prototipagem
   3. Modelos 3D do Molde
   4. Protótipos exploratórios
   5. Modelos 3D
   6. Outros Modelos
   7. Esboços e Pranchas-Resumo
   8. Pesquisa (moodboards, objetos similares)
   9. Outros elementos relevantes

5. **Voltar ao `index.md` da raiz** e adicionar um card na Galeria de Produtos para o novo membro:

```html
<a class="gallery-card" href="produtos/20231234-maria/">
  <img src="produtos/20231234-maria/attachments/hero.jpg" alt="" />
  <h3>Nome do Projeto</h3>
  <p>Nome do Aluno</p>
</a>
```

A pasta `_modelo/` original pode ser deixada como referência ou apagada — não aparece na galeria pública.

---

## 5. Imagens — como pôr a funcionar

### Imagens no corpo do texto

**Basta arrastar** uma imagem do Finder/Explorer para a janela do Obsidian. O Obsidian:

- Copia a imagem para `attachments/` ao lado do documento atual
- Insere automaticamente `![](attachments/nome-da-imagem.jpg)`

Estas imagens **funcionam sempre**, em qualquer ficheiro `.md`.

### Imagem de capa (hero) — convenção

**Regra única**: a imagem usada como hero (e thumbnail na galeria) deve chamar-se sempre `hero.jpg` (ou `hero.png`), guardada em `attachments/` ao lado do ficheiro `.md`. Cada nível tem o seu próprio `hero.jpg`:

- `attachments/hero.jpg` ao lado de `index.md` e `contexto.md` → hero do **grupo**
- `produtos/<numero>-<nome>/attachments/hero.jpg` ao lado do `index.md` e `processo.md` desse produto → hero do **produto**

Outras imagens no corpo (`![](attachments/foto.jpg)`) podem ter qualquer nome — só o hero é que tem nome obrigatório.

#### Caminho no frontmatter (`hero_image:`)

Há **uma regra de prefixo**:

| Tipo de ficheiro                                     | `hero_image:`             |
| ---------------------------------------------------- | ------------------------- |
| `index.md` (qualquer pasta)                          | `attachments/hero.jpg`    |
| Outros ficheiros (ex.: `contexto.md`, `processo.md`) | `../attachments/hero.jpg` |

O template já está pré-configurado corretamente — basta substituir o ficheiro `hero.jpg` pela vossa imagem real, mantendo o nome.

> *Porquê o `../`?* Os caminhos no frontmatter não são reescritos pelo gerador do site, ao contrário das imagens no corpo do texto. Os ficheiros não-`index.md` são publicados num URL com um nível extra (`processo/` em vez de `processo.html`), e por isso precisam de `../` para chegar à pasta `attachments` ao lado.

### Vídeos e modelos 3D

O site converte automaticamente:

- `![](video.mp4)` → vídeo embebido (também `.webm`, `.mov`, `.ogg`)
- `![](modelo.stl)` → visualizador 3D (também `.step`, `.obj`, `.glb`, `.gltf`)
- Links `https://a360.co/...` → visualizador Autodesk Fusion

---

## 6. Commit e push (apenas o líder)

No GitHub Desktop:

1. Vê os ficheiros alterados na coluna esquerda.
2. Escreve uma mensagem curta no campo *Summary* (ex.: "adicionar conceito do projeto da Maria").
3. *Commit to main* (botão azul).
4. *Push origin* (em cima).

Espera ~1-2 minutos. A galeria pública atualiza-se sozinha.

---

## 7. Privacidade

- `published: false` no `index.md` da raiz → o grupo **não** aparece na galeria pública.
- `published: false` no `index.md` de um produto → esse produto **não** é listado.

O repositório continua a existir, apenas não é mostrado.

---

## 8. Esquema-Ferramenta (C-E-T-F)

- **C — Conceito**: ideia, intenção, pergunta de partida
- **E — Enquadramento**: contexto, referências, posicionamento
- **T — Tecnologia**: meios de produção, materiais, ficheiros
- **F — Função**: uso, montagem, replicabilidade

A página de grupo (`index.md` + `contexto.md`) trabalha sobretudo C+E. Cada página de produto trabalha os 4 eixos.

---

## 9. Resolver problemas comuns

| Problema                                                        | Causa provável                                              | Solução                                                                                                            |
| --------------------------------------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| As imagens não aparecem na galeria pública                      | Links em formato Wiki `![[ ]]`                              | Verificar que estão no formato Markdown `![](caminho)`. Vault config deve ter "Use \[\[Wikilinks]]" desligado.     |
| Hero não aparece numa sub-página (`processo.md`, `contexto.md`) | Falta o prefixo `../`                                       | Frontmatter deve ter `hero_image: ../attachments/hero.jpg`                                                         |
| Hero não aparece no `index.md` da raiz do grupo                 | Tem um prefixo `../` a mais                                 | `index.md` deve ter `hero_image: attachments/hero.jpg` (sem `../`)                                                 |
| O grupo não aparece na galeria                                  | `published: false` no frontmatter, ou o último push falhou  | Confirmar `published: true`. No GitHub Desktop, ver se há commits por enviar (*Push origin*).                       |
| Conflito de merge no GitHub Desktop                             | Dois elementos editaram o mesmo ficheiro em paralelo        | Pedir ao professor. Para evitar: seguir o fluxo do líder técnico (secção 3).                                       |

---

## Ajuda

Para qualquer questão técnica, contactem o professor com:

1. Link do repositório
2. Descrição do problema
3. Screenshot, se aplicável
