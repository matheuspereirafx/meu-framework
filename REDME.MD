Pré-requisito: Pasta meu-framework/ com todas as skills instaladas em .claude/skills/.

1. Abre o terminal na pasta do framework
bashcd meu-framework
claude

2. Digita /agente-ideia
O agente inicia o Modo 1 — te faz perguntas uma por uma:

Qual o problema? Para quem? Como sabe que existe?
5 Porquês até chegar na causa raiz
Job To Be Done → gera o Job Statement
Mapa de Dor → identifica ponto de intervenção
Scorecard → avalia se o problema vale resolver

Entra no Modo 2 — Idealização:

Você descreve a solução
Automaticamente chama /pesquisa-mercado → pesquisa na web concorrentes, reviews, TAM/SAM/SOM com ticket médio real, e monta a persona com nome fictício, dores, comportamento digital e frase sobre o problema
Volta pro agente → Foco radical, Não clientes, Dao, CHA, Hipóteses

Gera: output/ideia.md + output/pesquisa-mercado.md

3. Digita /agente-estrategia
Lê automaticamente ideia.md e pesquisa-mercado.md.
Apresenta resumo do que encontrou e confirma contigo.
Trabalha em 4 fases:

Canvas → preenche os 9 blocos usando os outputs, só pergunta o que falta
ERRC → eliminar/reduzir/aumentar/criar baseado nos gaps e reviews
TAM/SAM/SOM → refina com ticket médio real e calcula receita potencial
Modelo de receita → sugere com justificativa baseada no mercado

Gera: output/estrategia.md

4. Digita /agente-financeiro
Lê estrategia.md.
Coleta premissas uma a uma:

Ticket, CAC, churn, custos fixos, investimento inicial, clientes mês 1, crescimento

Calcula:

Unit economics (LTV, LTV/CAC, payback, break-even)
Se LTV/CAC < 3x → alerta de risco crítico imediato
Projeção 24 meses em 3 cenários (pessimista -40% / realista / otimista +40%)
Sensibilidade (churn +40%, CAC +40%, ticket -20%)

Mostra resumo e pergunta:

"Posso gerar a planilha Excel?"

Gera: output/financeiro.md + output/financeiro.xlsx

5. Digita /agente-mvp
Lê ideia.md + financeiro.md.
Pega as hipóteses do agente-ideia, confirma contigo e ranqueia por risco.
Para cada hipótese decide:

Se é de desejo/conversão → experimento sem código (entrevista, landing page, smoke test)
Se é funcional/retenção → define features mínimas necessárias

Define indicadores de aderência:

Taxa de ativação, retenção semana 1 e 4, conversão free→pago, NPS

Gera: output/mvp.md

6. Digita /skill-plano-negocio
Lê todos os outputs de uma vez.
Identifica gaps e faz perguntas pontuais:

Missão, visão, estratégia de entrada, estrutura legal, roadmap

Gera 3 documentos:

output/resumo-executivo.md → síntese de 1 página para uso interno
output/plano-negocio.md → documento institucional completo
output/plano-negocio.docx → versão Word para investidores/bancos


7. Handoff para o projeto de desenvolvimento
bashcp output/ ../meu-projeto-dev/docs/
cd ../meu-projeto-dev
claude
# → /agente-prd (próxima fase)

Resultado final da pasta output/:
output/
├── ideia.md                ← problema + solução + hipóteses
├── pesquisa-mercado.md     ← concorrentes + persona + TAM real
├── estrategia.md           ← canvas + ERRC + modelo receita
├── financeiro.md           ← projeções + LTV/CAC + parecer
├── financeiro.xlsx         ← planilha com 3 cenários
├── mvp.md                  ← experimentos + indicadores
├── resumo-executivo.md     ← síntese 1 página
├── plano-negocio.md        ← documento completo
└── plano-negocio.docx      ← Word institucional
De ideia bruta a plano de negócio completo, sem sair do terminal.
