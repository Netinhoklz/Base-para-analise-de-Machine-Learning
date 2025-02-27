# Sistema Base para Análise de Machine Learning 🚀

📊 **Uma base estruturada e automatizada para construção e avaliação de modelos de machine learning.**

---

## 📝 Descrição  
Este repositório fornece um framework em Python robusto para simplificar o desenvolvimento de modelos de machine learning. Inclui balanceamento de dados, ajuste de hiperparâmetros, avaliação detalhada e visualizações intuitivas. Ideal para tarefas de classificação binária, como prever se um evento-alvo ocorrerá (ex: "fechar um gap").

---

## ✨ Funcionalidades  
- **Balanceamento de Classes**: Usa `RandomOverSampler` para tratar desbalanceamento de dados.  
- **Ajuste de Hiperparâmetros**: Utiliza `GridSearchCV` para encontrar parâmetros ideais.  
- **Avaliação do Modelo**: Calcula acurácia, precisão, recall, F1-score, ROC-AUC e mais.  
- **Análise Visual**: Gera matriz de confusão, curva ROC, análise de thresholds e importância de features.  
- **Otimização de Threshold**: Permite ajustar dinamicamente o threshold para equilibrar precisão/recall.  
- **Pronto para Produção**: Exporta o melhor modelo em `.pkl` para implantação.

---

## 🧩 Estrutura do Código  

### 1. Preparação dos Dados  
- **Importação**: Carrega dados pré-processados de `dados_tratados.csv`.  
- **Balanceamento**: Aplica oversampling para equilibrar classes.  
- **Divisão Treino-Teste**: Split estratificado para manter a distribuição das classes.

### 2. Treinamento do Modelo  
- **Random Forest**: Modelo padrão para classificação.  
- **Busca em Grade**: Testa hiperparâmetros como `n_estimators`, `max_depth` e `min_samples_split`.  
- **Seleção do Melhor Modelo**: Retorna o modelo com maior acurácia validada.

### 3. Avaliação e Visualização  
- **Matriz de Confusão**: Mostra classes previstas vs. reais.  
- **Curva ROC**: Analisa trade-offs entre taxa de verdadeiros positivos e falsos positivos.  
- **Análise de Threshold**: Exibe como precisão, recall e F1-score variam com o threshold.  
- **Importância de Features**: Destaca preditores-chave usando gráficos.

### 4. Exportação do Modelo  
- **Persistência**: Salva o melhor modelo como `melhor_modelo_prever_se_vai_fechar_o_gap.pkl` via `joblib`.

---

## 🎯 Vantagens Principais  
- **Automação**: Fluxo completo (dados → modelo) com intervenção mínima.  
- **Tratamento de Desbalanceamento**: Melhora desempenho em classes minoritárias.  
- **Métricas Abrangentes**: Avalia o modelo com múltiplas métricas.  
- **Clareza Visual**: Resultados interpretáveis através de gráficos.  
- **Flexibilidade**: Ajuste de thresholds para priorizar precisão ou recall conforme necessidade.

---

## 📊 Visualizações Exemplo  
| Matriz de Confusão | Curva ROC | Importância de Features |
|------------------|-----------|--------------------|
| ![Matriz de Confusão](https://via.placeholder.com/200x150/FF6B6B/FFFFFF?text=CM) | ![Curva ROC](https://via.placeholder.com/200x150/4ECDC4/FFFFFF?text=ROC) | ![Features](https://via.placeholder.com/200x150/45B7D1/FFFFFF?text=Features) |

---

## 🛠️ Como Usar  

### Pré-requisitos  
- Python 3.8+  
- Bibliotecas: `pandas`, `scikit-learn`, `imbalanced-learn`, `seaborn`, `matplotlib`, `joblib`  

### Passos  
1. **Prepare os Dados**: Coloque dados pré-processados em `dados_tratados.csv`.  
2. **Execute o Código**: Rode as células para treinar, avaliar e exportar o modelo.  
3. **Ajuste os Thresholds**: Modifique o threshold na seção "Analisando modelo com o Threshold em 0.6" conforme necessário.  

```bash
# Instale as dependências
pip install pandas scikit-learn imbalanced-learn matplotlib seaborn joblib
