# Residencial Forms

Formulário de cadastro de telefone para o **Residencial Imperatriz**, integrado ao backend Supabase do sistema Port Go. Permite que moradores registrem seu número de WhatsApp e configurem preferências de notificação para entregas e comunicados do condomínio.

## Stack

- HTML5 / CSS3 (inline) / JavaScript vanilla
- [Supabase](https://supabase.com) — backend via REST API (sem SDK, chamadas `fetch` diretas)
- Plus Jakarta Sans (Google Fonts)
- Sem frameworks ou dependências externas

## Funcionalidades

- Cadastro de morador com: apartamento, nome, telefone (+55) e descrição profissional opcional
- Preferências de notificação configuráveis:
  - Mensagens de encomendas normais (padrão: ativado)
  - Alertas de entregas urgentes/perecíveis (padrão: ativado)
  - Ligação telefônica para urgências (padrão: desativado)
  - Comunicados oficiais do condomínio (padrão: desativado)
- Validação de campos com feedback visual e animação de erro
- Contador de caracteres no campo "Sobre você" (máx. 500)
- Tela de sucesso com opção de cadastrar novo telefone
- Prevenção de double-tap zoom no iOS

## Fluxo de envio

1. Busca o `condominio_id` pelo slug `residencial-imperatriz`
2. Busca o `apartamento_id` pelo número informado
3. Insere o registro em `moradores`
4. Insere as preferências em `notification_prefs`

## Variáveis de ambiente

As credenciais do Supabase estão definidas diretamente no `index.html` (projeto estático sem build):

| Variável | Descrição |
|---|---|
| `SUPABASE_URL` | URL do projeto Supabase |
| `SUPABASE_ANON_KEY` | Chave anônima pública do Supabase |
| `CONDOMINIO_SLUG` | Slug do condomínio (`residencial-imperatriz`) |

## Como rodar

Abra `index.html` diretamente no navegador, ou use um servidor local:

```bash
npx serve .
```

## Deploy

Projeto estático — compatível com Vercel, Netlify, GitHub Pages ou qualquer servidor HTTP.

## Estrutura de pastas

```
Residencial_Forms/
├── index.html              # Formulário principal (HTML + CSS + JS)
├── residencial-logo.png    # Logo do Residencial Imperatriz
├── IDENTITY.md             # Design system Port Go (cores, fontes, tokens)
├── CLAUDE.md               # Instruções para o Claude Code
└── .claude/
    └── settings.local.json
```

## Design system

Documentado em `IDENTITY.md`. Principais características:

- **Tema:** Dark only, glassmorphism
- **Fonte:** Plus Jakarta Sans (300–800)
- **Cor primária:** `hsl(38, 92%, 50%)` (dourado)
- **Fundo:** `hsl(225, 50%, 3%)` (quase preto azulado)
- **Transições:** `300ms cubic-bezier(0.4, 0, 0.2, 1)`
