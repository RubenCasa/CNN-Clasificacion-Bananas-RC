# 🍌 Clasificación de Bananas con CNN

 <img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/4eb0b22e-a59c-4b94-bd14-efb0ca06dd72" /> ![0004](https://github.com/user-attachments/assets/8565a478-993f-4bfc-b2fc-2f92a5413cc0) 



Proyecto de clasificación de imágenes de bananas usando Redes Neuronales Convolucionales (CNN) y Transfer Learning.

##  Descripción

Este proyecto compara dos enfoques para clasificar bananas según su estado:
- **CNN desde cero**: Red neuronal entrenada sin conocimiento previo
- **Transfer Learning**: Usando ResNet18 preentrenado en ImageNet

### Clases del Dataset
 ## MI PROPIO DATASET
| Clase | Cantidad |
|-------|----------|
| NORMAL | 26 imágenes |
| DAÑADO | 26 imágenes |
| MUY DAÑADO | 26 imágenes |
| **Total** | **78 imágenes** |

## Estructura del Proyecto

```
├── CNN_Clasificacion_Bananas.ipynb  # Notebook principal
├── FOTO BANANA/                     # Dataset de imágenes
│   ├── NORMAL/
│   ├── DAÑADO/
│   └── MUY DAÑADO/
├── curvas_cnn.png                   # Gráficas CNN
├── curvas_transfer.png              # Gráficas Transfer Learning
└── comparacion_modelos.png          # Comparación final
```

## Arquitectura CNN

```
Bloque 1: Conv2D(3→32) → ReLU → MaxPool
Bloque 2: Conv2D(32→64) → ReLU → MaxPool
Clasificador: Flatten → Linear(128) → ReLU → Linear(3)
```

## Hiperparámetros

| Parámetro | Valor |
|-----------|-------|
| Learning Rate | 0.001 |
| Batch Size | 16 |
| Epochs | 15 |
| Optimizador | Adam |

## Resultados

| Modelo | Val Accuracy | Observaciones |
|--------|--------------|---------------|
| CNN desde cero | 91.67% | Presenta overfitting |
| Transfer Learning | 91.67% | Más estable |

##  Requisitos

```bash
pip install torch torchvision matplotlib numpy
```

##  Conclusiones

1. **Transfer Learning** es mejor para datasets pequeños
2. Ambos modelos alcanzan ~91% de accuracy
3. Transfer Learning muestra entrenamiento más estable
4. La reproducibilidad se garantiza fijando la semilla (seed=42)

##  Autor

Ruben Dario Casa.

##  Licencia

Este proyecto es para fines educativos.


