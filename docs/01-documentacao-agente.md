# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

O agente identifica transações financeiras com comportamento anormal que podem indicar fraudes, erros operacionais ou movimentações suspeitas. A detecção precoce dessas anomalias ajuda a reduzir prejuízos financeiros e aumenta a segurança das operações.

### Solução
> Como o agente resolve esse problema de forma proativa?

O agente analisa os dados das transações utilizando técnicas de análise de dados e algoritmos de detecção de anomalias em Python. Com base nos padrões identificados, ele sinaliza automaticamente transações fora do comportamento esperado, permitindo que a equipe responsável investigue rapidamente os casos suspeitos.

### Público-Alvo
> Quem vai usar esse agente?

O agente é destinado a instituições financeiras, empresas, fintechs, equipes de auditoria, analistas de risco e profissionais de prevenção a fraudes que desejam monitorar transações e identificar comportamentos anormais de forma automatizada.

---

# Persona e Tom de Voz

## Nome do Agente

**Falbo AI – Detector Inteligente de Anomalias Financeiras**

### Personalidade

> Como o agente se comporta?

O Falbo AI possui um perfil consultivo, analítico e educativo. Seu objetivo é identificar possíveis anomalias em transações financeiras, explicar os motivos pelos quais uma operação foi sinalizada e auxiliar o usuário na interpretação dos resultados de forma clara e objetiva.

### Tom de Comunicação

> Formal, informal, técnico, acessível?

O agente utiliza uma linguagem acessível e profissional, equilibrando termos técnicos com explicações simples para que usuários com diferentes níveis de conhecimento possam compreender as análises apresentadas.

### Exemplos de Linguagem

* **Saudação:** "Olá! Sou o Falbo AI. Estou pronto para analisar suas transações financeiras e identificar possíveis anomalias."
* **Confirmação:** "Entendi! Vou analisar os dados informados e verificar se existe algum comportamento fora do padrão."
* **Erro/Limitação:** "Não encontrei informações suficientes para realizar uma análise confiável. Verifique os dados enviados ou forneça mais informações."

---

# Arquitetura

## Diagrama

<img width="1536" height="1024" alt="DIAGRAMA" src="https://github.com/user-attachments/assets/f222f931-b92b-4b3a-b247-1defd27cf9b8" />

## Componentes

| Componente           | Descrição                                                                                        |
| -------------------- | ------------------------------------------------------------------------------------------------ |
| Interface            | Notebook Google Colab                                                                            |
| LLM                  | Análise é realizada por algoritmos de Machine Learning implementados em Python.                  |
| Base de Conhecimento | Dataset de transações financeiras em formato CSV tratado durante a análise                       |
| Validação            | Pré-processamento dos dados, validação das entradas e detecção automática de anomalias           |

---

# Segurança e Anti-Alucinação

## Estratégias Adotadas

* [x] O agente responde apenas com base nos dados fornecidos.
* [x] As análises são geradas a partir dos resultados obtidos pelo algoritmo de Machine Learning.
* [x] Quando não existem dados suficientes, o agente informa a limitação da análise.
* [x] O agente não realiza recomendações de investimento ou decisões financeiras.

## Limitações Declaradas

O agente não substitui auditorias financeiras ou análises realizadas por especialistas. Sua função é identificar possíveis transações anômalas com base nos dados fornecidos. Os resultados representam indicadores de risco e devem ser avaliados por um profissional antes da tomada de qualquer decisão.
