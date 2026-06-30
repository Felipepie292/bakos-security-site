# Bakos Security — CLAUDE.md

## Sobre o Projeto

Site institucional para **Bakos Security** — empresa de segurança e serviços terceirizados com sede em Curitiba, PR.
Projeto é **HTML/CSS/JS puro** (arquivo único `index.html`), single-page com navegação por âncoras.

---

## Arquivos do Projeto

- **`bakos-v3.html`** — template base com estrutura, CSS e JS prontos (sem conteúdo real, só placeholders)
- **`conteudo_bakos.md`** — todo o conteúdo textual extraído do site atual (bakos-security.com.br)
- **`index.html`** — arquivo de trabalho final (derivado do v3 com conteúdo real)

---

## Stack

- **HTML estático** — arquivo único `index.html`
- **Tailwind não usado** — CSS vanilla no `<style>` do próprio arquivo
- **Vanilla JavaScript** inline para animações, menu mobile, scroll observer
- **Google Fonts** — Outfit (300–900)
- **Sem frameworks JS**

---

## Design System

### Paleta
- **Fundo escuro:** `#0c0c0c` / `#141414` / `#1e1e1e`
- **Fundo claro (off-white):** `#f5f4f0` / `#eeece6` — usar em seções alternadas
- **Accent amarelo:** `#f5c400` (amarelo vivo da identidade Bakos — usar em detalhes, labels, ícones, bordas)
- **Accent dourado (template base):** `#c9a96e` — manter em elementos secundários
- **Texto claro:** `#ffffff` / `#888` (muted)
- **Texto escuro (sobre off-white):** `#111111` / `#444`

### Tipografia
- **Fonte:** Outfit (Google Fonts)
- **Títulos:** weight 800, letter-spacing −0.02em
- **Labels/tags:** weight 500–600, letter-spacing 0.16–0.18em, uppercase

### Estética
- Sem border-radius (cantos retos)
- Grid com `gap:2px` + `background:var(--border)` cria divisórias entre cards
- Animações de entrada: fade-up (`.rv`), line reveal (`.rl`), char reveal (`.chars-hidden`), curtain wipe (`.curtain`)

---

## Estrutura de Seções (ordem no HTML)

1. **Nav** — logo, links âncora, CTA "Orçamento", burger mobile
2. **Hero** — headline forte + subtítulo + CTA → foto hero
3. **Clientes (esteira)** — marquee infinito logo abaixo do hero, fundo escuro com borda. Por ora nomes em texto; substituir por logos quando disponíveis. ID: `#clientes`
4. **Trust / Sobre** — grid 2 colunas: fotos equipe + texto com diferenciais em checkboxes
5. **Serviços** — fundo off-white, grid 2x2 de cards com foto
6. **Nossa História / Sobre** — fundo escuro, texto 2 colunas + foto (`quemsomos.jpeg`)
7. **Diferenciais** — fundo off-white, 4 cards numerados
8. **Eventos** — fundo escuro, accordion 5 itens
9. **Especializados** — fundo escuro, 2 colunas: Cursos e Treinamentos + Investigação e Inteligência
10. **Contato** — fundo off-white, grid: info contato + formulário
11. **Footer** — fundo escuro

> Regra de alternância: seções escuras e off-white se alternam para criar ritmo visual.

---

## Conteúdo Real (resumo)

**Identidade:**
- Nome: Bakos Security | Tagline: Segurança e Serviços
- WhatsApp: (41) 99744-4276
- Cidade: Curitiba, PR

**Serviços principais (3):**
- Portaria 24 horas
- Segurança Patrimonial (Controle de Acesso e Vigia)
- Limpeza e Conservação

**Eventos (5 sub-serviços):**
- Suporte para Eventos, Recepção, Limpeza, Controle de Acesso, Estacionamento/Manobrista

**Vantagens recorrentes (usar como diferenciais):**
1. Redução de custos vs. contratação direta
2. Equipe treinada e preparada
3. Gestão de pessoal terceirizada
4. Substituição rápida em ausências

**Conteúdo completo:** ver `conteudo_bakos.md`

---

## Imagens (a gerar com IA)

Placeholders (`.ph`) marcam onde vão as fotos. Não remover os placeholders — apenas substituir pelo `<img>` quando as fotos chegarem.

- `foto-hero.jpg` — profissional de segurança, retrato, fundo escuro, ~800×1080px
- `foto-equipe-1.jpg` — equipe em operação, ~600×400px
- `foto-equipe-2.jpg` — detalhe operacional, ~300×170px
- `foto-equipe-3.jpg` — detalhe operacional, ~300×170px
- `foto-sobre.jpg` — equipe/operação, ~580×460px
- `foto-servico-portaria.jpg` — portaria/recepção, ~400×280px
- `foto-servico-seguranca.jpg` — segurança patrimonial, ~400×280px
- `foto-servico-limpeza.jpg` — limpeza profissional, ~400×280px
- `foto-evento.jpg` — equipe em evento, ~400×280px

---

## Responsividade

- **≤1024px:** serv-grid 2 colunas, foot-top 2 colunas
- **≤800px:** hero 1 coluna, trust/story/contact grids 1 coluna, why-grid 1 coluna
- **≤620px:** nav links ocultos → burger ativo, serv-grid 1 coluna, foot-top 1 coluna

---

## Regras

1. Arquivo único `index.html` — não criar arquivos separados de CSS ou JS.
2. Manter sistema de animações do template base (`.rv`, `.rl`, `.curtain`, `.chars-hidden`).
3. Amarelo `#f5c400` apenas em detalhes (labels, ícones de check, bordas de destaque) — nunca como fundo de seção inteira.
4. Seções off-white usam texto escuro (`#111`, `#444`) — ajustar contraste.
5. Não inventar informações sobre a empresa — só usar o que está em `conteudo_bakos.md`.
6. Ao adicionar seções ou mudar estrutura, atualizar este arquivo.
