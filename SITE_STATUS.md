# Econs UFJF — Status do Site
> Atualizado em agosto de 2026

## Repositório e publicação

| Item | Valor |
|---|---|
| Repositório | `github.com/econsufjf/econs_site` |
| URL pública | `econsufjf.github.io` |
| Publicar | `documentacao_interna\gerenciar_repos.bat` → opção [3] Publicar econs_site |
| Atualizar (outro PC) | `documentacao_interna\gerenciar_repos.bat` → opção [1] Atualizar todos |

---

## Estrutura de pastas

```
D:\0_Github\econs_site\
├── index.html                          ← página principal do site
├── atualizar.bat                       ← git pull
├── publicar.bat                        ← git add + commit + push
├── econsdados\
│   └── index.html                      ← página EconsDados (catálogo de bases)
└── observatorios\
    ├── mercado_de_trabalho\
    │   └── [142 htmls por município]   ← gerados por roda_html.R
    └── indicadores_mercado_de_trabalho\
        ├── index.html                  ← entrada do painel PNADC
        ├── desemprego.html
        ├── ocupacao.html
        ├── participacao.html
        ├── subutilizacao.html
        ├── taxa_ocupacao.html
        ├── nivel_desocupacao.html
        ├── combinada_desocup_ftpotencial.html
        ├── combinada_desocup_subocup.html
        └── libs\                       ← JS/CSS compartilhado dos painéis PNADC
```

---

## Seções do index.html

| ID | Título | Status |
|---|---|---|
| `#hero` | Hero com logo + PNIPE | ✅ completo |
| `#sobre` | Sobre o laboratório | ✅ texto real |
| `#pesquisa` | Pesquisa | ⬜ só cabeçalho |
| `#econsdados` | EconsDados | ✅ completo |
| `#observatorio` | Observatórios (2 cards) | ✅ completo |
| `#publicacoes` | Publicações | ⬜ só cabeçalho |
| `#membros` | Membros | ✅ 3 membros reais |
| `#noticias` | Notícias | ⬜ só cabeçalho |
| `#oportunidades` | Oportunidades | ⬜ só cabeçalho |
| `#contato` | Contato | ✅ dados reais |

---

## Design

- **Paleta:** navy `#0f1f3d`, blue `#1e4a8a`, gold `#c9a84c`, cream `#f7f5f0`
- **Fontes:** Playfair Display (títulos) · DM Sans (corpo) · DM Mono (labels/mono)
- **Navbar:** fixo, fundo navy, borda dourada — links em maiúsculas pequenas
- **"Observatórios" no navbar:** submenu dropdown com os dois observatórios
- **Observatórios:** abrem em nova aba (`target="_blank"`)

---

## Membros cadastrados

- Prof. Dr. Ricardo Freguglia
- Dr. Igor Procópio
- Profa. Dra. Flávia Chein

---

## Contato

- E-mail: `lab.econs@ufjf.br`
- Telefone: `(32) 2102-3541`
- Endereço: Faculdade de Economia, UFJF — Campus Universitário, Juiz de Fora MG

---

## Credencial institucional (Hero)

- PNIPE · MCTI — link: `pnipe.mcti.gov.br/laboratory/43813`

---

## Repositório EconsDados (separado)

```
D:\0_Github\econsdados\
├── README.md
├── _template_base.md
├── assets\
│   └── wordmark.svg
├── educacao\
│   └── saeb\
└── saude\
    ├── sinasc\
    └── sihsus\
```

- Repositório: `github.com/econsufjf/econsdados`
- Bases disponíveis: SAEB ✅, SINASC ✅, SIHSUS 🔄, RAIS 🔄, CAGED 🔄, PNADC 🔄
- PNADC listada no catálogo (`econsdados/index.html`) em dois blocos: Mercado de Trabalho (com link "Ver em IBGE") e IBGE (fonte canônica) — documentação técnica pública ainda pendente

---

## Observatório Zona da Mata — geração dos HTMLs

- Script: `F:\Projeto Mercado de Trabalho\2 - Dashboard\roda_html.R`
- `DIR_OUT` aponta para: `D:/0_Github/econs_site/observatorios/mercado_de_trabalho`
- Fonte dos dashboards PNADC: `F:\Projeto PNADC\R\dashboard_dividido\`

---

## Pendências conhecidas

- Seções Pesquisa, Publicações, Notícias e Oportunidades estão em branco (só cabeçalho) — a preencher quando houver conteúdo real
- Seção "Pesquisadores Associados e Pós-Graduação" em Membros está vazia
