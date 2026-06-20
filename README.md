# 🤖 Falbo AI – Agente Financeiro Inteligente com IA Generativa

## 📖 Sobre o Projeto

O **Falbo AI** é um agente financeiro inteligente desenvolvido durante o laboratório da **DIO**, utilizando conceitos de **IA Generativa**, recuperação de contexto (Retrieval), engenharia de prompts e bases de conhecimento estruturadas.

O agente consulta informações sobre o cliente, histórico de atendimentos, produtos financeiros e transações para fornecer respostas personalizadas, contextualizadas e seguras.

Seu principal objetivo é auxiliar clientes na tomada de decisões financeiras, oferecendo recomendações adequadas ao perfil do investidor e identificando possíveis comportamentos financeiros fora do padrão.

---

## 🎯 Objetivos

* Personalizar recomendações financeiras conforme o perfil do cliente.
* Consultar automaticamente uma base de conhecimento.
* Recuperar o histórico de atendimentos para contextualizar respostas.
* Sugerir produtos financeiros compatíveis.
* Analisar transações financeiras e identificar possíveis anomalias.
* Produzir respostas confiáveis, reduzindo riscos de alucinação.

---

## 🚀 Funcionalidades

* 📊 Consulta ao perfil do investidor.
* 💬 Histórico inteligente de atendimentos.
* 💰 Recomendação de produtos financeiros.
* 📈 Consulta ao histórico de transações.
* 🚨 Identificação de possíveis movimentações anômalas.
* 🛡️ Estratégias para reduzir respostas incorretas (Anti-Hallucination).

---

## 🧠 Arquitetura do Agente

```text
Usuário
    │
    ▼
Falbo AI
    │
    ├── Consulta perfil_investidor.json
    ├── Consulta historico_atendimento.csv
    ├── Consulta produtos_financeiros.json
    ├── Consulta transacoes.csv
    │
    ▼
Monta o contexto da conversa
    │
    ▼
IA Generativa
    │
    ▼
Resposta personalizada
```

---

## 📂 Estrutura do Projeto

```text
dio-lab-bia-do-futuro
│
├── README.md
│
├── data
│   ├── historico_atendimento.csv
│   ├── perfil_investidor.json
│   ├── produtos_financeiros.json
│   └── transacoes.csv
│
├── docs
│   ├── 01-documentacao-agente.md
│   ├── 02-base-conhecimento.md
│   ├── 03-prompts.md
│   ├── 04-metricas.md
│   └── 05-pitch.md
│
├── assets
│
└── src
```

---

## 📚 Base de Conhecimento

O agente utiliza quatro conjuntos de dados:

| Arquivo                     | Descrição                        |
| --------------------------- | -------------------------------- |
| `perfil_investidor.json`    | Perfil e objetivos do cliente    |
| `historico_atendimento.csv` | Histórico de atendimentos        |
| `produtos_financeiros.json` | Catálogo de produtos financeiros |
| `transacoes.csv`            | Histórico de transações          |

Esses dados são consultados dinamicamente para construir o contexto utilizado pelo agente antes da geração da resposta.

---

## 🛠️ Tecnologias Utilizadas

* Python
* Google Colab
* Pandas
* JSON
* IA Generativa
* Engenharia de Prompts
* Git
* GitHub

---

## 🔒 Segurança

O Falbo AI foi desenvolvido seguindo boas práticas para reduzir respostas incorretas:

* Utiliza apenas informações presentes na base de conhecimento.
* Consulta dinamicamente os arquivos antes de responder.
* Não cria informações inexistentes.
* Informa quando não possui dados suficientes.
* Não realiza recomendações financeiras sem considerar o perfil do cliente.

---

## 📁 Documentação

Toda a documentação do projeto encontra-se na pasta **docs**:

* Documentação do agente
* Base de conhecimento
* Engenharia de prompts
* Métricas de avaliação
* Pitch do projeto

---

## 👨‍💻 Autor

**Newton Falbo**

Projeto desenvolvido durante o laboratório **BIA do Futuro – DIO** como aplicação prática de IA Generativa para agentes financeiros inteligentes.
