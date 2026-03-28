# Residencial Forms

Formulario de cadastro de telefone para o **Residencial Imperatriz**, utilizado no contexto do aplicativo Port Go. Pagina estatica com branding customizado.

## Stack

- HTML5
- CSS3 (inline)
- JavaScript puro (vanilla)
- Sem frameworks ou dependencias externas

## Funcionalidades

- Formulario de cadastro de telefone estilizado
- Design system documentado em `IDENTITY.md`:
  - Fonte: Plus Jakarta Sans
  - Cores em HSL
  - Tema escuro (dark theme)
  - Efeitos glassmorphism
- Branding visual do Port Go aplicado

## Pre-requisitos

Nenhum. O projeto e composto por arquivos estaticos que rodam diretamente no navegador.

## Como rodar

Abra o arquivo `index.html` diretamente no navegador ou utilize qualquer servidor HTTP local:

```bash
npx serve .
```

## Deploy

O projeto e destinado a hosting estatico. Pode ser publicado em qualquer plataforma que sirva arquivos HTML (Vercel, Netlify, GitHub Pages, etc.).

## Estrutura de pastas

```
Residencial_Forms/
├── index.html            # Formulario principal
├── residencial-logo.png  # Logo do Residencial Imperatriz
├── IDENTITY.md           # Documentacao do design system (cores, fontes, tokens)
└── .claude/
    └── settings.local.json
```

## Status

**Em desenvolvimento** -- Formulario em fase de construcao e refinamento.
