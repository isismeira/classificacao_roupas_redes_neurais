# 👕 Classificação de Peças de Roupas com Redes Neurais *Feedforward*

## 🎯 Objetivo
Este projeto tem como objetivo desenvolver e avaliar uma rede neural *feedforward* (*Perceptron Multicamadas - MLP*) para classificar peças de roupas utilizando o conjunto de dados Fashion MNIST. O foco é explorar a arquitetura de redes neurais densas para realizar a classificação multiclasse das imagens, analisando o desempenho do modelo através de métricas como perda (loss) e acurácia durante o treinamento e a validação, além de avaliar a performance final no conjunto de teste. O projeto aborda desde o carregamento e pré-processamento dos dados, a construção e compilação do modelo utilizando a Sequential API do Keras, até o treinamento, avaliação e a realização de predições.

## 💾 Dataset
O dataset utilizado é o Fashion MNIST, um substituto direto do MNIST. Ele contém 70 mil imagens pré-processadas em escala de cinza, cada uma com 28x28 pixels, distribuídas em 10 classes distintas.

## 🧠 Arquitetura da Rede Neural
A arquitetura da rede neural foi definida para uma tarefa de classificação multiclasse e consiste em:

*   **Camada de Entrada:** Uma camada `Flatten` para converter as imagens 28x28 em um vetor 1D de 784 características.
*   **Camadas Ocultas:**
    *   Primeira camada densa com 300 neurônios e função de ativação ReLU.
    *   Segunda camada densa com 100 neurônios e função de ativação ReLU.
*   **Camada de Saída:** Uma camada densa com 10 neurônios (um para cada classe) e função de ativação Softmax para produzir probabilidades de classe.

A rede possui um total de 266.610 parâmetros treináveis.

## ⚙️ Configuração do Modelo
O modelo foi compilado com:
*   **Função de Perda:** `sparse_categorical_crossentropy`, adequada para rótulos esparsos e classes exclusivas.
*   **Otimizador:** `sgd` (Gradiente Descendente Estocástico).
*   **Métricas:** `accuracy` para monitorar o desempenho.

## 📈 Treinamento
O modelo foi treinado por 30 épocas utilizando os conjuntos de treino e validação. As curvas de aprendizado (perda e acurácia) foram plotadas para visualizar o progresso do treinamento e identificar sinais de sobreajuste.

## ✅ Avaliação
O modelo foi avaliado no conjunto de teste para verificar sua capacidade de generalização.

## ▶️ Predições
Exemplos de predições foram realizados nas primeiras instâncias do conjunto de teste para demonstrar a capacidade do modelo em classificar novas imagens.
