# Atividade - Segmentação Semântica

## Passos recomendados para instalação do ambiente de treinamento:
* ``conda``, Python 3.10 and CUDA 11.8
* Testado com essas configurações e funcional
  
> ```bash
> conda create --name deepl python=3.10 --no-default-packages
> conda activate deepl
> ```

> ```bash
> pip install torch torchvision --index-url https://download.pytorch.org/whl/cu118
> pip install -r requirements.txt
> ```

## Hands-on
A atividade consiste em realizar algumas tarefas principais condizentes com o pipeline padrão adotado em problemas de segmentação semântica e implantação.

Seu objetivo geral é treinar um modelo de segmentação semântica, implantar esse modelo no seu smartphone. Por fim, enviar um print e o link do seu repositório pelo classroom.


---
## Sugestões de implementação para treinamento

### Etapa 1: Introdução e treinamento de segmentação

* **Dataset**: Oxford-IIIT Pet (disponível em ``torchvision.datasets.OxfordIIITPet`` por exemplo)
  *  Utilizar recorte reduzido do dataset para facilitar treinamento (``torch.utils.data.Subset`` por exemplo)
* **Modelo sugerido**: UNet

### Etapa 2: Avaliação de desempenho e métricas
* IoU
* Acurácia
* Possível de calcular essas métricas com ``torchmetrics``

### Etapa 3: Visualização dos resultados
* Implementar código para aplicativo de smartphone
* Realizar predição no aplicativo e exibir a máscara sobreposta à foto ou vídeo

## Entregáveis
* Print do aplicativo funcionando com a segmentação em imagem ou vídeo
* Link do repositório com a sua implementação
