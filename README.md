# Agentes de IA — Orquestração e Aplicabilidade

Slides da palestra apresentada na **Universidade Federal do Piauí (UFPI)**, cobrindo arquitetura, padrões de orquestração e aplicabilidade prática de agentes de inteligência artificial.

---

## Visão geral

70 slides construídos com **Reveal.js 5.1.0** (canvas 1280 × 800 px) que percorrem desde os fundamentos conceituais de agentes até decisões arquiteturais avançadas e o protocolo MCP (Model Context Protocol).

---

## Conteúdo

| Parte | Tema |
|-------|------|
| I | O que é um Agente de IA — conceitos e Agent Loop |
| II | Tipos de memória e ferramentas disponíveis |
| III | Padrões de orquestração (ReAct, Plan-and-Execute, Multi-Agent…) |
| IV | Árvore de decisão arquitetural para agentes |
| V | Model Context Protocol (MCP) — arquitetura e casos de uso |
| VI | Aplicabilidade prática e casos reais |
| VII | Encerramento |

---

## Como executar localmente

Pré-requisito: **Python 3** instalado.

```bash
git clone https://github.com/charlenopires/agentesdeia-orquestracao.git
cd agentesdeia-orquestracao
python3 -m http.server 7890
```

Abra no navegador: [http://localhost:7890/orquestracao_aplicabilidade.html](http://localhost:7890/orquestracao_aplicabilidade.html)

### Atalhos do Reveal.js

| Tecla | Ação |
|-------|------|
| `→` / `Space` | Próximo slide |
| `←` | Slide anterior |
| `F` | Tela cheia |
| `S` | Modo apresentador |
| `O` | Visão geral |
| `Esc` | Sair da visão geral |

---

## Stack

- **[Reveal.js 5.1.0](https://revealjs.com/)** — framework de apresentação
- **[Mermaid 10.9.1](https://mermaid.js.org/)** — diagramas declarativos
- **[IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans)** — tipografia body
- **[Instrument Serif](https://fonts.google.com/specimen/Instrument+Serif)** — tipografia display
- **[JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono)** — código e eyebrows
- **SVG animado** — diagramas do Agent Loop e MCP

### Paleta de cores

| Nome | Hex | Papel |
|------|-----|-------|
| Prussian Blue | `#003049` | Texto primário e fundos escuros |
| Imperial Red | `#D62828` | Accent principal |
| Alloy Orange | `#F77F00` | Accent secundário |
| Amber | `#FCBF49` | Highlights e badges |
| Vanilla | `#EAE2B7` | Base dos fundos |

---

## Autor

**Charleno Pires**
Professor · Instituto Federal do Piauí (IFPI)
[charlenopires@ifpi.edu.br](mailto:charlenopires@ifpi.edu.br)

---

## Licença

Material didático de livre uso para fins educacionais, com atribuição.
