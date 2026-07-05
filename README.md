# Proyecto Final Tópicos D: Predicción de Enfermedad Cardíaca

**Asignatura:** Tópicos D  
**Carrera:** Ingeniería en Computación e Informática - Universidad de Magallanes  
**Profesor:** Dr. Carlos Arias Méndez  
**Integrantes:** Felipe Cárcamo Oyarzún, Christofer Gutiérrez Pacheco  

## Descripción del Proyecto
Este proyecto desarrolla un flujo metodológico de Machine Learning para predecir la presencia o ausencia de enfermedades cardíacas basándose en 13 atributos clínicos (presión arterial, colesterol, etc.). El objetivo es aplicar y evaluar comparativamente modelos de aprendizaje supervisado, centrándose en el control del *overfitting*.

## Conjunto de Datos
Se utilizó el **Heart Disease Dataset** (heart.csv). Tras el análisis exploratorio (EDA) y la limpieza de 723 registros duplicados, se obtuvo una muestra de 302 pacientes únicos con un balance de clases óptimo (54.3% enfermos, 45.7% sanos).

## Metodología
1. **Preprocesamiento:** Limpieza de duplicados, división de los datos en Entrenamiento (60%), Validación (20%) y Prueba (20%), y escalado de atributos con `StandardScaler`.
2. **Modelos Evaluados:** 
   - Árbol de Decisión (Decision Tree)
   - Random Forest (Bosque Aleatorio)
3. **Sintonización:** Ajuste de hiperparámetros (`max_depth=3` y `n_estimators=200`) para combatir el sobreajuste.

## Resultados Principales
El modelo ganador fue el **Random Forest Regulado**, el cual logró mitigar el overfitting presente en los modelos base. Las métricas finales en el conjunto de prueba (Test) completamente aislado fueron:
- **Accuracy:** 80.32%
- **Precision:** 83.87%
- **Recall:** 78.78%
- **F1-Score:** 81.25%

## Estructura del Repositorio
- `notebook.ipynb`: Código fuente con el análisis exploratorio, entrenamiento, visualización y evaluación de los modelos.
- `Informe_Final_Proyecto.pdf`: Documento detallado con la justificación clínica, análisis técnico, implicaciones éticas y conclusiones.
- `Dataset/`: Carpeta que contiene el archivo `heart.csv`.

## Conclusión y Ética
El modelo demostró ser robusto y estable. No obstante, se enfatiza que este sistema actúa estrictamente como una herramienta de tamizaje complementaria y en ningún caso sustituye el diagnóstico clínico de un profesional de la salud.