# 🖥️ Classificador de Dígitos MNIST com Machine Learning

## 📋 Sobre o Projeto

Este projeto implementa um sistema de classificação de dígitos manuscritos (0-9) utilizando o dataset MNIST. O objetivo é comparar diferentes algoritmos de machine learning e avaliar seu desempenho em tarefas de reconhecimento de imagem.

## 🎯 Problema Resolvido

O reconhecimento de dígitos manuscritos é um problema clássico de visão computacional. Este projeto demonstra como diferentes modelos de machine learning podem ser aplicados para resolver esse problema, analisando suas vantagens e desvantagens.

## 🛠️ Tecnologias Utilizadas

### Bibliotecas Principais
- **Python 3.14** - Linguagem de programação
- **Scikit-learn** - Modelos de machine learning
- **NumPy** - Operações matemáticas
- **Matplotlib** - Visualização de dados
- **Seaborn** - Visualização estatística
- **Pandas** - Manipulação de dados
- **Jupyter Notebook** - Desenvolvimento interativo

### Modelos Testados
1. **K-Nearest Neighbors (KNN)**
2. **Random Forest**
3. **MLP (Rede Neural)**

## 📁 Estrutura do Projeto

```
meu-projeto-ia/
│
├── data/                          # Dados do projeto
│   └── dados_funcionarios.csv     # Dados gerados para análise
│
├── notebooks/                     # Notebooks Jupyter
│   └── fase1_eda_mnist.ipynb      # Análise completa
│
├── src/                           # Código fonte Python
│   └── analise.py                 # Funções auxiliares
│
├── requirements.txt               # Dependências do projeto
├── README.md                      # Documentação
└── .gitignore                     # Arquivos ignorados
```

## 🔄 Fluxo de Trabalho (Git)

O projeto seguiu o fluxo de trabalho Git Flow:
main
└── develop
└── feature/fase1-eda

**Branches:**
- `main`: Código final e estável
- `develop`: Desenvolvimento ativo
- `feature/fase1-eda`: Análise exploratória e modelos

## 📊 Metodologia

### Fase 1: Análise Exploratória (EDA)
- Carregamento do dataset MNIST
- Visualização das imagens
- Análise de balanceamento das classes
- Documentação da estrutura dos dados

### Fase 2: Pré-processamento
- Divisão treino/teste (80%/20%) com estratificação
- Normalização dos pixels para [0, 1]
- Justificativa: acelerar convergência e evitar dominância de features

### Fase 3: Treinamento e Ajuste
**Modelos treinados com GridSearch:**

| Modelo | Hiperparâmetros | Melhores Valores |
|--------|----------------|------------------|
| KNN | n_neighbors, weights | 5, 'distance' |
| Random Forest | n_estimators, max_depth | 100, 20 |
| MLP | hidden_layer_sizes, learning_rate_init | (128,), 0.001 |

### Fase 4: Avaliação Comparativa
- Matrizes de confusão
- Classification Report completo
- Análise de custo-benefício

**Resultados:**

| Modelo | Acurácia | Precisão | Recall | F1-Score |
|--------|----------|----------|--------|----------|
| KNN | 0.97XX | 0.97XX | 0.97XX | 0.97XX |
| Random Forest | 0.97XX | 0.97XX | 0.97XX | 0.97XX |
| MLP | 0.98XX | 0.98XX | 0.98XX | 0.98XX |

### Fase 5: Testes de Robustez
- **Class Masking**: Treino sem classes 4 e 7
- **OOD (Out-of-Distribution)**: Teste apenas com classes 4 e 7
- **Imagens Próprias**: Processamento e classificação de imagens personalizadas

## 🚀 Como Executar

### 1. Clone o repositório
git clone https://github.com/hugocileiro/meu-projeto-ia.git
cd meu-projeto-ia

### 2. Instale as dependências
pip install -r requirements.txt

### 3. Execute o Jupyter Notebook
jupyter notebook

### 4. Abra o notebook
- Navegue até a pasta `notebooks`
- Abra `fase1_eda_mnist.ipynb`
- Execute as células em ordem

## 📈 Resultados e Insights

### ✅ Principais Descobertas
- **Random Forest** oferece o melhor custo-benefício (alta acurácia com tempo moderado)
- **MLP** tem a maior acurácia, mas exige mais tempo de treinamento
- **KNN** é o mais rápido, mas menos preciso

### 🔍 Dígitos Mais Confundidos
- 4 e 9: Formas visualmente similares
- 7 e 9: Traços que podem se confundir
- 3 e 5: Curvas semelhantes

### ⚠️ Limitações
- O modelo falha ao reconhecer dígitos que nunca viu (classes 4 e 7 no treino)
- A "falsa certeza" (overconfidence) é um problema quando o modelo encontra dados desconhecidos

## 💡 Melhorias Futuras

1. **Augmentação de dados**: Rotação, zoom e deslocamento para aumentar a robustez
2. **Redes Neurais Profundas**: Usar CNNs para melhorar a acurácia
3. **Ensemble Learning**: Combinar modelos para melhor performance
4. **Detecção de OOD**: Implementar métodos para detectar dados fora da distribuição
5. **Deploy em produção**: Criar uma API para classificação em tempo real

## 📝 Lições Aprendidas

1. **Normalização** é crucial para algoritmos baseados em gradiente
2. **GridSearch** ajuda a encontrar os melhores hiperparâmetros
3. **Estratificação** mantém o balanceamento das classes
4. **Testes de estresse** revelam limitações do modelo

## 👨‍💻 Autor

**Hugo Cileiro**

## 📅 Data de Entrega

14/09/2026

## 📚 Referências

- [MNIST Dataset](http://yann.lecun.com/exdb/mnist/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [Machine Learning Mastery](https://machinelearningmastery.com/)
