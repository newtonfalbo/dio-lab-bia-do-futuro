# Base de Conhecimento

## Dados Utilizados

| Arquivo                     | Formato | Utilização no Agente                                                                                                          |
| --------------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `historico_atendimento.csv` | CSV     | Consulta o histórico de atendimentos para contextualizar as interações anteriores do cliente.                                 |
| `perfil_investidor.json`    | JSON    | Recupera o perfil do investidor, objetivos financeiros e nível de risco para personalizar as recomendações.                   |
| `produtos_financeiros.json` | JSON    | Disponibiliza informações sobre produtos financeiros, como categoria, risco, rentabilidade, aporte mínimo e público indicado. |
| `transacoes.csv`            | CSV     | Analisa o histórico de transações para identificar padrões financeiros e possíveis movimentações anômalas.                    |

---

## Adaptações nos Dados

Foram utilizados os arquivos disponibilizados pela DIO sem alterações em sua estrutura. Durante a execução, os dados são carregados e organizados em DataFrames (CSV) e objetos JSON para facilitar consultas e integrar as informações utilizadas pelo agente.

---

## Estratégia de Integração

### Como os dados são carregados?

Os arquivos da pasta `data` são carregados no início da execução da aplicação. Os arquivos CSV são importados utilizando a biblioteca **Pandas**, enquanto os arquivos JSON são carregados com o módulo **json** da biblioteca padrão do Python.

### Como os dados são usados no prompt?

O agente utiliza uma estratégia de recuperação de contexto (*Retrieval*). Antes de gerar uma resposta, ele consulta dinamicamente os arquivos da base de conhecimento e seleciona apenas as informações relacionadas à solicitação do usuário. Essas informações são utilizadas para compor o contexto enviado ao modelo, tornando as respostas mais precisas, consistentes e personalizadas.

---

## Exemplo de Contexto Montado

```json
{
  "cliente": {
    "nome": "João Silva",
    "perfil_investidor": "moderado",
    "objetivo": "Crescimento Patrimonial"
  },
  "historico_atendimento": {
    "data": "2025-09-15",
    "canal": "chat",
    "tema": "CDB",
    "resumo": "Cliente perguntou sobre rentabilidade e prazos.",
    "resolvido": true
  },
  "transacoes": [
    {
      "data": "2025-09-15",
      "tipo": "PIX",
      "valor": 850.00
    },
    {
      "data": "2025-09-18",
      "tipo": "Supermercado",
      "valor": 420.50
    },
    {
      "data": "2025-09-21",
      "tipo": "TED",
      "valor": 9800.00,
      "status": "Possível anomalia"
    }
  ],
  "produto_recomendado": {
    "nome": "Tesouro Selic",
    "categoria": "renda_fixa",
    "risco": "baixo",
    "rentabilidade": "100% da Selic",
    "aporte_minimo": 30.00,
    "indicado_para": "Reserva de emergência e iniciantes"
  }
}
```
