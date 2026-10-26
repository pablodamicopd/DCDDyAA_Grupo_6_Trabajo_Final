# Predicción de Intención de Compra en E-Commerce

**Diplomatura en Ciencia de Datos y Análisis Avanzado — UTN.BA**  
**Grupo N° 6**  
* **Integrantes:** Cicchitti Silvana, D'Amico Pablo Ezequiel, Maguina Carla, Morrone Marianela, Rey Pablo Agustín.

---

## 📌 Descripción del Proyecto
Desarrollo de un modelo de clasificación supervisada para predecir si una sesión de navegación web culminará en transacción (`Revenue = True`), optimizando la asignación de recursos comerciales e incentivos en tiempo real.

---

## ⚙️ Metodología y Hallazgos Clave
* **Marco metodológico:** CRISP-DM.
* **Mitigación de Data Leakage:** Se excluyó la variable `PageValues` por riesgo severo de incorporar información post-conversión, garantizando la viabilidad del modelo en un entorno de producción real.
* **Modelo Seleccionado:** Regresión Logística con umbral de decisión calibrado en **0,491** para priorizar la captura de compradores frente a la asimetría de costos del negocio.
* **Desempeño del Modelo (Sin PageValues):** Recall: 75,13% | Precision: 25,49% | F1-Score: 38,06% | ROC-AUC: 0,7344 | PR-AUC: 0,3192.
* **Impacto Comercial:** Al intervenir sobre el **Top 20%** de las sesiones con mayor probabilidad estimada, el modelo captura al **44,0% de los compradores reales** (Lift de **2,20x** frente al azar), permitiendo contactar **92 compradores adicionales** con el mismo presupuesto.

---

## 📁 Contenido del Repositorio
* `DCDDyAA_Grupo_6_Trabajo_Final.ipynb`: Notebook principal con el desarrollo técnico completo (análisis exploratorio, pruebas de Chi-cuadrado, modelos evaluados, calibración de umbrales y curvas de ganancia/lift).
* `online_shoppers_intention.csv`: Dataset original de navegación web utilizado para entrenar y evaluar los modelos.
* `DCDDyAA_Grupo_6_Trabajo_Final.pdf`: Informe ejecutivo final del trabajo integrador.

---

## 🚀 Cómo ejecutar

### Google Colab (Recomendado)
1. Abrir `DCDDyAA_Grupo_6_Trabajo_Final.ipynb` en Google Colab.
2. Subir el archivo `online_shoppers_intention.csv` al entorno de trabajo (pestaña lateral de Archivos).
3. Ir al menú superior y seleccionar **Entorno de ejecución → Ejecutar todas**.

### Entorno Local
Clonar el repositorio y configurar el entorno virtual:
```bash
git clone [https://github.com/pablodamicopd/DCDDyAA_Grupo_6_Trabajo_Final.git](https://github.com/pablodamicopd/DCDDyAA_Grupo_6_Trabajo_Final.git)
cd DCDDyAA_Grupo_6_Trabajo_Final

python -m venv .venv
# Windows: .venv\Scripts\activate
# Linux/Mac: source .venv/bin/activate

# Instalar dependencias
pip install pandas numpy scikit-learn matplotlib seaborn scipy xgboost jupyter

# Iniciar la notebook
jupyter notebook DCDDyAA_Grupo_6_Trabajo_Final.ipynb
