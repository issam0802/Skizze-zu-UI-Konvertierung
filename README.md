# Skizze-zu-UI-Konvertierung
the code provided by [mzbac](https://github.com/mzbac/sketch2code),  and I used it for project work purposes.

Dieses Repository enthält den Quellcode für ein Deep Learning-Modell zur automatischen Konvertierung von UI-Skizzen in UI-Elemente. Das Modell verwendet Convolutional Neural Networks (CNN) und Recurrent Neural Networks (RNN), um Skizzen in Benutzeroberflächenelemente wie Schaltflächen, Textfelder und Listen umzuwandeln.

![Sketchtocode](https://github.com/ashnkumar/sketch-code/blob/master/header_image.png)

## Model architecture
![Model architecture](https://raw.githubusercontent.com/mzbac/sketch2code/master/model_architecture.png)

## Installieren Dataset

Bevor Sie das Modell ausführen können, müssen Sie das Dataset installieren. Das Dataset enthält eine Sammlung von UI-Skizzen, die verwendet werden können, um das Modell zu trainieren.
1. Klonen Sie das Repository: git clone https://github.com/username/repository.git
2. Navigieren Sie zum Verzeichnis "data": cd data
3. Führen Sie das Skript "get_data.sh" aus: 
```
bash get_data.sh
```
## Install dependencies
````
pip install -r requirements.txt
````
## Load pre-trained weights
Um das Modell mit den vortrainierten Gewichten zu verwenden, laden Sie die Gewichte von der [Link to pre-trained weights] herunter und speichern Sie sie im Ordner "weights".

```
encoder = torch.load('model_weights/encoder_resnet34_0.060610368847846985.pt')
decoder = torch.load('model_weights/decoder_resnet34_0.060610368847846985.pt')
```

## Pre-trained weight preview:
![Pre-trained weight preview](https://raw.githubusercontent.com/mzbac/sketch2code/master/image_sketch2code_loss_0.061.png)

## Pre-trained model's BLEU score
Das vortrainierte Modell wurde auf einer Reihe von UI-Skizzen trainiert und wurde anhand des BLEU-Scores evaluiert. Der BLEU-Score ist eine Metrik zur Bewertung der Qualität von maschinell übersetzten Texten, die auch für die Bewertung von Textgenerierungsmodellen verwendet wird.
````
Der BLEU-Score des vortrainierten Modells beträgt 0.9741881046090399
.
````
