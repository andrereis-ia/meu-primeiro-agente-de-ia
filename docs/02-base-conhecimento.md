# 📚 Base de Conhecimento

## 📊 Dados Utilizados

| Arquivo | Formato | Para que serve no Amigo Investidor? |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores, ou seja, dar continuidade ao atendimento de forma mais eficiente. 🔄 |
| `perfil_investidor.json` | JSON | Personalizar as explicações sobre as dúvidas e necessidades de aprendizado do cliente. 👤 |
| `produtos_financeiros.json` | JSON | Conhecer os produtos disponíveis para que eles possam ser ensinados ao cliente. 💰 |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente e usar essas informações de forma didática. 📈 |

---

## 🛠️ Adaptações nos Dados

O produto **Fundo Imobiliário (FII)** substituiu o Fundo Multimercado, pois pessoalmente me sinto mais confiante em usar apenas produtos financeiros que eu conheço. Assim, poderei validar as respostas do Amigo Investidor de forma mais assertiva. ✅

---

## 🚀 Estratégia de Integração

### Como os dados são carregados? 💻

Existem duas possibilidades: injetar os dados diretamente no prompt (Ctrl + C, Ctrl + V) ou carregar os arquivos via código, como no exemplo abaixo:

```python
import pandas as pd
import json

perfil = json.load(open('./data/perfil_investidor.json'))
transacoes = pd.read_csv('./data/transacoes.csv')
historico = pd.read_csv('./data/historico_atendimento.csv')
produtos = json.load(open('./data/produtos_financeiros.json'))
```
---
## Como os dados são usados no prompt? 🧩

Para simplificar, podemos simplesmente "injetar" os dados em nosso prompt, garantindo que o Agente tenha o melhor contexto possível. Lembrando que, em soluções mais robustas, o ideal é que essas informações sejam carregadas dinamicamente para ganhar flexibilidade.

---

## 📝 Exemplo de Contexto Montado

O exemplo de contexto montado abaixo se baseia nos dados originais da base de conhecimento, mas os sintetiza deixando apenas as informações mais relevantes, otimizando assim o consumo de tokens.

---

## 📌 Dados do Cliente:

Nome: João Silva

Perfil: Moderado

Objetivo: Construir reserva de emergência 🛡️

Reserva atual: R$ 10.000 (meta: R$ 15.000)

---

### 💸 Resumo dos Gastos:

Moradia: R$ 1.380

Alimentação: R$ 570

Transporte: R$ 295

Saúde: R$ 188

Lazer: R$ 55,90

Total de saídas: R$ 2.488,90

---

### 🎓 Produtos Disponíveis para ExplicaR:

Tesouro Selic (risco baixo)

CDB Liquidez Diária (risco baixo)

LCI/LCA (risco baixo)

Fundo Imobiliário - FII (risco médio) 🏢

Fundo de Ações (risco alto) 📉

---
