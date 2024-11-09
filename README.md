Projeto Integrador Ciclo 2 - Ferramentas Computacionais

Índice de Cursos - Processamento de Imagens

Este projeto foi desenvolvido para aplicar técnicas de processamento de imagens ao índice de cursos, usando a biblioteca OpenCV. O objetivo é transformar visualmente as imagens para 
facilitar a identificação de quais cursos foram visualizados. Este README explica o funcionamento do código e como ele processa as imagens por meio de várias etapas.

Objetivo

Automatizar o processamento de imagens para gerar uma série de transformações, como binarização, redimensionamento, realce e filtragem, permitindo uma análise visual mais prática dos cursos visualizados ou não.

Requisitos

Python 3.x: Linguagem utilizada no desenvolvimento.

OpenCV (cv2): Biblioteca essencial para o processamento de imagens.

Para instalar o OpenCV: pip install opencv-python

pip install opencv-python

Estrutura do Projeto

O projeto utiliza dois diretórios principais:

input_dir: Diretório onde as imagens de entrada (originais) são armazenadas.

output_dir: Diretório onde as imagens processadas são salvas com versões diferentes conforme as transformações aplicadas.
Explicação das Etapas de Processamento de Imagens

O código percorre todas as imagens presentes no diretório de entrada e realiza as seguintes etapas de processamento:

Conversão para Escala de Cinza

As imagens coloridas são convertidas para escala de cinza. Esse processo reduz as informações de cor, facilitando etapas de processamento subsequentes que não necessitam da complexidade das cores.

Conversão para Imagem Binária

A imagem em escala de cinza é binarizada. Esse passo aplica um limiar, separando os pixels em apenas dois valores (preto e branco). Essa simplificação facilita a visualização em casos onde o contraste entre áreas claras e escuras é essencial.

Transformações Geométricas

Rotação: Cada imagem é rotacionada 90 graus no sentido horário, o que pode ser útil para alinhar imagens em uma orientação específica.

Redimensionamento: As imagens são redimensionadas para a metade de sua altura e largura originais, economizando espaço e tornando o processamento mais rápido em futuras análises.
Realce de Contraste com Equalização de Histograma
Esta etapa aumenta o contraste da imagem, permitindo que detalhes em áreas escuras ou claras se destaquem. É especialmente útil para imagens com contraste baixo.

Filtragem

Suavização: Um filtro de suavização é aplicado para reduzir ruídos, resultando em uma imagem mais "limpa".
Detecção de Bordas: Utilizando o método de Canny, são identificadas e evidenciadas as bordas da imagem, destacando transições bruscas de intensidade e facilitando a análise de contornos.

Execução do Projeto

Para executar o projeto:

Preparo das Imagens de Entrada: Coloque todas as imagens que deseja processar na pasta especificada como input_dir.

Processamento: Ao executar o script, cada imagem passa pelas etapas mencionadas, gerando versões processadas em output_dir.

Visualização: As imagens processadas têm diferentes nomes que indicam as transformações aplicadas, como binary_nome_imagem.jpg para as imagens binárias ou rotated_nome_imagem.jpg para as imagens rotacionadas.

Resultados
As imagens processadas são salvas no diretório de saída, com várias versões de cada imagem, facilitando a análise visual. Esse processo visa criar uma base visual que permite identificar rapidamente o progresso nos cursos e se eles foram ou não visualizados.