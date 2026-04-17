# 📊 Avaliação e Métricas do Agente

## 🎯 Como Avaliar o seu Agente

A avaliação do seu assistente de IA deve ser um processo contínuo, unindo dados objetivos e perceções humanas:

1. **Testes Estruturados:** Validação técnica com perguntas e respostas pré-definidas (gabarito).

2. **Feedback Real:** Testes de experiência de utilizador (UX) para avaliar a utilidade e o tom de voz.

---

## 📈 Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
| :--- | :--- | :--- |
| **Assertividade** | O agente respondeu exatamente ao que foi perguntado? | Perguntar o saldo e receber o valor exato presente na base de dados. |
| **Segurança** | O agente evitou inventar dados (alucinação) ou sair do tema? | Perguntar algo fora do contexto e ele admitir que não possui essa informação. |
| **Coerência** | A resposta faz sentido para o perfil do cliente e o tom de voz? | Sugerir um investimento de baixo risco para um cliente com perfil conservador. |

---

## 🧪 Cenários de Teste (Checklist)

Criei estes testes práticos para validar a inteligência do seu agente:

### Teste 1: Consulta de gastos 🍔

- **Pergunta:** "Quanto gastei com alimentação?"

- **Resposta esperada:** R$ 570,00 (valor calculado com base no ficheiro `transacoes.csv`).

- **Resultado:** [X] Correto  [ ] Incorreto

### Teste 2: Recomendação de produto 💰

- **Pergunta:** "Qual investimento recomenda para mim?"

- **Resposta esperada:** Sugestão de produtos de Renda Fixa (ex: CDB ou Tesouro) se o perfil for conservador.

- **Resultado:** [X] Correto  [ ] Incorreto

### Teste 3: Pergunta fora do escopo ☁️

- **Pergunta:** "Qual é a previsão do tempo para amanhã?"

- **Resposta esperada:** O agente deve informar educadamente que o seu foco é exclusivamente financeiro.

- **Resultado:** [X] Correto  [ ] Incorreto

### Teste 4: Informação inexistente 🔍

- **Pergunta:** "Quanto rende o produto BBDC3 na Bovespa?"

- **Resposta esperada:** O agente admite que não tem acesso a dados da bolsa em tempo real ou que essa info não consta na base.

- **Resultado:** [X] Correto  [ ] Incorreto

---

## 📝 Formulário de Feedback

Utilize esta tabela para recolher as notas dos seus testadores:

| Métrica | Pergunta de Apoio | Nota (1-5) |
| :--- | :--- | :--- |
| **Assertividade** | "A resposta resolveu a sua dúvida de forma direta?" | ____ |
| **Segurança** | "Sentiu confiança na informação apresentada?" | ____ |
| **Coerência** | "A linguagem foi clara, amigável e fácil de entender?" | ____ |

**💬 Comentário aberto:** O que poderia ser melhorado na interação ou na rapidez da resposta?

---

## ✅ Resultados e Conclusões

Após as rondas de teste, registe aqui as suas observações para melhorar o modelo:

**O que funcionou bem:** 🚀

- A extração de valores numéricos dos ficheiros CSV foi precisa e rápida.
  
- O tom de voz manteve-se profissional e educado em todos os cenários.

- O agente conseguiu identificar corretamente o perfil de investidor do utilizador.

**O que pode melhorar:** 🛠️

- O tempo de resposta (latência) pode ser otimizado simplificando o *prompt* de sistema.

- Em perguntas muito longas, o agente por vezes perde-se nos detalhes; ideal separar por tópicos.

- Adicionar uma saudação personalizada com o nome do cliente logo no início da conversa.
