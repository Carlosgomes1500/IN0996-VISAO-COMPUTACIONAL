# IN0996 - Visão Computacional

Este repositório contém a resolução da atividade final da disciplina de Visão Computacional do Centro de Informática (CIn) da UFPE. O projeto explora diversas técnicas clássicas de processamento de imagens, extração de características e análise geométrica. Todo o código foi desenvolvido em Python e estruturado para execução no Google Colab.

## Resumo das Atividades

O projeto está dividido em cinco partes principais, focadas em resolver problemas práticos e analíticos de visão computacional:

* **Questão 1: Análise de Ilusões de Ótica**
    * Aplicação do detector de bordas de Canny e da Transformada de Hough para detecção de linhas e círculos.
    * O algoritmo utiliza geometria analítica para comprovar matematicamente o paralelismo na Ilusão de Zöllner, obtendo um ângulo relativo de 0.00 graus.
    * Também demonstra a equivalência dimensional de círculos internos em outra ilusão de ótica através do cálculo de tangentes.

* **Questão 2: Detecção de Placa de Trânsito**
    * Conversão da imagem original para escala de cinza e aplicação de filtro de desfoque para redução de ruído.
    * Utilização da Transformada de Hough nativa do OpenCV para buscar padrões circulares.
    * A placa alvo foi isolada selecionando o círculo detectado com o maior raio, baseando-se na heurística de perspectiva de que o objeto mais próximo à câmera aparenta ser maior.

* **Questão 3: Classificação de Texturas**
    * Extração de descritores numéricos de imagens utilizando o Histograma de Gradientes Orientados (HOG).
    * Avaliação de diferentes métricas de distância (Euclidiana, Cosseno e Qui-Quadrado).
    * A Distância Qui-Quadrado foi selecionada como a melhor métrica por maximizar a distância inter-classe e minimizar a intra-classe, resultando na classificação automática e correta de imagens de teste.

* **Questão 4: Detecção de Objetos (Tomates)**
    * Pré-processamento com conversão para escala de cinza e detecção de bordas via Canny com limiares de 100 e 200.
    * Identificação de quatro tomates na imagem utilizando a Transformada de Hough para círculos, configurada para buscar picos em um intervalo de raios definido entre 75 e 100 pixels.

* **Questão 5: Correção de Cores (Color Constancy)**
    * Implementação dos algoritmos *White Patch Retinex* e *Gray World* para realizar ajustes de iluminação nas imagens.
    * Foram aplicados cortes baseados em percentis do histograma (*thresholds* de 0.01, 0.13 e 0.25) para aumentar a robustez dos algoritmos contra ruídos e reflexos especulares.
    * Os resultados experimentais indicaram um bom equilíbrio cromático geral ao utilizar o método *Gray World* em diferentes cenários e limiares.

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Processamento de Imagem:** OpenCV (`cv2`), Scikit-image (`skimage`)
* **Manipulação de Dados e Matemática:** NumPy, SciPy
* **Visualização Gráfica:** Matplotlib
* **Ambiente:** Google Colab integrado ao Google Drive
