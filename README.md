
# Challenge Telecom X: parte 2

## **Propósito del análisis realizado.**
Analizar, en base a los datos ya tratados, variables relevantes y crear modelos de machine learning para la predicción del churn, con el objetivo de prever el riesgo de la fuga de clientes y tomar decisiones estratégicas en base a ello.

## **Estructura del proyecto y organización de los archivos**

1. **Preparación de los Datos**
   - Extracción del Archivo Tratado
   - Eliminación de columnas redundantes y Encoding
   - Verificación de la proporción de Churn y Balanceo de Clases
2. **Correlación y Selección de Variables**
   - Análisis de Correlación
   - Análisis Dirigido
3. **Modelado Predictivo**
   - Separación de datos
   - Normalización de Datos
   - Creación de modelos
   - Evaluación de los modelos
4. **Interpretación y Conclusiones**
   - Interpretación de resultados
   - Conclusiones

## Descripción del proceso

La clasificación de variables se realizó en la parte 1, clasificándolas como variables numéricas, variables categóricas binarias y variables categóricas multiclase. A estas últimas se les aplicó One Hot Encoding durante la parte 1. 

Después se separaron los datos en conjuntos de entrenamiento y prueba y se normalizaron. Esto ya que las escalas de algunas variables poseían diferencias muy pronunciadas, lo que habría afectado el rendimiento de los modelos. 

Después se crearon los modelos, se entrenaron y se probaron. Los modelos creados fueron Random Forest y KNN, además del modelo Dummy como modelo baseline. Se escogieron estos modelos porque KNN requiere normalización, lo que permitiría contrastar modelos con diferencias claras. Se ajustaron manualmente para mejorar el desempeño discretamente y luego se analizó su desempeño. Se crearon las matrices de confusión de los modelos y se analizaron sus métricas para evaluar su desempeño. Las matrices de confusión de ambas fueron similares entre sí y un análisis visual preliminar indica que ambos tienen buen desempeño, pero que Random Forest era mejor: la matriz de KNN presentó mayor cantidad de falsos positivos. Esto lo vuelve menos confiable en la práctica. 

## **Ejemplos de gráficos e insights obtenidos**
![Análisis dirigido](https://github.com/remBits/Challenge-Telecom-X-parte-2/blob/main/reportes_graficos/analisis_dirigido.png)
![Matrices de confusión](https://github.com/remBits/Challenge-Telecom-X-parte-2/blob/main/reportes_graficos/matrices_confusion.png)
![Importancia de variables](https://github.com/remBits/Challenge-Telecom-X-parte-2/blob/main/reportes_graficos/importancia_variables.png)

- El factor más importante fueron los contratos mes a mes. 
- Los servicios adicionales tienen especial relevancia.
- El mejor modelo fue Random Forest: es robusto y balanceado.
- Se recomienda priorizar los contratos a largo plazo, promover la contratación de servicios adicionales, promover la permanencia entre los clientes y, finalmente, examinar, diagnosticar e implementar mejoras en el servicio de internet por fibra óptica.
## **Instrucciones para ejecutar el notebook**

1. Clonar este repositorio:
   ```bash
   git clone https://github.com/remBits/Challenge-Telecom-X-parte-2.git
```
2. Acceder a la carpeta del proyecto:
   ```bash
   cd Challenge-Telecom-X-parte-2
```
3. Instalar librerías:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```
4. Ejecutar Notebook: 
```bash
jupyter notebook
```
5. Abrir el archivo Challenge-Telecom-X-parte-2.ipynb y ejecutar las celdas.



