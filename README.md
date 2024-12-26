# 🦁 Detecção de Animais Africanos com YOLO

Este projeto utiliza YOLOv8 para detectar diferentes animais africanos em imagens. O modelo foi treinado para identificar:
- 🦬 Buffalo
- 🐘 Elephant
- 🦏 Rhino
- 🦓 Zebra

## 📋 Pré-requisitos

- Python 3.8+
- GPU (recomendado)
- Bibliotecas necessárias (instale usando o arquivo requirements.txt):
```bash
pip install -r requirements.txt
```

## 🗂️ Estrutura do Projeto
```bash
dio-yolo-segmentacao/
├── datasets/african-wildlife/    # Dataset
├── notebooks/                    # Jupyter notebooks
├── predict/                      # Resultados das predições
├── runs/detect/                  # Logs e pesos do modelo
└── requirements.txt
```

## 🚀 Como Usar

## 1. Preparação do Ambiente
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/dio-yolo-segmentacao.git
cd dio-yolo-segmentacao

# Instale as dependências
pip install -r requirements.txt
```

## 2. 🏋️‍♂️ Treinamento do Modelo

Execute o notebook yolo-segmentacao.ipynb:

Carrega o dataset African Wildlife
Configura o modelo YOLOv8
Treina por 100 épocas
Salva os melhores pesos

## 3. 🔍 Fazendo Predições
Usando o Notebook
Abra yolo-predict.ipynb e siga as instruções para:

Carregar imagens
Fazer predições
Visualizar resultados

Usando Linha de Comando
```bash
# Para uma única imagem
yolo predict model=runs/detect/train/weights/best.pt source=sua_imagem.jpg
```

## Para várias imagens em uma pasta
```bash
yolo predict model=runs/detect/train/weights/best.pt source=pasta_imagens/
```

## Para usar webcam
```bash
yolo predict model=runs/detect/train/weights/best.pt source=0
```

## 📊 Resultados
O modelo foi treinado com:

1052 imagens de treino
225 imagens de validação
227 imagens de teste

## 💡 Dicas

Ajuste o threshold de confiança para melhorar as detecções:
```bash
pythonCopymodel.predict(source='imagem.jpg', conf=0.25)  # Padrão é 0.25
```

## Para melhores resultados:

Use imagens bem iluminadas
Evite imagens muito distantes
Mantenha resolução similar ao treino (640x640)

## 🤝 Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para:

Reportar bugs
Sugerir melhorias
Enviar pull requests

## 📝 Licença
Este projeto está sob a licença MIT.

Desenvolvido para o curso da DIO 🚀
 
