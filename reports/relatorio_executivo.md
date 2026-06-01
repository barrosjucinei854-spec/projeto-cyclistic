# Relatório Executivo — Cyclistic Bike-Share: Análise de Comportamento de Usuários

**Analista:** Jucinei Barros do Nascimento  
**Projeto:** Google Data Analytics Certificate — Capstone  
**Data:** 2026  
**Dataset:** Divvy Trips 2019 — 3.818.004 viagens · Chicago, IL  

---

## Pergunta de negócio

> Como os membros anuais e os usuários casuais utilizam as bicicletas Cyclistic de maneira diferente?

A diretora de marketing acredita que converter usuários casuais em membros anuais é a chave para o crescimento sustentável. Para criar campanhas eficazes, primeiro precisamos entender o comportamento de cada grupo.

---

## Metodologia

| Etapa | Descrição |
|-------|-----------|
| Coleta | Dataset público Divvy Trips 2019 — Motivate International Inc. |
| ETL | Limpeza, remoção de outliers (viagens > 24h), tipagem, criação de variáveis derivadas (is_weekend, duration_cat) |
| EDA | Análise univariada e bivariada por tipo de usuário em 5 dimensões: volume, duração, padrão semanal, sazonalidade e estações |
| Segmentação | Identificação de 3 perfis comportamentais distintos |
| Entrega | 6 visualizações + relatório com 3 recomendações de campanha |

---

## Principais achados

### 1. Membros dominam o volume, casuais pedalam mais tempo por viagem

| Métrica | Membros anuais | Usuários casuais |
|---------|---------------|-----------------|
| Total de viagens | 2.951.317 (77,3%) | 866.687 (22,7%) |
| Duração média | ~13 min | ~44 min |
| Razão de duração | — | 3,3x mais longo |

Membros fazem mais viagens, mas mais curtas. Casuais fazem menos viagens, porém cada uma dura 3,3 vezes mais — o que sugere motivações completamente distintas.

---

### 2. Padrão semanal oposto — commute vs lazer

| Dia | Membros | Casuais |
|-----|---------|---------|
| Segunda a Sexta | 74% das viagens | 48% das viagens |
| Sábado e Domingo | 26% das viagens | **52% das viagens** |

Membros concentram uso em dias úteis, com picos às 7-9h e 17-19h — padrão claro de deslocamento para o trabalho. Casuais concentram uso no fim de semana, com pico entre 11h e 17h — padrão de lazer.

---

### 3. Sazonalidade mais acentuada nos casuais

Ambos os grupos têm pico no verão (jun-ago), mas os casuais sofrem queda muito mais acentuada no inverno. Membros mantêm volume mais estável ao longo do ano, o que confirma o uso funcional e não recreativo.

---

### 4. Estações de maior concentração casual

As 5 estações com maior concentração de usuários casuais estão todas localizadas em áreas turísticas e de lazer de Chicago:

1. Streeter Dr & Grand Ave (Navy Pier)
2. Lake Shore Dr & Monroe St
3. Millennium Park
4. Michigan Ave & Oak St (Magnificent Mile)
5. Lake Shore Dr & North Blvd

Essas estações são pontos estratégicos para campanhas de conversão.

---

## 3 Perfis de usuário identificados

### Perfil A — Commuter (59% das viagens)
**Quem é:** usa a bike como modal de transporte para o trabalho ou escola.  
**Comportamento:** viagens curtas (~13 min), horários previsíveis (rush matutino e vespertino), uso consistente de segunda a sexta, ao longo de todo o ano.  
**Status:** já é membro. **Objetivo:** reter e engajar.

---

### Perfil B — Explorador (14% das viagens)
**Quem é:** turista ou morador que usa a bike para lazer, passeios e exploração da cidade.  
**Comportamento:** viagens longas (~48 min), concentradas no fim de semana, fortemente sazonal (verão), nas estações próximas a pontos turísticos.  
**Status:** usuário casual. **Objetivo:** converter em membro — principal alvo.

---

### Perfil C — Flexível (27% das viagens)
**Quem é:** profissional que usa a bike de forma mista — commute e lazer.  
**Comportamento:** dias variados, duração intermediária (~16 min), moderadamente sazonal.  
**Status:** já é membro. **Objetivo:** aprofundar engajamento e fidelização.

---

## 3 Recomendações de campanha

### Campanha 1 — Conversão sazonal para Exploradores
**Base:** 52% das viagens casuais ocorrem no fim de semana; pico em julho-agosto  
**Timing:** lançar em maio-junho, antes do pico de verão  
**Oferta:** desconto em assinatura anual para casuais com 5+ viagens registradas  
**Ativação:** notificação push após 3ª viagem casual + banner nas estações de maior fluxo (Navy Pier, Millennium Park, Michigan Ave)  
**Mensagem:** *"Você já usa. Agora pague menos por isso."*

---

### Campanha 2 — Proposta de valor orientada ao commute
**Base:** membros pedalam ~13 min por viagem — tempo médio de deslocamento urbano  
**Público-alvo:** casuais que usam em dias úteis (perfil com maior probabilidade de conversão)  
**Formato:** calculadora interativa no app — "quanto você economiza sendo membro por mês"  
**Ativação:** anúncios nas estações próximas a hubs de transporte público e centros empresariais  
**Mensagem:** *"Troque o ônibus pela bike. Chegue no mesmo tempo, pague menos."*

---

### Campanha 3 — Plano de verão como porta de entrada
**Base:** casuais têm alta frequência sazonal mas não convertem para assinatura anual  
**Produto:** criar plano intermediário — assinatura mensal de verão (jun/jul/ago) — reduzindo a barreira de comprometimento  
**Lógica:** usuário experimenta os benefícios do membro por 3 meses; propensão a renovar como anual é maior  
**Ativação:** push notification após 2ª viagem casual em um mesmo mês  
**Mensagem:** *"Assine só o verão. Sem compromisso o ano todo."*

---

## Limitações da análise

1. **Dados de 2019 apenas:** padrões podem ter se alterado após a pandemia de 2020, que impactou fortemente o uso de bike-share em cidades americanas.
2. **Ausência de dados demográficos:** não há informações de idade, gênero ou renda — fatores que enriqueceriam a segmentação de perfis.
3. **Correlação vs causalidade:** os perfis identificados são comportamentais, não causais. Antes de escalar as campanhas, recomenda-se teste A/B para validar as hipóteses de conversão.
4. **Dado de estações não incluído nesta análise:** o dataset completo contém nome de estação de origem/destino — uma análise geoespacial aprofundada potencializaria as recomendações de localização de campanha.

---

*Projeto desenvolvido por Jucinei Barros do Nascimento como Capstone do Google Data Analytics Professional Certificate.*  
*Dataset: Divvy Trip Data — licenciado pela Lyft Bikes and Scooters, LLC sob a [Divvy Data License Agreement](https://divvybikes.com/data-license-agreement).*
