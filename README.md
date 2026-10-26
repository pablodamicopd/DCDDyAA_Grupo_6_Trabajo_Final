# DCDDyAA_Grupo_6_Trabajo_Final
Repositorio del trabajo final DCDDYAA, equipo 6.
# Predicción de Intención de Compra en E-Commerce

**Diplomatura en Ciencia de Datos y Análisis Avanzado — UTN.BA**  
**Grupo N° 6**  
* Integrantes: Cicchitti Silvana, D'Amico Pablo Ezequiel, Maguina Carla, Morrone Marianela, Rey Pablo Agustín.

---

## 📌 Descripción del Proyecto
Desarrollo de un modelo de clasificación supervisada para predecir en tiempo real si una sesión de navegación web culminará en transacción (`Revenue = True`), optimizando la asignación de recursos comerciales y reduciendo el abandono de usuarios.

## ⚙️ Metodología y Hallazgos Clave
* **Marco:** Metodología estándar CRISP-DM.
* **Mitigación de Data Leakage:** Se excluyó la variable `PageValues` por riesgo severo de incorporar información post-conversión, garantizando la viabilidad en producción.
* **Modelo Final:** Regresión Logística con umbral de decisión calibrado en **0,5055** sobre un set de validación independiente.
* **Desempeño en Test:** Recall: 72,77% | Precision: 25,30% | F1-Score: 37,54%.
* **Impacto Comercial:** Al intervenir sobre el **Top 20%** de las sesiones con mayor probabilidad, se captura al **44,0% de los compradores reales** (Lift de 2,20x frente al azar).

## 📁 Contenido del Repositorio
* `notebook_final.ipynb`: Código fuente completo con análisis exploratorio, modelado, calibración de umbrales y gráficos.
* `Informe_Final_Grupo_6.pdf`: Informe ejecutivo del trabajo integrador.

## 🔗 Fuente de Datos
* [UCI Online Shoppers Purchasing Intention Dataset](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset)
