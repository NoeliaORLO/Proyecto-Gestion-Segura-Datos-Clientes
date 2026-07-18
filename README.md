# Proyecto: Gestión Segura de Datos de Clientes 👨🏻‍💻
Breve proyecto enfocado en aplicar la ética y la privacidad a un csv de datos de clientes.

## ¿ Qué pretende este proyecto?
Con este proyecto pretendo volcar todos los conocimientos adquiridos en el ámbito de la ética y la privacidad en Data Science. Para ello, aplico técnicas de anonimización, pseudonimización y balanceo 
de datos a un csv de clientes que contiene datos relativos al nombre, dirección, edad, categoría y salario. 

## Resumen del proyecto
Trabajo con un dataset que contiene datos ficticios de clientes relativos a su nombre, dirección, edad, categoría y salario, los cuales permiten identificarlos personalmente. Es por ello que se deben 
aplicar técnicas de anonimización y pseudonimización para preservar la privacidad de las personas. 

Respecto a la anonimización, utilizo las técnicas de redondeo, en el campo de edad; ruido aleatorio, en el campo de salario; y permutación (shuffling) en el campo de dirección. 

Para aplicar la pseudonimización utilizo la técnica de hashing, generando códigos hash para cada nombre. Podría haber utilizado la técnica de Tokens, pero al no ser datos que se necesiten recuperar 
(como si pasa por ejemplo en el ámbito de la salud o de la seguridad), he preferido utilizar esta técnica y sustituir toda la columna de nombre por los códigos hash.

También es importante mirar si hay un desbalance de datos en el csv, lo cual ocurre respecto a la columna "categoría", de la cual no hay la misma representación de la clase 0 que de la 1. Por lo tanto,
aplico un balanceo de datos mediante el agrupamiento por categoría y la posterior creación de un grupo balanceado donde se igualan las muestras por categoría en 100, aplicando el remuestreo (oversampling con reemplazo) 

## Para ejecutar el script...
Se necesita tener un intérprete de Python que contenga las librerías Pandas, Numpy, Seaborn, Matplotlib, Hashlib y Scikit-learn. En mi caso yo uso conda (obtenible mediante la descarga de Anaconda), ejecutando el 
notebook desde Jupyter Notebook o VS Code.
