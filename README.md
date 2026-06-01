# Cyclistic Bike-Share — Análise de Comportamento de Usuários

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualização-4c72b0)
![Google](https://img.shields.io/badge/Google_Data_Analytics-Capstone-4285F4?logo=google)
![Status](https://img.shields.io/badge/Status-Concluído-1D9E75)

> Projeto Capstone do Google Data Analytics Professional Certificate.  
> Análise de 3,8 milhões de viagens de bike-share em Chicago para identificar diferenças de comportamento entre membros anuais e usuários casuais e gerar recomendações de campanha de conversão.

---

## Pergunta de negócio

**Como os membros anuais e os usuários casuais utilizam as bicicletas Cyclistic de maneira diferente?**

A empresa quer converter usuários casuais em membros anuais. Para isso, precisa entender o comportamento de cada grupo e criar campanhas orientadas por dados.

---

## Principais resultados

| Métrica | Membros anuais | Usuários casuais |
|---------|---------------|-----------------|
| Volume de viagens | **2.951.317** (77,3%) | **866.687** (22,7%) |
| Duração média | **~13 min** | **~44 min** (3,3x maior) |
| Dia de pico | Segunda a sexta | Sábado e domingo |
| Horário de pico | 7-9h e 17-19h | 11h-17h |
| Motivação | Commute (trabalho) | Lazer e turismo |
| Sazonalidade | Estável o ano todo | Fortemente sazonal (verão) |

---

## 3 perfis de usuário identificados

```
┌─────────────────────────────────────────────────────────────────┐
│  PERFIL A — Commuter          59% das viagens   [JÁ É MEMBRO]  │
│  Viagens curtas (~13min) · Dias úteis · Rush matutino/vespertino│
├─────────────────────────────────────────────────────────────────┤
│  PERFIL B — Explorador        14% das viagens   [CASUAL → ALVO]│
│  Viagens longas (~48min) · Fim de semana · Turismo e lazer      │
├─────────────────────────────────────────────────────────────────┤
│  PERFIL C — Flexível          27% das viagens   [JÁ É MEMBRO]  │
│  Uso misto · Dias variados · Duração intermediária (~16min)     │
└─────────────────────────────────────────────────────────────────┘
```

---

## Estrutura do repositório

```
projeto-cyclistic/
│
├── data/
│   └── README_dados.md           # Instruções para baixar o dataset oficial
│
├── notebooks/
│   └── analise_cyclistic.ipynb   # Análise completa: ETL → EDA → Perfis → Recomendações
│
├── reports/
│   ├── relatorio_executivo.md    # Relatório com 3 recomendações de campanha
│   ├── fig_volume_usuarios.png
│   ├── fig_duracao_viagens.png
│   ├── fig_padrao_semanal.png
│   ├── fig_sazonalidade.png
│   ├── fig_duracao_semanal.png
│   ├── fig_3_perfis.png
│   └── fig_painel_comparativo.png
│
├── requirements.txt
└── README.md
```

---

## Como executar

### 1. Baixar o dataset oficial

O dataset Divvy Trips 2019 está disponível publicamente em:  
👉 **https://divvy-tripdata.s3.amazonaws.com/index.html**

Baixe os arquivos trimestrais de 2019 (`Divvy_Trips_2019_Q1.zip` até `Q4`) e salve em `data/`.

> Licenciado pela Lyft Bikes and Scooters, LLC sob a [Divvy Data License Agreement](https://divvybikes.com/data-license-agreement).

### 2. Instalar dependências

```bash
pip install -r requirements.txt
```

### 3. Executar o notebook

```bash
jupyter notebook notebooks/analise_cyclistic.ipynb
```

Ou abra diretamente no **VS Code** com a extensão Jupyter instalada.

---

## Tecnologias utilizadas

| Ferramenta | Uso |
|-----------|-----|
| Python 3.10 | Linguagem principal |
| Pandas | ETL e manipulação de dados |
| NumPy | Operações numéricas |
| Matplotlib | Visualizações customizadas |
| Seaborn | Heatmaps e gráficos estatísticos |
| Jupyter Notebook | Ambiente de análise interativo |

---

## Metodologia

```
Dataset Divvy 2019 (3,8M registros)
          │
          ▼
    [ ETL com Pandas ]
    · Remoção de outliers (viagens > 24h)
    · Criação: is_weekend, duration_cat
    · Tipagem e normalização
          │
          ▼
    [ EDA em 5 dimensões ]
    · Volume por tipo de usuário
    · Duração das viagens
    · Padrão semanal e horário
    · Sazonalidade mensal
    · Duração por dia da semana
          │
          ▼
    [ Segmentação de Perfis ]
    · 3 perfis comportamentais identificados
    · Commuter · Explorador · Flexível
          │
          ▼
    [ Recomendações de Campanha ]
    · 3 estratégias orientadas por dados
    · Timing · Canal · Mensagem · Público
```

---

## Recomendações de campanha (resumo)

**1. Conversão sazonal para Exploradores**  
Campanha em maio-junho antes do pico de verão. Desconto em assinatura anual para casuais com 5+ viagens. Ativar nas estações turísticas (Navy Pier, Millennium Park).

**2. Proposta de valor orientada ao commute**  
Calculadora "quanto você economiza sendo membro" no app. Foco em casuais que já usam em dias úteis — perfil com maior probabilidade de conversão.

**3. Plano de verão como porta de entrada**  
Assinatura mensal de verão (jun-ago) como produto intermediário. Reduz barreira de comprometimento e cria experiência de membro antes da conversão anual.

> Relatório completo com dados, metodologia e limitações em [`reports/relatorio_executivo.md`](reports/relatorio_executivo.md)

---

## Sobre o projeto

Este projeto foi desenvolvido como **Capstone do Google Data Analytics Professional Certificate** (Coursera, 2026), seguindo o framework de análise de dados do programa: Ask → Prepare → Process → Analyze → Share → Act.

---

## Sobre o autor

**Jucinei Barros do Nascimento**  
Analista de Dados em formação · GTI — UNINTER  
Google Data Analytics Professional Certificate · Coursera 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Jucinei_Barros-0A66C2?logo=linkedin)](https://www.linkedin.com/in/jucinei-barros-48b9a43b0/)
[![GitHub](https://img.shields.io/badge/GitHub-barrosjucinei854--spec-181717?logo=github)](https://github.com/barrosjucinei854-spec)

---

*Veja também:* [**Análise de Rotatividade de RH**](https://github.com/barrosjucinei854-spec/projeto-hr-analytics) — análise de 14.999 registros identificando padrões de turnover com Python e Power BI.
