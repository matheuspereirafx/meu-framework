---
name: pesquisa-mercado
description: >
  Pesquisa de mercado completa. Cobre concorrentes diretos e indiretos com análise de funcionalidades e preços,
  Grade ERRC (Oceano Azul), TAM/SAM/SOM com memória de cálculo, persona detalhada, Não-Clientes em 3 níveis
  e Benchmarks Financeiros do setor (Churn, CAC, LTV, Payback, MRR/ARR, margens).
  Gera output .md, .docx geral e .docx financeiro separado. Chamada automaticamente pelo Agente Ideia na Fase 0F e na Fase 1A.
---

# Skill — Pesquisa de Mercado

## Objetivo

Realizar pesquisa de mercado estruturada sobre a solução descrita, cobrindo:

1. Concorrentes diretos — funcionalidades e preços
2. Concorrentes indiretos — soluções alternativas
3. Grade ERRC (Estratégia Oceano Azul)
4. Tamanho de mercado — TAM / SAM / SOM com memória de cálculo
5. Persona detalhada baseada em dados reais
6. Não-Clientes — 3 níveis
7. **Benchmarks Financeiros do setor** ← nova seção

---

## Ativação

Quando chamada sem contexto, pergunte:
> "Qual é a ideia ou solução que devo pesquisar? Descreva em 1–3 frases e, se possível, informe o país/região-alvo."

Se chamada pelo Agente Ideia, use o contexto disponível (Causa Raiz + JTBD + Veredito) diretamente, sem perguntar.

---

## Execução da Pesquisa

### Etapa 1 — Concorrentes Diretos

Pesquise soluções que resolvem **exatamente** o mesmo problema.

Queries sugeridas:
- `"[solução] alternatives [ano]"`
- `"[problema] best tools [ano]"`
- `"[nicho] software comparison"`
- `"[solução] vs [concorrente] reddit"`

Para cada concorrente, mapeie:

| # | Concorrente | Plataforma | Modelo de Negócio | Preço (mensal) | Principais Funcionalidades | Avaliação | Usuários estimados |
|---|-------------|-----------|-------------------|---------------|---------------------------|-----------|-------------------|
| 1 | ... | Web / Mobile / Desktop | Freemium / SaaS / Licença | R$ / US$ ... | [F1], [F2], [F3] | x/5 | ... |
| 2 | ... | | | | | | |
| 3 | ... | | | | | | |

**Ticket médio do mercado:**
```
Ticket médio = média simples dos preços dos planos pagos encontrados
Cálculo: (R$X + R$Y + R$Z) / N concorrentes = R$ [valor]
```

---

### Etapa 2 — Concorrentes Indiretos

Soluções que resolvem o problema de forma diferente: planilhas, processos manuais, ferramentas adjacentes.

| Solução Indireta | Como resolve o problema | Limitação principal |
|-----------------|------------------------|-------------------|
| Planilha Excel / Google Sheets | ... | ... |
| Processo manual / papel | ... | ... |
| Ferramenta adjacente | ... | ... |

---

### Etapa 3 — Grade ERRC (Oceano Azul)

A Grade ERRC identifica como diferenciar a solução criando um espaço de mercado sem concorrência direta.

| Ação | Fatores | Justificativa |
|:-----|:--------|:-------------|
| **ELIMINAR** ✂️ | [Fator que o setor oferece mas não gera valor real] | Por que eliminar? |
| **REDUZIR** ↓ | [Fator presente nos concorrentes mas que pode ser simplificado] | Abaixo de qual nível? |
| **AUMENTAR** ↑ | [Fator existente mas aquém do que o cliente precisa] | Aumentar até onde? |
| **CRIAR** ✨ | [Fator inexistente no setor que cria novo valor] | Que valor novo gera? |

**Curva de Valor Resultante:**
> Descreva em 2–3 linhas como a combinação ERRC cria uma proposta de valor diferente de todos os concorrentes mapeados.

---

### Etapa 4 — Tamanho de Mercado (TAM / SAM / SOM)

Use o **ticket médio real** calculado na Etapa 1 como base de todos os cálculos.

Queries sugeridas:
- `"[nicho] market size [ano]"`
- `"[nicho] total addressable market report"`
- `"[nicho] number of users worldwide"`
- `"[país] [nicho] industry revenue"`

#### TAM — Total Addressable Market
```
TAM = total de pessoas/empresas com o problema × ticket médio anual
Memória de cálculo:
  Universo do problema: [N] pessoas/empresas
  × Ticket médio anual: R$ [valor/mês × 12]
  = TAM: R$ [valor total]
Fonte do universo: [link ou referência]
```

#### SAM — Serviceable Addressable Market
```
SAM = TAM × % segmentável pelo modelo de negócio e geografia
Memória de cálculo:
  TAM: R$ [valor]
  × % geograficamente atingível: [X%] → [critério: país, idioma, região]
  × % atingível pelo canal de distribuição: [Y%] → [critério: digital, B2B, etc.]
  = SAM: R$ [valor]
```

#### SOM — Serviceable Obtainable Market
```
SOM = SAM × % realista de market share nos primeiros 24 meses
Memória de cálculo:
  SAM: R$ [valor]
  × Market share conservador: [0,5% a 5%] → justificativa: [nível de competitividade]
  = SOM: R$ [valor]
Referência de benchmark: [concorrente similar em estágio inicial]
```

| Mercado | Valor (R$) | Premissa central | Fonte |
|---------|-----------|-----------------|-------|
| TAM | R$ ... | ... | ... |
| SAM | R$ ... | ... | ... |
| SOM | R$ ... | ... | ... |

**Ticket médio usado como base:** R$ [valor] / mês

---

### Etapa 5 — Persona

Com base nos reviews dos concorrentes, perfis de usuários e contexto do Agente Ideia.

**Nome fictício:** [Nome Sobrenome]
**Idade:** [X anos] | **Profissão:** [Cargo] | **Onde mora:** [Cidade] | **Renda:** [Faixa]

**Contexto:** _[Parágrafo de 3–4 linhas descrevendo dia a dia e como o problema aparece na rotina.]_

**Dores específicas:**
- [Dor 1 — extraída de reviews reais]
- [Dor 2 — frustração recorrente]
- [Dor 3 — consequência não-óbvia]

**Comportamento digital:**
- Redes: [lista] | Formato: [vídeos/artigos/podcasts] | Dispositivo: [Mobile/Desktop] | Frequência: [Diário/Semanal]

**O que usa hoje:** [Solução 1] — insuficiente porque [razão]. [Solução 2] — insuficiente porque [razão].

**Frase:** > _"[Frase em primeira pessoa extraída de review real se possível]"_

---

### Etapa 6 — Não-Clientes: 3 Níveis (Oceano Azul)

#### Nível 1 — À Beira do Mercado ("Soon-to-be")
- **Quem são:** [Perfil] | **Por que ainda usam:** [Razão] | **Gatilho de troca:** [O que os faria migrar]

#### Nível 2 — Recusando o Mercado ("Refusing")
- **Quem são:** [Perfil] | **Por que recusam:** [Barreira] | **Condição de adoção:** [O que precisariam ver]

#### Nível 3 — Inexplorados ("Unexplored")
- **Quem são:** [Perfil] | **Por que invisíveis:** [Razão estrutural] | **Como alcançar:** [Estratégia]

---

### Etapa 7 — Benchmarks Financeiros do Setor ← NOVA SEÇÃO

**Objetivo:** Coletar dados financeiros reais do setor para que o Agente Financeiro tenha benchmarks confiáveis de churn, CAC, LTV, payback e margens — em vez de partir do zero.

Queries sugeridas para cada métrica:

```
Churn:       "[nicho] SaaS average churn rate [ano]"
             "[nicho] customer retention rate benchmark"
             "monthly churn [setor] startups"

CAC:         "[nicho] customer acquisition cost benchmark"
             "[nicho] SaaS CAC average"
             "how much does [concorrente] spend on customer acquisition"

LTV:         "[nicho] lifetime value benchmark"
             "[nicho] SaaS LTV average"
             "LTV CAC ratio [setor]"

Payback:     "[nicho] payback period SaaS"
             "[nicho] months to recover CAC"

MRR/ARR:     "[concorrente] MRR ARR revenue [ano]"
             "[nicho] SaaS revenue benchmarks"
             "[concorrente] annual recurring revenue"

Margens:     "[nicho] SaaS gross margin benchmark"
             "[nicho] net revenue retention"
             "[nicho] EBITDA margin"
```

Para cada métrica, busque:
1. O valor médio do setor (benchmark de mercado)
2. O valor dos concorrentes diretos identificados (se disponível publicamente)
3. A faixa saudável para o modelo de negócio (referência: SaaS benchmarks, OpenView, KeyBanc, Bessemer)

---

#### 7.1 — Churn Rate

O **churn** mede a taxa de cancelamento/perda de clientes em um período.

| Tipo | Definição | Benchmark do setor | Fonte |
|:-----|:----------|:-----------------:|:-----:|
| **Monthly Churn** | % de clientes que cancelam por mês | [X%] | [fonte] |
| **Annual Churn** | % de clientes que cancelam por ano | [X%] | [fonte] |
| **Revenue Churn** | % da receita perdida por mês | [X%] | [fonte] |
| **Net Revenue Retention (NRR)** | Expansão compensa cancelamentos? | [X%] | [fonte] |

**Referências saudáveis por segmento:**
- SMB (pequenas empresas): monthly churn entre 3–7% é típico; acima de 10% é sinal de alerta.
- Mid-market: monthly churn entre 1–3%.
- Enterprise: annual churn abaixo de 5%.
- NRR acima de 100% significa que expansão supera cancelamentos — ideal.

**Churn dos concorrentes identificados:**

| Concorrente | Churn estimado | Base da estimativa |
|:------------|:--------------:|:------------------|
| [Concorrente A] | [X%/mês] | [review, relatório público, estimativa] |
| [Concorrente B] | [X%/mês] | ... |

**Implicação para o negócio:**
> _O que o churn do setor significa para o modelo: quanto tempo para um cliente se pagar? Com esse churn, qual a vida útil média do cliente?_

---

#### 7.2 — CAC (Customer Acquisition Cost)

O **CAC** é o custo total para adquirir um novo cliente pagante.

```
CAC = Total gasto em vendas + marketing no período
      ───────────────────────────────────────────
      Número de novos clientes adquiridos no mesmo período
```

| Canal | CAC estimado do setor | Fonte |
|:------|:--------------------:|:-----:|
| Orgânico / SEO | R$ [valor] | [fonte] |
| Paid (Google/Meta Ads) | R$ [valor] | [fonte] |
| Indicação / Viral | R$ [valor] | [fonte] |
| Vendas outbound | R$ [valor] | [fonte] |

**CAC dos concorrentes (se disponível):**

| Concorrente | CAC estimado | Canal principal | Fonte |
|:------------|:-----------:|:---------------|:-----:|
| [A] | R$ [valor] | [canal] | [fonte] |
| [B] | R$ [valor] | [canal] | [fonte] |

**Benchmarks de referência:**
- CAC/LTV ratio saudável: LTV deve ser pelo menos 3× o CAC.
- CAC payback abaixo de 12 meses é considerado saudável para SaaS.

---

#### 7.3 — LTV (Lifetime Value)

O **LTV** é a receita total esperada de um cliente durante toda a relação.

```
LTV (simplificado) = Ticket médio mensal × Vida útil média do cliente (meses)
                   = Ticket médio mensal ÷ Churn rate mensal

Memória de cálculo com benchmarks do setor:
  Ticket médio: R$ [valor] / mês
  Churn mensal do setor: [X%]
  Vida útil média: 1 ÷ [X%] = [N] meses
  LTV = R$ [ticket] × [N] meses = R$ [LTV]
```

**LTV estimado com dados do setor:**

| Cenário | Churn/mês | Vida útil | LTV |
|:--------|:---------:|:---------:|:---:|
| Pessimista | [X%] | [N] meses | R$ [valor] |
| Realista (benchmark) | [X%] | [N] meses | R$ [valor] |
| Otimista | [X%] | [N] meses | R$ [valor] |

**Ratio LTV/CAC estimado:**
| Cenário | LTV | CAC estimado | LTV/CAC | Avaliação |
|:--------|:---:|:------------:|:-------:|:---------:|
| Pessimista | R$ | R$ | [X]x | 🔴 / 🟡 / 🟢 |
| Realista | R$ | R$ | [X]x | |
| Otimista | R$ | R$ | [X]x | |

> Referência: LTV/CAC < 1x = negócio insustentável. 1–3x = viável mas apertado. > 3x = saudável. > 5x = escala.

---

#### 7.4 — Payback Period

Tempo necessário para recuperar o custo de aquisição de um cliente.

```
Payback (meses) = CAC ÷ Receita mensal por cliente (descontando COGS)

Memória de cálculo:
  CAC estimado: R$ [valor]
  Ticket médio mensal: R$ [valor]
  Margem bruta estimada: [X%]
  Receita líquida por cliente/mês: R$ [ticket] × [margem] = R$ [valor]
  Payback = R$ [CAC] ÷ R$ [receita líquida] = [N] meses
```

**Payback dos concorrentes / setor:**

| Referência | Payback estimado | Fonte |
|:-----------|:----------------:|:-----:|
| Benchmark do setor | [N] meses | [fonte] |
| [Concorrente A] | [N] meses | [estimativa] |

**Referência saudável:** Payback abaixo de 12 meses para SaaS SMB. Abaixo de 18 meses para mid-market.

---

#### 7.5 — MRR / ARR dos Concorrentes

**MRR** (Monthly Recurring Revenue) e **ARR** (Annual Recurring Revenue) revelam o tamanho real dos competidores.

Queries: `"[concorrente] MRR revenue [ano]"`, `"[concorrente] ARR funding"`, `"[concorrente] crunchbase revenue"`

| Concorrente | MRR estimado | ARR estimado | Estágio | Usuários | Fonte |
|:------------|:-----------:|:-----------:|:-------:|:--------:|:-----:|
| [A] | R$ [valor] | R$ [valor] | Seed/Series A/B... | [N] | [fonte] |
| [B] | R$ [valor] | R$ [valor] | ... | [N] | [fonte] |

**Crescimento MoM (Month-over-Month) do setor:**
> Qual a taxa de crescimento mensal típica para startups neste nicho em estágio inicial? [X% MoM]

---

#### 7.6 — Margens e Estrutura de Custos do Setor

| Métrica | Benchmark do setor | Referência saudável | Fonte |
|:--------|:-----------------:|:-------------------:|:-----:|
| **Gross Margin (Margem Bruta)** | [X%] | > 60–70% para SaaS | [fonte] |
| **COGS como % da receita** | [X%] | < 30–40% | [fonte] |
| **Custo de infraestrutura/usuário** | R$ [valor] | Depende do modelo | [fonte] |
| **Custo de suporte/usuário** | R$ [valor] | [referência] | [fonte] |
| **EBITDA margin (estágio inicial)** | [X%] | Negativo é normal; positivo após [N] anos | [fonte] |

---

#### 7.7 — Síntese Financeira do Setor

Com base em todos os dados coletados, apresente o **quadro-síntese de saúde financeira do mercado**:

| Indicador | Benchmark do setor | O que significa para o negócio |
|:----------|:-----------------:|:-------------------------------|
| Monthly Churn | [X%] | Vida útil média do cliente: [N] meses |
| CAC | R$ [valor] | Recuperável em [N] meses com ticket atual |
| LTV | R$ [valor] | LTV/CAC = [X]x — [avaliação] |
| Payback | [N] meses | [viável / atenção / crítico] |
| Gross Margin | [X%] | [impacto na escalabilidade] |
| NRR | [X%] | [expansão compensa churn? sim/não] |
| ARR médio (concorrentes) | R$ [valor] | [referência de tamanho do mercado] |

**Veredito financeiro do setor:**
> _Em 3–5 linhas: o setor tem margens que permitem escala? O churn típico compromete o LTV? O CAC é recuperável com o ticket médio praticado? Vale a pena competir aqui financeiramente?_

---

## OUTPUT

### Output 1 — pesquisa-mercado.md

```markdown
# Pesquisa de Mercado — [Nome da Ideia / Solução]
_Gerado pela Skill pesquisa-mercado · [DATA]_

## 1. Concorrentes Diretos
[tabela]
**Ticket médio do mercado:** R$ [valor]/mês

## 2. Concorrentes Indiretos
[tabela]

## 3. Grade ERRC — Oceano Azul
[tabela]
**Curva de Valor:** [síntese]

## 4. TAM / SAM / SOM
[tabela com memória de cálculo]

## 5. Persona
[ficha completa]

## 6. Não-Clientes — 3 Níveis
[3 níveis]

## 7. Benchmarks Financeiros do Setor
### 7.1 Churn Rate
[tabelas de benchmark + concorrentes + implicação]

### 7.2 CAC
[tabelas por canal + concorrentes]

### 7.3 LTV e LTV/CAC
[cálculo com memória + 3 cenários + ratio]

### 7.4 Payback Period
[cálculo com memória + benchmark]

### 7.5 MRR/ARR dos Concorrentes
[tabela]

### 7.6 Margens
[tabela]

### 7.7 Síntese Financeira
[quadro-síntese + veredito]

## Conclusão Geral
[Síntese integrada: mercado real? gap principal? financeiramente viável? não-clientes revelam expansão? vale construir?]

---
_Pronto para o Agente Planejamento e Agente Financeiro_
```

---

### Output 2 — pesquisa-mercado.docx

Documento Word completo com todas as 7 seções, capa, sumário automático, tabelas formatadas, ERRC colorida por ação e cards de Não-Clientes.

---

### Output 3 — benchmarks-financeiros.md ← NOVO

```markdown
# Benchmarks Financeiros — [Nome do Setor / Nicho]
_Gerado pela Skill pesquisa-mercado · Seção 7 · [DATA]_

---

## Resumo Executivo

| Indicador | Benchmark do Setor | Avaliação |
|:----------|:-----------------:|:---------:|
| Monthly Churn | [X%] | 🟢 / 🟡 / 🔴 |
| Annual Churn | [X%] | |
| NRR | [X%] | |
| CAC (canal principal) | R$ [valor] | |
| LTV | R$ [valor] | |
| LTV/CAC | [X]x | |
| Payback | [N] meses | |
| Gross Margin | [X%] | |

**Veredito financeiro:** [🟢 Saudável / 🟡 Atenção / 🔴 Estruturalmente difícil]

---

## Churn Rate
[detalhamento completo da 7.1]

## CAC por Canal
[detalhamento completo da 7.2]

## LTV e Cenários
[detalhamento completo da 7.3]

## Payback Period
[detalhamento completo da 7.4]

## MRR/ARR dos Concorrentes
[detalhamento completo da 7.5]

## Margens do Setor
[detalhamento completo da 7.6]

## Síntese e Implicações Estratégicas
[detalhamento completo da 7.7]

---
_Pronto para o Agente Financeiro_
```

---

### Output 4 — benchmarks-financeiros.docx ← NOVO

Documento Word focado exclusivamente nos dados financeiros, formatado para apresentação a investidores ou parceiros, com:
- Capa com nome do setor, data e subtítulo "Benchmarks Financeiros do Mercado"
- Resumo executivo na primeira página com quadro-síntese e veredito destacado
- Seção de Churn com tabelas de benchmark + concorrentes + gráfico de vida útil estimada
- Seção de CAC com tabela por canal
- Seção de LTV com os 3 cenários (pessimista / realista / otimista) e ratio LTV/CAC
- Seção de Payback com memória de cálculo
- Seção de MRR/ARR dos concorrentes
- Seção de Margens
- Veredito financeiro final em destaque (box colorido)
- Rodapé com nome do documento, data e número de página

---

Ao finalizar:
> "✅ 4 outputs gerados: pesquisa-mercado.md, pesquisa-mercado.docx, benchmarks-financeiros.md e benchmarks-financeiros.docx. Retornando ao Agente Ideia."
