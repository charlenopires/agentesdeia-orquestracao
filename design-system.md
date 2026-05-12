# Design System — Agentes de IA · Paleta Coolors Warm
**Palestra: Orquestração e Aplicabilidade**  
Paleta: [003049 · D62828 · F77F00 · FCBF49 · EAE2B7](https://coolors.co/palette/003049-d62828-f77f00-fcbf49-eae2b7)  
Versão 2.0 · Maio 2026

---

## 1. Filosofia

Sistema editorial claro e quente com base em creme-baunilha e dois accents expressivos — **vermelho imperial** e **laranja** — ancorados num texto **azul prussiano** profundo. Cada cor da paleta tem um papel semântico claro.

---

## 2. Paleta-raiz

| Nome         | Hex       | Papel principal                         |
|--------------|-----------|-----------------------------------------|
| Prussian Blue| `#003049` | Texto primário, headings, fundos escuros |
| Imperial Red | `#D62828` | Accent principal (botões, bordas, destaques) |
| Alloy Orange | `#F77F00` | Accent secundário (ícones, regras, bullets) |
| Amber        | `#FCBF49` | Highlight / badge background / warn bg  |
| Vanilla      | `#EAE2B7` | Base do sistema de fundos               |

---

## 3. Tokens de Cor

### Fundos (`--bg-*`)

| Token         | Hex          | Uso                                         |
|---------------|--------------|---------------------------------------------|
| `--bg`        | `#FDFAF0`    | Fundo raiz (branco-creme muito suave)        |
| `--bg-deep`   | `#F5EDCF`    | Seções mais profundas, rodapé               |
| `--bg-elev`   | `#FFFFFF`    | Cards elevados, pré / code blocks            |
| `--bg-card`   | `#F2EDD4`    | Cards padrão (tint creme)                   |
| `--bg-soft`   | `rgba(234,226,183,0.65)` | Glassmorphism / overlays    |

### Texto (`--fg-*`)

| Token        | Hex       | Uso                              | Contraste bg |
|--------------|-----------|----------------------------------|--------------|
| `--fg`       | `#003049` | Texto primário                   | ≈ 18:1 AAA  |
| `--fg-mute`  | `#1A4A64` | Texto secundário, parágrafos     | ≈ 10:1 AAA  |
| `--fg-dim`   | `#5A8098` | Labels, captions, placeholders   | ≈ 4.5:1 AA  |

### Bordas

| Token          | Hex       | Uso                        |
|----------------|-----------|----------------------------|
| `--border`     | `#C8C0A0` | Bordas de cards e divisores |
| `--border-sub` | `#DDD5B5` | Bordas sutis internas       |

### Accents

| Token            | Hex       | Uso                                        | Contraste |
|------------------|-----------|--------------------------------------------|-----------|
| `--purple`       | `#D62828` | Red accent — botões, bordas, bullets        | 5.1:1 AA |
| `--purple-soft`  | `#E84848` | Red leve — gradientes, hover, tags          | 3.8:1 AA-Large |
| `--purple-deep`  | `#A01818` | Red profundo — estados pressed, sombras     | 8.5:1 AAA |
| `--coral`        | `#F77F00` | Orange — eyebrow, regras, bullets           | decorativo |
| `--coral-soft`   | `#C06000` | Orange escuro — links, código inline        | 4.0:1 AA-Large |

> **Nota**: `--coral` (`#F77F00`) e `#FCBF49` (amber) são muito claros para texto em fundo creme — use-os apenas como decoração, bordas, ou backgrounds com texto `--fg` em cima.

### Status

| Token     | Hex       | Uso                    | Contraste |
|-----------|-----------|------------------------|-----------|
| `--ok`    | `#1A8035` | Sucesso                | 5.8:1 AA |
| `--warn`  | `#C06000` | Atenção (texto/borda)  | 4.0:1 AA-Large |
| `--error` | `#D62828` | Erro                   | 5.1:1 AA |

---

## 4. Tipografia

### Famílias

| Papel   | Família                                    |
|---------|--------------------------------------------|
| Display | **Instrument Serif** (Italic & Roman)      |
| Body    | **IBM Plex Sans** 300/400/500/600/700      |
| Mono    | **JetBrains Mono** 400/500/700             |

### Escala

| Elemento    | Tamanho  | Família | Cor            |
|-------------|---------|---------|----------------|
| h1 (capa)   | 11rem   | Display | gradient animado |
| h2          | 3.8rem  | Display | `--fg`         |
| h3          | 2.5rem  | Display | `--fg`         |
| Parágrafo   | 1.4rem  | Body    | `--fg-mute`    |
| Eyebrow     | 0.85rem | Mono    | `--coral`      |
| List item   | 1.3rem  | Body    | `--fg-mute`    |
| Código      | 0.9em   | Mono    | `--coral-soft` |

---

## 5. Gradiente Animado

```css
background: linear-gradient(270deg, #D62828, #F77F00, #003049, #E84848, #FF9520);
background-size: 400% 400%;
animation: cover-gradient-shift 5s ease infinite;
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

Usado em: `.cover-title-animated`, `.divider h1`

---

## 6. Componentes

### Tags / Badges

```
.tag         → bg: rgba(214,40,40,0.10)  | color: #D62828   | border: rgba(214,40,40,0.40)
.tag-coral   → bg: rgba(247,127,0,0.12)  | color: #C06000   | border: rgba(247,127,0,0.45)
.tag-warn    → bg: rgba(252,191,73,0.22) | color: #8A5000   | border: rgba(252,191,73,0.65)
.tag-ok      → bg: rgba(26,128,53,0.10)  | color: #1A6A30   | border: rgba(26,128,53,0.40)
.tag-error   → bg: rgba(214,40,40,0.10)  | color: #D62828   | border: rgba(214,40,40,0.40)
```

### Cards

```
.card           → bg: --bg-card (#F2EDD4)  |  border: --border
.card-accent    → + left bar 3px --coral (#F77F00)
.card-accent-purple → + left bar 3px --purple (#D62828)
.card-accent-warn   → + left bar 3px --warn (#C06000)
```

### SVG — Átomo de Capa

```
Núcleo (circle r=20): gradiente #004A70 → #003049 (Prussian Blue)
Texto "IA": fill="white" (contraste 18:1 sobre núcleo escuro)
Órbita 1: stroke="#D62828" (red)
Órbita 2: stroke="#F77F00" (orange)
Órbita 3: stroke="#003049" (blue)
Elétrons: #D62828, #F77F00, #FCBF49
```

### SVG — Diagrama MCP (slide 25b)

```
HOST/CLIENT boxes:  bg cream  #F2EDD4 → gradiente EDE4C8
SERVERS boxes:      bg cream  #F2EDD4 → gradiente EDE4C8  | border #D62828
EXTERNAL boxes:     bg blue   #E8F0F8 → gradiente D8E8F4  | border #0A3A6A
Texto HOST/CLIENT:  #003049 / #8A4000 / #C06000
Texto SERVERS:      #A81818 / #C02020
Texto EXTERNAL:     #1A5A8A / #003049
Partículas:         orange #F77F00, blue #003049
```

---

## 7. Logo Institucional (IFPI)

- Posição: canto superior **esquerdo** — `left: clamp(1rem, 2.5vw, 2.5rem)`
- Filtro feColorMatrix: verde original → `#003049`, vermelho original → `#D62828`
- Drop-shadow: `rgba(0,48,73,0.22)`

---

## 8. Acessibilidade

| Texto         | Fundo     | Contraste | WCAG      |
|---------------|-----------|-----------|-----------|
| `#003049`     | `#FDFAF0` | ≈ 18:1    | AAA       |
| `#1A4A64`     | `#FDFAF0` | ≈ 10:1    | AAA       |
| `#D62828`     | `#FDFAF0` | ≈ 5.1:1   | AA        |
| `#C06000`     | `#FDFAF0` | ≈ 4.0:1   | AA-Large  |
| `#8A5000`     | `#FCBF49 bg` | ≈ 5.5:1 | AA      |
| `FCBF49`      | `#FDFAF0` | ≈ 1.8:1   | ❌ só decoração |
| `F77F00`      | `#FDFAF0` | ≈ 2.2:1   | ❌ só decoração |

---

## 9. Uso / Extensão

1. Use tokens `var(--xxx)` para cores — nunca hexadecimais hardcoded.
2. `#FCBF49` e `#F77F00` **nunca como texto** sobre fundo claro — use como background, border ou decoração.
3. Para texto sobre backgrounds amber (#FCBF49): use `#003049` ou `#8A5000`.
4. Gradiente animado: `.cover-title-animated` e `.divider h1`.
5. Núcleos SVG escuros (#003049): texto branco interno mantém contraste máximo.
