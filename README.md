# 📊 Modelo de Concessão de Crédito com Machine Learning

## 📌 Objetivo do Projeto
Desenvolver um modelo de Machine Learning capaz de prever a probabilidade de inadimplência de clientes, apoiando decisões de concessão de crédito.

---

## 🧠 Problema de Negócio

Instituições financeiras precisam decidir **para quem conceder crédito** minimizando risco.

O custo de aprovar um cliente inadimplente é muito maior do que recusar um cliente bom.

Por isso, o modelo foi otimizado para **alta sensibilidade (recall)** na classe inadimplente.

---

## 🗂️ Dados

Os dados utilizados são públicos e podem ser obtidos em:

🔗 [COLE AQUI O LINK DA BASE]

Devido ao tamanho do dataset, os dados não estão incluídos neste repositório.

---

## 🔧 Etapas do Projeto

### 1. Pré-processamento
- Tratamento de valores inválidos (ex: `DAYS_EMPLOYED = 365243`)
- Criação de novas variáveis
- Tratamento de missing values
- Padronização com `StandardScaler`

### 2. Divisão dos dados
- Treino
- Validação
- Teste

### 3. Modelagem
- Modelo baseline: Regressão Logística
- Modelo com balanceamento de classes (`class_weight='balanced'`)

### 4. Ajuste de Threshold
Escolha do limiar de decisão com base em:
- Precision
- Recall
- F1-score

Foco: **maximizar recall com equilíbrio de precisão**

### 5. Avaliação final no conjunto de teste

---

## 📈 Resultados do Modelo Final

**Threshold escolhido:** 0.35

### Métricas no conjunto de teste:

- **Recall (inadimplentes):** 87%
- **Precision (inadimplentes):** 11%
- **AUC:** 0.73

📌 Interpretação:

- O modelo consegue identificar a **maior parte dos inadimplentes**
- Mesmo com precisão baixa, isso é esperado em cenários com classes desbalanceadas
- Estratégia adequada para **política de crédito conservadora**

---

## 📊 Principais Insights

- Clientes com histórico de atraso apresentam maior risco
- Clientes mais novos tendem a maior inadimplência
- Variáveis de comportamento têm maior poder preditivo

---

## 🚀 Próximos Passos

- Testar modelos mais robustos (Random Forest, XGBoost)
- Engenharia de features avançada
- Ajuste de hiperparâmetros com GridSearch
- Uso de técnicas como SMOTE
- Monitoramento do modelo em produção

---

## 🧰 Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib / Seaborn

---

## 👨‍💻 Autor

**Maylson Maia**  
Projeto desenvolvido para portfólio de Ciência de Dados.
