# Identidade Visual - Port Go

## Fonte
- **Família:** Plus Jakarta Sans
- **Pesos:** 300, 400, 500, 600, 700, 800
- **Import:** `https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap`

## Paleta de Cores (HSL)

### Cores Principais
| Nome | HSL | Uso |
|------|-----|-----|
| **Primary (Dourado)** | `hsl(38, 92%, 50%)` | Cor de destaque principal, botões, links |
| **Accent** | `hsl(38, 70%, 45%)` | Variação mais escura do dourado |
| **Background** | `hsl(225, 50%, 3%)` | Fundo principal (quase preto azulado) |
| **Foreground** | `hsl(210, 40%, 98%)` | Texto principal (branco suave) |

### Cores de UI
| Nome | HSL | Uso |
|------|-----|-----|
| **Card** | `hsl(222, 30%, 14%)` | Fundo de cards |
| **Secondary** | `hsl(223, 30%, 18%)` | Elementos secundários |
| **Muted** | `hsl(223, 25%, 18%)` | Elementos desabilitados |
| **Muted Foreground** | `hsl(215, 20%, 55%)` | Texto secundário/placeholder |
| **Border** | `hsl(223, 25%, 22%)` | Bordas |
| **Input** | `hsl(223, 30%, 16%)` | Fundo de inputs |

### Cores de Status
| Nome | HSL | Uso |
|------|-----|-----|
| **Success** | `hsl(142, 76%, 45%)` | Sucesso (verde) |
| **Info** | `hsl(210, 100%, 52%)` | Informativo (azul) |
| **Warning** | `hsl(38, 92%, 50%)` | Alerta (dourado) |
| **Destructive** | `hsl(0, 84%, 60%)` | Erro/Perigo (vermelho) |

## Border Radius
- **Base (--radius):** `0.875rem` (14px)
- **Large (lg):** `0.875rem`
- **Medium (md):** `calc(0.875rem - 2px)` = ~12px
- **Small (sm):** `calc(0.875rem - 4px)` = ~10px

## Gradientes

### Gradient Primary (Botões)
```css
background: linear-gradient(135deg, hsl(38 92% 50%) 0%, hsl(28 80% 40%) 100%);
```

### Gradient Text (Texto Dourado)
```css
background: linear-gradient(135deg, hsl(38 92% 55%) 0%, hsl(38 70% 45%) 40%, hsl(28 65% 38%) 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

## Estilos de Cards

### Glass Card (Padrão)
```css
background: hsl(220 25% 16%);
border: 1px solid hsl(220 20% 30%);
box-shadow:
  0 8px 32px hsl(224 71% 4% / 0.5),
  inset 0 1px 0 hsl(210 40% 98% / 0.06);
```

### Glass Card Interactive (Hover)
```css
background: hsl(220 22% 15%);
border: 1px solid hsl(220 18% 30%);
/* No hover: */
border-color: hsl(38 92% 50% / 0.4);
box-shadow: 0 0 24px hsl(38 92% 50% / 0.12);
```

## Estilos de Input

### Input Premium
```css
background: hsl(223 40% 10% / 0.8);
border: 1px solid hsl(223 25% 24% / 0.6);
border-radius: 0.75rem; /* rounded-xl */
padding: 0.875rem 1rem; /* py-3.5 px-4 */
font-size: 0.875rem; /* text-sm */
font-weight: 500; /* font-medium */

/* Focus */
border-color: hsl(38 92% 50% / 0.4);
box-shadow: 0 0 0 3px hsl(38 92% 50% / 0.1);
```

## Estilos de Botão

### Botão Primário
```css
background: linear-gradient(135deg, hsl(38 92% 50%) 0%, hsl(28 80% 40%) 100%);
color: hsl(224 71% 4%); /* texto escuro */
font-weight: 700; /* font-bold */
font-size: 0.875rem; /* text-sm */
border-radius: 0.75rem; /* rounded-xl */
```

## Glow Effects

### Primary Glow
```css
box-shadow:
  0 0 20px hsl(38 92% 50% / 0.2),
  0 0 60px hsl(38 92% 50% / 0.06);
```

## Tipografia

| Classe | Tamanho | Peso | Uso |
|--------|---------|------|-----|
| heading-1 | text-2xl | font-extrabold | Títulos principais |
| heading-2 | text-lg | font-bold | Subtítulos |
| label-text | text-xs | font-semibold (uppercase) | Labels |
| body-text | text-sm | font-medium | Texto corpo |
| caption-text | text-xs | font-medium | Legendas |

## Tema Geral
- **Modo:** Dark only (sem modo claro)
- **Estilo:** Premium/Glassmorphism
- **Transições:** `0.3s cubic-bezier(0.4, 0, 0.2, 1)`
