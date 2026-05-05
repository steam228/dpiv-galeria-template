# Portfólio de Grupo

Este repositório é a **entrega final do vosso grupo**. Tem duas componentes:

- **`index.md`** — página de grupo: conceito comum, marca e embalagem (Fase 2 — 30%)
- **`membros/<numero>-<nome>.md`** — uma página por elemento, com o projeto individual (Fase 1 — 70%)

Cada commit no `main` atualiza automaticamente a galeria pública do site da disciplina (~1-2 minutos).

---

## O que preencher

### 1. Página de Grupo (`index.md`)

No topo do ficheiro, atualizem o frontmatter:

```yaml
group_name: "Nome do Grupo"
group_number: "G01"
course: "DesignDeProdutoIV"   # ou "PrototipagemDigital"
members:
  - name: "Aluno A"
    number: "20XXXXX"
    page: "membros/20XXXXX-aluno-a.md"
  - name: "Aluno B"
    number: "20YYYYY"
    page: "membros/20YYYYY-aluno-b.md"
```

Depois preencham as secções: **Conceito Comum**, **Enquadramento**, **Estratégia de Marca e Embalagem**, e o **catálogo de Projetos Individuais** (cards com link para cada página individual).

### 2. Páginas Individuais (`membros/`)

Cada elemento do grupo:

1. Duplica `membros/_modelo.md`
2. Renomeia para `<numero>-<primeiro-nome>.md` (ex.: `20231234-maria.md`)
3. Atualiza o frontmatter (`student_name`, `student_number`, `title`, `hero_title`, `hero_subtitle`)
4. Preenche as secções: Conceito, Tecnologia, Função, Processo, Galeria, Reflexão

### 3. Imagens e ficheiros (`attachments/`)

- `attachments/hero.jpg` — imagem de capa do grupo (a galeria pública usa-a como thumbnail)
- Coloquem aqui imagens partilhadas (marca, embalagem). Cada elemento pode adicionar imagens/ficheiros próprios à mesma pasta ou criar subpastas.

---

## Conversões automáticas

O site converte automaticamente:

- `![](modelo.stl)` → visualizador 3D interativo (também `.step`, `.obj`, `.glb`, `.gltf`)
- `![](video.mp4)` → vídeo embebido (também `.webm`, `.mov`, `.ogg`)
- Links `a360.co/...` → visualizador Autodesk

---

## Privacidade

- `published: false` no `index.md` → o grupo não aparece na galeria pública.
- `published: false` no `.md` de um membro → essa página individual não é listada.

O repositório continua a existir, apenas não é incluído na galeria.

---

## Esquema-Ferramenta (Design de Produto IV)

Organizem o pensamento pelos 4 eixos:

- **C — Conceito**: ideia, intenção, pergunta de partida
- **E — Enquadramento**: contexto, referências, posicionamento
- **T — Tecnologia**: meios de produção, materiais, ficheiros
- **F — Função**: uso, montagem, replicabilidade

A página de grupo trabalha sobretudo C+E (e a embalagem em T+F). As páginas individuais trabalham os 4 eixos por completo no objeto-brinquedo.
