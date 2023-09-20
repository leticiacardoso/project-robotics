# YOLO (You Only Look Once):
O YOLO é um método de detecção de objetos em tempo real que se destaca por sua velocidade e precisão. Em vez de dividir o processo de detecção em várias etapas, como muitos outros métodos, o YOLO trata a detecção de objetos como um problema de regressão para localizar diretamente as caixas delimitadoras (bounding boxes) e prever as classes dos objetos.

## Principais características do YOLO
- Detecção em uma única passagem (single pass): examina a imagem inteira em uma única passagem, em vez de usar regiões de interesse.

- Caixas de Ancoragem (Anchors): usa caixas de ancoragem para prever as caixas delimitadoras (bounding boxes). Cada célula na grade de detecção é responsável por prever um conjunto de caixas de ancoragem.

- Classificação Simultânea: YOLO prevê as classes e localiza as caixas delimitadoras (bounding boxes) em uma única saída.

- Camadas de convolução: Usa camadas de convolução para detectar objetos em várias escalas e níveis de resolução.

- Não Dependente de Propostas: Não requer geração prévia de propostas de regiões de interesse, oque o torna mais rápido.

- Aplicabilidade em Tempo Real: É amplamente usado para aplicações que requerem detecção em tempo real.

## A abordagem - abordagem de Detecção de Objetos

A abordagem YOLO pode ser utilizada para identificar e classificar as garrafas em tempo real conforme elas passam por uma esteira, por exemplo.

## Funcionamento (ideia de código para o projeto):
- A câmera captura a imagem do possível residuo

- A imagem é então processada pelo modelo YOLO treinado especificamente para detectar garrafas

- O modelo YOLO localiza as garrafas na imagem e atribui uma classe a cada uma delas

- Com base nas detecções, um sistema de acionamento automatizado se direciona para a coleta das garrafas (Eye-to-Hand)

## Exemplos de objetos que podem ser identificados
- Garrafas de Plástico: Garrafas de água, refrigerante ou outras bebidas em garrafas de plástico, ter uma forma e textura distintas que podem ser um desafio para detectar

- Garrafas de Vidro: Geralmente Garrafas de bebidas em vidro têm uma forma única

## Próximos passos e resalvas
- continuar com ajustes nos parâmetros para melhorar a precisão

- modelos de detecção de objetos podem ser sensíveis a variações nas condições de iluminação, ângulos de visão e tipos de garrafas. A precisão do modelo depende da qualidade e diversidade do conjunto de dados de treinamento

- como o modelo é relativamente grande, ele requer recursos de hardware suficientes para executar eficientemente, especialmente em tempo real, tornando árduo rodar os testes na raspberry