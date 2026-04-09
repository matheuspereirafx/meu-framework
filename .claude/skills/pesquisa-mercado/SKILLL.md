---
name: pesquisa-mercado
description: Pesquisa de mercado completa. Cobre concorrentes diretos e indiretos, reviews negativos (gaps), TAM/SAM/SOM com ticket médio real do mercado, persona detalhada e tendências. Chamada automaticamente pelo Agente Ideia na Fase 1A.
---

# Skill — Pesquisa de Mercado

## Objetivo
Realizar pesquisa de mercado completa sobre a ideia descrita, cobrindo:
1. Concorrentes diretos e indiretos
2. Reviews negativos — gaps do mercado
3. TAM/SAM/SOM com ticket médio real dos concorrentes
4. Persona detalhada baseada em dados reais
5. Tendências do setor

---

## Ativação

Quando chamada sem contexto, pergunte:
> "Qual é a ideia ou solução que devo pesquisar? Descreva em 1-3 frases."

Se chamada pelo Agente Ideia, use o contexto disponível diretamente sem perguntar.

---

## Execução da Pesquisa

### Etapa 1 — Concorrentes Diretos

Pesquise na web soluções que resolvem **exatamente** o mesmo problema.

Queries sugeridas:
- "[solução] app alternatives"
- "[problema] best tools [ano]"
- "[nicho] software comparison"
- "[solução] vs [concorrente]"

Para cada concorrente, mapeie:

| Concorrente | Plataforma | Modelo | Preço | Avaliação | Usuários |
|-------------|-----------|--------|-------|-----------|----------|
| ... | ... | ... | R$/US$ ... | .../5 | ... |

Calcule o **ticket médio do mercado**:
```
Ticket médio = média dos preços dos concorrentes diretos encontrados
```

---

### Etapa 2 — Concorrentes Indiretos

Pesquise soluções que resolvem o problema de forma diferente (planilhas, métodos manuais, soluções adjacentes).

| Solução Indireta | Como resolve | Limitação principal |
|-----------------|-------------|-------------------|
| ... | ... | ... |

---

### Etapa 3 — Reviews Negativos (Gap Analysis)

Pesquise reviews negativos (1-3 estrelas) dos principais concorrentes.

Queries sugeridas:
- "[concorrente] negative reviews reddit"
- "[concorrente] complaints"
- "[concorrente] 1 star review app store"
- "site:reddit.com [nicho] problems"

Identifique padrões de reclamação mais frequentes:

| Reclamação | Frequência | Concorrentes afetados |
|------------|-----------|----------------------|
| ... | Alta/Média/Baixa | ... |

**Top 3 Gaps — problemas não resolvidos por nenhum concorrente:**
1. [Gap mais relevante]
2. [Segundo gap]
3. [Terceiro gap]

---

### Etapa 4 — TAM / SAM / SOM

Use o **ticket médio real** calculado na Etapa 1 como base.

Queries sugeridas:
- "[nicho] market size [ano]"
- "[nicho] TAM report"
- "[nicho] total users worldwide"
- "[nicho] industry revenue"

**TAM — Total Addressable Market**
```
TAM = total de pessoas com o problema × ticket médio anual do mercado
Base: [fonte ou estimativa]
```

**SAM — Serviceable Addressable Market**
```
SAM = TAM × % atingível pelo modelo e geografia
Base: [critérios de segmentação]
```

**SOM — Serviceable Obtainable Market**
```
SOM = SAM × % realista de market share nos primeiros 2 anos
Referência: 0,5% a 5% dependendo da competitividade
```

Para cada valor, mostre a base de cálculo explícita e a fonte.

---

### Etapa 5 — Persona

Com base nos reviews, perfil de usuários dos concorrentes e `output/ideia.md`, construa a persona principal.

Queries sugeridas:
- "[nicho] user profile reddit"
- "who uses [concorrente]"
- "[nicho] target audience"
- "[problema] forum complaints"

Monte a persona com dados reais sempre que possível:

**Nome fictício:** [nome + sobrenome brasileiro]
**Idade:** [faixa etária — ex: 28 anos]
**Profissão:** [ocupação típica do usuário]
**Onde mora:** [cidade/região típica]

**Dores específicas:**
- [Dor 1 — extraída dos reviews e ideia.md]
- [Dor 2 — comportamento observado nos reviews]
- [Dor 3 — frustração recorrente]

**Comportamento digital:**
- Redes que usa: [Instagram, TikTok, YouTube, LinkedIn...]
- Como consome conteúdo: [vídeos curtos, artigos, podcasts...]
- Dispositivo principal: [mobile / desktop]
- Frequência de uso de apps similares: [diário / semanal / mensal]

**O que usa hoje para resolver o problema:**
- [Solução 1 com por que é insuficiente]
- [Solução 2 com por que é insuficiente]

**Frase que ela diria sobre o problema:**
> "[Frase em primeira pessoa, coloquial, que resume a frustração — extraída de review real se possível]"

---

### Etapa 6 — Tendências

Pesquise tendências relevantes para o mercado.

Queries sugeridas:
- "[nicho] trends [ano]"
- "[tecnologia] growing market"
- "[nicho] future report"

Mapeie:
- Crescimento do setor (YoY se disponível)
- Tecnologias emergentes que impactam o mercado
- Mudanças de comportamento do consumidor
- Regulações relevantes

---

## OUTPUT

Salve como `output/pesquisa-mercado.md`:

```markdown
# Pesquisa de Mercado — [Nome da Ideia]
_Gerado pela Skill pesquisa-mercado_

## Concorrentes Diretos
| Concorrente | Plataforma | Modelo | Preço | Avaliação | Usuários |
|-------------|-----------|--------|-------|-----------|----------|
| ... | ... | ... | ... | ... | ... |

**Ticket médio do mercado:** R$ [valor]

## Concorrentes Indiretos
| Solução | Como resolve | Limitação |
|---------|-------------|-----------|
| ... | ... | ... |

## Gap Analysis
| Reclamação | Frequência | Concorrentes afetados |
|------------|-----------|----------------------|
| ... | ... | ... |

### Top 3 Gaps
1. [Gap 1]
2. [Gap 2]
3. [Gap 3]

## TAM / SAM / SOM
| Mercado | Valor | Base de Cálculo | Fonte |
|---------|-------|----------------|-------|
| TAM | R$ ... | ... | ... |
| SAM | R$ ... | ... | ... |
| SOM | R$ ... | ... | ... |

**Ticket médio usado:** R$ [valor dos concorrentes]

## Persona
**Nome:** [Nome Fictício]
**Idade:** [X anos]
**Profissão:** [ocupação]
**Onde mora:** [cidade/região]

**Dores específicas:**
- [Dor 1]
- [Dor 2]
- [Dor 3]

**Comportamento digital:**
- Redes: [lista]
- Consome: [formato]
- Dispositivo: [mobile/desktop]
- Frequência: [diário/semanal]

**O que usa hoje:**
- [Solução 1] — insuficiente porque [razão]
- [Solução 2] — insuficiente porque [razão]

**Frase sobre o problema:**
> "[frase em primeira pessoa]"

## Tendências
- [Tendência 1]
- [Tendência 2]
- [Tendência 3]

## Conclusão
[Síntese: tem mercado? qual o gap principal? ticket médio suporta o modelo? vale construir?]

---
_Pronto para o Agente Estratégia_
```

Ao finalizar:
> "✅ pesquisa-mercado.md salvo em output/. Retornando ao Agente Ideia."
