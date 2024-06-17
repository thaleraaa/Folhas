# Descrição do Conjunto de Dados

Este conjunto de dados é destinado à classificação de doenças foliares em plantas de milho e inclui as seguintes categorias com o respectivo número de imagens:

- **0: Ferrugem Comum** - 1.306 imagens
- ![image](https://github.com/thaleraaa/Folhas/assets/163169162/a94c37c7-acf9-48c2-9875-b2154fc116bf)
- **1: Mancha Cinzenta na Folha** - 574 imagens
- ![image](https://github.com/thaleraaa/Folhas/assets/163169162/3feedaf5-8983-4cd2-8c06-4a3450c319c6)
- **2: Praga** - 1.146 imagens
- ![image](https://github.com/thaleraaa/Folhas/assets/163169162/a2ddd7ff-5f4f-4d35-b3cb-f8e2941259cf)
- **3: Saudável** - 1.162 imagens
- ![image](https://github.com/thaleraaa/Folhas/assets/163169162/bc3bdaba-aca3-4423-808b-d17afc9b9bee)


## Origem do Conjunto de Dados

O conjunto de dados foi compilado utilizando os populares conjuntos de dados PlantVillage e PlantDoc. Algumas imagens foram removidas durante a formação do conjunto de dados por não serem consideradas úteis. Os autores originais detêm os direitos autorais dos respectivos conjuntos de dados.

Fonte de dados:
https://www.kaggle.com/datasets/smaranjitghose/corn-or-maize-leaf-disease-dataset

## Metodologia

O projeto utiliza a rede Vision Transformer (ViT) específica `facebook/dino-vitb16` para a classificação de doenças foliares em plantas de milho. As etapas seguidas na implementação do modelo foram:

1. **Escolha do Modelo de Rede:** Foi selecionado o modelo pré-treinado devido à sua eficácia comprovada em tarefas de visão computacional.
2. **Ajuste Fino de Aprendizado:** Realizamos o fine-tuning do modelo com nosso conjunto de dados específico para melhorar a precisão da classificação.
3. **Verificação de Resultados e Tempo de Aprendizagem:** Após o ajuste fino, avaliamos a performance do modeloem termos de precisão e eficiência, considerando também o tempo necessário para o aprendizado.

A escolha deste modelo contribuiu significativamente para a precisão e robustez dos resultados obtidos.

## Resultados

O modelo `facebook/dino-vitb16` alcançou os seguintes resultados durante o treinamento e avaliação:

- **Avaliação após 1 época:**
  - Loss: 0.1539
  - Acurácia: 95.35%
  - Tempo de execução: 9.35s
  - Amostras por segundo: 89.58
  - Passos por segundo: 22.45

- **Avaliação após 2 épocas:**
  - Loss: 0.1378
  - Acurácia: 95.35%
  - Tempo de execução: 9.35s
  - Amostras por segundo: 89.62
  - Passos por segundo: 22.46

- **Avaliação após 3 épocas:**
  - Loss: 0.1007
  - Acurácia: 97.37%
  - Tempo de execução: 8.91s
  - Amostras por segundo: 94.07
  - Passos por segundo: 23.57

- **Métricas finais de treinamento após 3 épocas:**
  - Tempo total de treinamento: ~287s
  - Amostras por segundo: ~35
  - Passos por segundo: ~3.5
  - Loss médio de treinamento: ~0.1471

Esses resultados demonstram a eficácia do ajuste fino realizado no modelo `facebook/dino-vitb16`, refletindo uma alta acurácia e eficiência no processo de aprendizagem.



## Citações

- Singh D, Jain N, Jain P, Kayal P, Kumawat S, Batra N. PlantDoc: um conjunto de dados para detecção visual de doenças em plantas. Nos Anais do 7º ACM IKDD CoDS e 25º COMAD, 5 de janeiro de 2020 (pp. 249-253).
- J, ARUN PANDIAN; GOPAL, GEETHARAMANI (2019), “Dados para: Identificação de doenças foliares de plantas usando uma rede neural convolucional profunda de 9 camadas”, Mendeley Data, V1, doi: 10.17632/tywbtsjrjv.1.
