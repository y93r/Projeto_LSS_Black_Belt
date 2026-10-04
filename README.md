# Projeto_LSS_Black_Belt
Projeto de certificação Black Belt pelo Grupo Voitto

# 📈 Lean Six Sigma Black Belt Project | Otimização da Eficiência Operacional Regional

![DMAIC](https://img.shields.io/badge/Methodology-DMAIC_Black_Belt-blue.svg)
![Python](https://img.shields.io/badge/Python-3.14-green.svg)
![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen.svg)

## 📌 Visão Geral do Projeto
Este projeto aplicou a metodologia **DMAIC (Lean Six Sigma Black Belt)** para resolver o gargalo de atendimento em 5 unidades da Regional MG do Grupo Vitta. O objetivo principal foi elevar o Nível de Serviço (NS) global da regional de uma média histórica deficitária para o patamar sustentado de **≥ 80%**.

---

## 🎯 Resumo das Etapas DMAIC

### 1. Define (Definição)
* **Escopo:** 5 unidades de saúde (BH Centro, BH Pampulha, Betim, BH Belvedere e Contagem).
* **Problema Identificado:** Unidades **Contagem** (~41,1%) e **BH Belvedere** (~56,8%) atuavam como os principais gargalos regionais.
* **Metas Estabelecidas:** 
  * Meta global regional: **80%**.
  * Meta conjunta ajustada para os gargalos: **~74,9%** (+18,2 p.p. em Belvedere e +33,8 p.p. em Contagem).

### 2. Measure (Medição)
* **Amostragem e Confiabilidade:** Cálculo amostral formal $n=196$ (95% Confiança, 5% Margem de Erro); validação do dataset de $N=57$ registros via Teorema do Limite Central.
* **Levantamento de Dados:** Mapeamento dos tempos de pré-autorização, guias rasuradas e fluxo horários de passageiros/clientes nos guichês.

### 3. Analyze (Análise)
Aplicação de testes de hipóteses estatísticos e modelagem preditiva no Python:
* **Teste t Pareado / Qui-Quadrado:** Confirmação do impacto crítico da ausência/rasura de documentos no tempo total de recepção.
* **ANOVA & Post-Hoc de Tukey:**
  * Identificação do **Plano D** como a operadora de maior burocracia, exigindo **15 a 16 min adicionais** de espera e registrando a menor taxa de aprovação.
* **Regressão Linear & Capacidade:**
  * Modelo: $\text{Capacidade}(Y) = -3{,}46 + 4{,}13 \times \text{Guichês}(X)$ ($R^2 = 0{,}988$).
  * **Diagnóstico de Pico:** Confirmado déficit físico de **2 guichês em Belvedere** (capacidade 17 vs. demanda 24 cl/h) e de **3 guichês em Contagem** (capacidade 25 vs. demanda 38 cl/h).

### 4. Improve (Melhoria)
* **Matriz de Priorização (Custo x Facilidade x Impacto):** Descarte de investimentos em hardware (compra de novos computadores, score 55) em prol de otimizações de processos/OPEX (score 105).
* **Plano de Ação 5W2H Executado:**
  * Tratativa antecipada (D-1) de exames do **Plano D**.
  * Reorganização das escalas de trabalho para manter 100% dos guichês ativos nos horários de pico.
  * Padronização do cadastro e triagem na recepção.

### 5. Control (Controlo e Sustentabilidade)
* **Cartas de Controle $X$-AM (CEP):**
  * **BH Belvedere:** Quebra do LSC histórico ($74{,}9\%$), estabilizando em **> 82%**.
  * **Contagem:** Salto de $52{,}5\%$ para a faixa de **76% a 79%**.
  * **Regional MG:** Transição sustentada para a faixa de **82,7% a 88,4%**, superando a meta global.
* **Garantia de Longo Prazo:**
  * Criação de Procedimentos Operacionais Padronizados (POPs).
  * Gestão à vista via Dashboards BI e monitoramento periódico das Cartas $X$-AM.

---

## 💰 Retorno Financeiro (ROI)
Com base no modelo de valoração de **R$ 235,00 por ponto percentual acima de 75%** para cada 1.000 clientes/ano em uma base regional de 192.000 clientes/ano:

**Ganho Anual** = `(83,39% - 75,0%) × R$ 235,00 × 192` = **R$ 378.444,00 / ano**
---
## 🛠️️ Tecnologias e Ferramentas Utilizadas
* **Linguagens & Bibliotecas:** Python (`pandas`, `scipy`, `pingouin`, `matplotlib`, `seaborn`).
* **Ferramentas Lean Six Sigma:** SIPOC, Análise de Processo, Diagrama de Ishikawa, Matriz Causa e Efeito, Matriz Esforço x Impacto, Matriz de Priorização, 5W2H, ANOVA, Post-Hoc Tukey, Regressão Linear e Cartas de Controlo $X$-AM, .
