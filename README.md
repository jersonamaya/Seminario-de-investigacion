# 🌽🫘 Detección de Enfermedades en Cultivos — CAE

Sistema de detección automática de enfermedades en **maíz** y **frijol** usando autoencoders convolucionales. Se entrena solo con hojas sanas y detecta anomalías por error de reconstrucción.

## Enfermedades detectadas

| Cultivo | Enfermedades |
|---------|-------------|
| Maíz    | Tizón tardío, Mancha gris, Roya común |
| Frijol  | Antracnosis, Mancha angular, Roya |

## Instalación

```bash
git clone https://github.com/jersonamaya/Seminario-de-investigacion.git
cd Seminario-de-investigacion
pip install -r requirements.txt
```

## Uso rápido

```python
from model.autoencoder import ConvAutoencoder

ae = ConvAutoencoder.load('checkpoints/autoencoder_maiz.h5')
result = ae.predict('hoja.jpg')

print("Enferma" if result['anomaly'] else "Sana ✓")
```

## Resultados esperados

| Métrica | Objetivo |
|---------|----------|
| Accuracy | ≥ 90% |
| AUC-ROC  | ≥ 0.93 |
| Inferencia | < 100 ms |

## Tecnologías

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=flat&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.10+-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Google Colab](https://img.shields.io/badge/Colab-GPU-F9AB00?style=flat&logo=googlecolab&logoColor=white)

## Autor

**Jerson Ricardo Lopez Amaya** · UNAH · jerson.amaya@unah.hn


