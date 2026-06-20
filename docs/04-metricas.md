# Métricas de Avaliação

## Objetivo

As métricas de avaliação têm como finalidade verificar a qualidade, a confiabilidade e a precisão das respostas geradas pelo Falbo AI, garantindo que o agente utilize corretamente a base de conhecimento e forneça informações consistentes aos usuários.

---

## Métricas Utilizadas

| Métrica | Objetivo | Meta |
|----------|----------|------|
| Precisão das Respostas | Verificar se as respostas estão de acordo com a base de conhecimento. | ≥ 95% |
| Personalização | Avaliar se as recomendações consideram o perfil do investidor. | 100% |
| Detecção de Anomalias | Medir a capacidade do agente em identificar transações fora do padrão. | ≥ 90% |
| Tempo de Resposta | Medir o tempo necessário para gerar uma resposta ao usuário. | ≤ 2 segundos |
| Segurança | Garantir que nenhuma informação inexistente seja criada pelo agente. | 100% |

---

## Cenários de Teste

### Cenário 1 – Consulta de Produto

**Entrada**

> Qual investimento é recomendado para um perfil moderado?

**Resultado Esperado**

O agente deve consultar `perfil_investidor.json` e `produtos_financeiros.json`, recomendando apenas produtos compatíveis com o perfil do cliente.

---

### Cenário 2 – Histórico de Atendimento

**Entrada**

> Qual foi meu último atendimento?

**Resultado Esperado**

O agente deve recuperar a informação presente em `historico_atendimento.csv`.

---

### Cenário 3 – Análise de Transações

**Entrada**

> Existe alguma movimentação suspeita?

**Resultado Esperado**

O agente deve consultar `transacoes.csv` e destacar apenas transações fora do comportamento esperado.

---

## Critérios de Qualidade

O Falbo AI será considerado adequado quando:

- Recuperar corretamente as informações da base de conhecimento.
- Não gerar informações inexistentes.
- Personalizar as respostas conforme o perfil do cliente.
- Informar quando não houver dados suficientes.
- Manter respostas claras, objetivas e coerentes.

---

## Estratégias de Validação

- Testes com perguntas conhecidas.
- Comparação das respostas com os dados armazenados.
- Verificação da consistência das recomendações.
- Avaliação da identificação de possíveis anomalias.
- Revisão manual das respostas geradas.

---

## Resultado Esperado

Espera-se que o Falbo AI forneça respostas precisas, contextualizadas e seguras, utilizando exclusivamente as informações disponíveis na base de conhecimento e contribuindo para uma melhor experiência do usuário.
