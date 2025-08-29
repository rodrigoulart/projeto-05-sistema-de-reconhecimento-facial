# 🎯 Projeto 05 — Sistema de Reconhecimento Facial  

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)](https://www.python.org/)  [![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange?logo=tensorflow)](https://www.tensorflow.org/)  [![OpenCV](https://img.shields.io/badge/OpenCV-VisãoVerde-green?logo=opencv)](https://opencv.org/)  [![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Modelagem-lightgrey?logo=python)](https://scikit-learn.org/stable/)  

> Quinto projeto do **Bootcamp Machine Learning** da [DIO](https://www.dio.me/) em parceria com a **BairesDev**.  
> Aplicação prática de **detecção e reconhecimento facial** utilizando um dataset de rostos organizados por classes.  

---

## 📌 Sobre o Projeto  

Este projeto demonstra como detectar e classificar rostos em imagens usando técnicas de visão computacional e aprendizado de máquina.  

**O programa realiza:**  

1. Detecção de rostos em imagens usando OpenCV.  
2. Extração de embeddings com ResNet50 (TensorFlow).  
3. Treinamento de um classificador **SVM** para múltiplas classes.  
4. Exibição de **bounding boxes** ao redor de cada rosto com nome previsto e probabilidade.  

**Objetivos do projeto**:  
- 🧮 Aplicar técnicas de detecção e reconhecimento facial.  
- 📊 Visualizar bounding boxes com nomes e probabilidades das predições.  
- 📈 Avaliar a acurácia do modelo com múltiplas classes de rostos.  
- 💾 Treinar e salvar modelos para uso futuro.  

---

## **🛠️ Tecnologias e Ferramentas**  

- **Python 3.10+** ([link](https://www.python.org/))  
- **TensorFlow** → Extração de embeddings com ResNet50  
- **OpenCV** → Detecção de rostos e manipulação de imagens  
- **Scikit-Learn** → Treinamento do classificador SVM e codificação de rótulos  
- **Matplotlib** → Visualização de imagens com bounding boxes  
- **Seaborn** → Visualização de métricas e matriz de confusão  

---

## **📂 Estrutura do Projeto no Colab**  

```text
projeto-05-sistema-de-reconhecimento-facial/
├── dataset/                      # Imagens organizadas por classe
│   ├── lula/
│   ├── bolsonaro/
│   └── outros/
├── faces_dataset/                # (Opcional) Rostos extraídos automaticamente
├── outputs/                      # Modelos treinados e LabelEncoder
│   ├── face_classifier.pkl
│   └── label_encoder.pkl               # Imagens para teste do modelo
└── test_images/                  # Imagens para teste do modelo
```

---

## 📊 Resultados
```text
O modelo SVM é treinado com embeddings extraídos das imagens de rostos.
As previsões do modelo exibem:
Matriz de Confusão: permite analisar erros e acertos na classificação por classe.
Bounding boxes em imagens de teste: mostram rostos detectados, classe prevista e probabilidade.

Relatório de classificação:  
              precision    recall  f1-score   support  

   bolsonaro       0.75      1.00      0.86         3  
        lula       1.00      1.00      1.00         3  
      outros       1.00      0.67      0.80         3  
  
    accuracy                           0.89         9  
   macro avg       0.92      0.89      0.89         9  
weighted avg       0.92      0.89      0.89         9  


Resumo do dataset processado:  
Classe 'bolsonaro': 16 imagens processadas  
Classe 'outros': 13 imagens processadas  
Classe '.ipynb_checkpoints': 0 imagens processadas  
Classe 'lula': 13 imagens processadas  
```

---

## 🚀 Como Executar

```bash
# Clone o repositório
git clone https://github.com/rodrigoulart/projeto-05-sistema-de-reconhecimento-facial.git

# Acesse a pasta do projeto
cd projeto-05-sistema-de-reconhecimento-facial

# Crie uma pasta chamada "dataset"

# Crie pastas com os nomes das classes e faça o upload das imagens a serem processadas, dentro de sua pasta correspondente(este exemplo) ou faça o upload das imegens rotulada diretamente na pasta "dataset"

# Abra o notebook no Colab e execute os blocos

# Faça o upload da imagem a ser detectada e classificada, através do file input que irá aparecer na última célula de código do notebook
```

O notebook irá:

Treinar o modelo SVM com embeddings extraídos das imagens do dataset.

Salvar o modelo e o LabelEncoder em outputs/.

Permitir o upload de novas imagens e detectar/classificar múltiplos rostos com bounding boxes.

---

## 📚 Conceitos Aplicados

Detecção de rostos → Identificação das regiões faciais nas imagens.

Extração de embeddings → Representação vetorial dos rostos usando ResNet50.

Classificação SVM → Previsão da classe de cada rosto detectado.

Matriz de Confusão → Avaliação detalhada do desempenho do classificador.

Probabilidades de predição → Indicam a confiança do modelo em cada previsão.

## 🏆 Créditos

Desenvolvido por Rodrigo Moraes, como parte dos desafios do Bootcamp de Machine Learning da DIO em parceria com a BairesDev.

📎 Repositório: github.com/rodrigoulart/projeto-05-sistema-de-reconhecimento-facial
