PySpark Notas
=============

Colección de apuntes de los conceptos más importantes que me han ayudado a comprender y aplicar spark

Spark y Hadoop
======================

**Componentes de Hadoop**

Hadoop es una tecnología que permite procesar eficazmente grandes volúmenes de datos, facilita la creación de clústeres de hardware de consumo para analizar conjuntos de datos masivos en paralelo.

HDFS (Hadoop Distributed File System): Sistema que permite almacenar los datos locales de su cluster en bloques de gran tamaño.

YARN (Yet Another Resource Negotiator): Componente que se encarga de la administracion de los recursos, supervisa todos los recursos del cluster y se asegura de que se asignen de forma dinamica a din de completas las tareas del trabajo de procesamiento.

MapReduce: Es un motor de ejecucion que permite dividir los trabajos en tareas mas pequenas que se pueden distribuir entre nodos, es tolerante a fallos. Si se produce un fallo en un servidor que está ejecutando una tarea, Hadoop la ejecuta en otro equipo hasta que se finalice.

**¿Cómo funciona Hadoop?**

Hadoop permite la distribución de conjuntos de datos en un clúster de hardware básico. El procesamiento se realiza en paralelo en varios servidores de forma simultánea.

Los clientes de software ingresan datos en Hadoop. HDFS maneja los metadatos y el sistema de archivos distribuido. Luego, MapReduce procesa y convierte los datos. Por último, YARN divide los trabajos entre los clústeres de procesamiento.

Todos los módulos de Hadoop están diseñados con la suposición fundamental de que las fallas de hardware de máquinas individuales o en bastidores son comunes y que el framework debe administrarlas de forma automática en el software.

**¿Cómo funciona MapReduce?**

MapReduce divide el trabajo de procesamiento de grandes volúmenes de datos en tareas más pequeñas (Map), organiza y agrupa los resultados (Shuffle and Sort), y luego los reduce a un resultado final (Reduce).

Esto permite que el procesamiento sea escalable y se realice en paralelo en varios nodos del clúster, lo que hace que MapReduce sea muy eficiente para manejar grandes cantidades de datos.


**Spark**

Spark se creó para superar las limitaciones de Hadoop MapReduce, ofreciendo un sistema más rápido, flexible y adecuado para una gama más amplia de aplicaciones de procesamiento de datos. Aunque Hadoop sigue siendo una tecnología fundamental en el ecosistema de Big Data, Spark se ha convertido en una herramienta clave debido a su capacidad para realizar procesamiento en memoria, soportar computación iterativa, y ofrecer APIs más fáciles de usar.

**Spark Core**

RDD (Resilient Distributed Dataset), es una colección de objetos distribuidos de manera segura y eficiente en un clúster. Los RDDs permiten realizar operaciones en paralelo y gestionar los fallos automáticamente.

Spark Core es el núcleo esencial de Apache Spark, ofreciendo las capacidades fundamentales para procesar grandes volúmenes de datos distribuidos. Mediante el uso de RDDs y una API rica en transformaciones y acciones, Spark Core permite realizar análisis y procesamiento de datos de manera eficiente y escalable.

**Spark SQL**

 Spark SQL es una poderosa herramienta dentro de Apache Spark para trabajar con datos estructurados. Ofrece una interfaz SQL familiar y un potente API de DataFrames que permite realizar consultas y operaciones complejas de manera eficiente. Permite la carga de datos, realizar consultas SQL, calcular agregaciones, y utilizar funciones SQL en DataFrames, lo que hace que Spark SQL sea extremadamente flexible y adecuado para una amplia gama de tareas de análisis de datos.
