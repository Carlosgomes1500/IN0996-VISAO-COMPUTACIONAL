# IN0996 - Visão Computacional

Este repositório contém a resolução da atividade final da disciplina de Visão Computacional do Centro de Informática (CIn) da UFPE. [cite_start]O projeto explora diversas técnicas clássicas de processamento de imagens, extração de características e análise geométrica[cite: 1]. [cite_start]Todo o código foi desenvolvido em Python e estruturado para execução no Google Colab[cite: 16, 277].

## Resumo das Atividades

O projeto está dividido em cinco partes principais, focadas em resolver problemas práticos e analíticos de visão computacional:

* **Questão 1: Análise de Ilusões de Ótica**
    * [cite_start]Aplicação do detector de bordas de Canny e da Transformada de Hough para detecção de linhas e círculos[cite: 5, 6, 314, 318].
    * [cite_start]O algoritmo utiliza geometria analítica para comprovar matematicamente o paralelismo na Ilusão de Zöllner, obtendo um ângulo relativo de 0.00 graus[cite: 153, 155].
    * [cite_start]Também demonstra a equivalência dimensional de círculos internos em outra ilusão de ótica através do cálculo de tangentes[cite: 330, 339].

* **Questão 2: Detecção de Placa de Trânsito**
    * [cite_start]Conversão da imagem original para escala de cinza e aplicação de filtro de desfoque para redução de ruído[cite: 464, 468, 469].
    * [cite_start]Utilização da Transformada de Hough nativa do OpenCV para buscar padrões circulares[cite: 473].
    * [cite_start]A placa alvo foi isolada selecionando o círculo detectado com o maior raio, baseando-se na heurística de perspectiva de que o objeto mais próximo à câmera aparenta ser maior[cite: 478, 479].

* **Questão 3: Classificação de Texturas**
    * [cite_start]Extração de descritores numéricos de imagens utilizando o Histograma de Gradientes Orientados (HOG)[cite: 550, 551].
    * [cite_start]Avaliação de diferentes métricas de distância (Euclidiana, Cosseno e Qui-Quadrado)[cite: 555].
    * [cite_start]A Distância Qui-Quadrado foi selecionada como a melhor métrica por maximizar a distância inter-classe e minimizar a intra-classe, resultando na classificação automática e correta de imagens de teste[cite: 571, 588, 589].

* **Questão 4: Detecção de Objetos (Tomates)**
    * [cite_start]Pré-processamento com conversão para escala de cinza e detecção de bordas via Canny com limiares de 100 e 200[cite: 722, 726].
    * [cite_start]Identificação de quatro tomates na imagem utilizando a Transformada de Hough para círculos, configurada para buscar picos em um intervalo de raios definido entre 75 e 100 pixels[cite: 729, 730].

* **Questão 5: Correção de Cores (Color Constancy)**
    * [cite_start]Implementação dos algoritmos *White Patch Retinex* e *Gray World* para realizar ajustes de iluminação nas imagens[cite: 801, 806, 811].
    * [cite_start]Foram aplicados cortes baseados em percentis do histograma (*thresholds* de 0.01, 0.13 e 0.25) para aumentar a robustez dos algoritmos contra ruídos e reflexos especulares[cite: 801, 803, 804].
    * [cite_start]Os resultados experimentais indicaram um bom equilíbrio cromático geral ao utilizar o método *Gray World* em diferentes cenários e limiares[cite: 818, 827].

## Tecnologias Utilizadas

* [cite_start]**Linguagem:** Python [cite: 277]
* [cite_start]**Processamento de Imagem:** OpenCV (`cv2`), Scikit-image (`skimage`) [cite: 19, 347, 508, 600]
* [cite_start]**Manipulação de Dados e Matemática:** NumPy, SciPy [cite: 22, 599]
* [cite_start]**Visualização Gráfica:** Matplotlib [cite: 21, 175, 176]
* [cite_start]**Ambiente:** Google Colab integrado ao Google Drive [cite: 16-18]
