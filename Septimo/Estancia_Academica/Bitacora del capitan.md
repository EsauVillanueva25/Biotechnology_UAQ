# Bitácora del capitan

## lunes 23-06-2025

El dia lunes aprendí sobre teoría de graficas. Aprendí sobre los nodos, los links y el grado de  cada nodo (cuantos links tiene cada nodo), el promedio de grado <k>, el grado de entrada y salida en graficas  dirigidas; el <k> de loas graficas dirigidas, la distribución de grado (saber si en nuestra grafica se tienen muchos nodos con pocos links o con muchos).

## Martes 24-06-2025

Comencé a aprender a programar en Unix. Comencé con conocer la terminal, buscar archivos, 
crear y borrar directorios, archivos y carpetas; copiar carpetas y archivos con el uso de la terminal, aprendí a crear pipelines y como programar la terminal para buscar, clasificar y mostrar resultados de datos almacenados.

## Miercoles 25-06-2025

El día de hoy se comenzó repazando el tema de conjuntos, donde se vieron los temas de 
unión, intersección, resta y resta simetrica. depúes se paso al la base de teória de grafos, que en el primer día empece a ver, me explicaron las bases de un grafo; vi definición de un grafo, la definición de un producto cartesiano (A x B), el tamaño de un grafo, definición de grafo dirigido y no dirigido. Con estas definiciones construí mi primer grafo (orgulloso de mi), aprendí los tipos de grafos, aprendi a construir subgrafos y subgrafos inducidos. 
En la parte de programación, seguí aprendiendo sobre Unix, donde aprendí a crear bucles para mover archivos, crearlos y clasificar los datos de archivos. Para esto tambien logré entender y hacer diagramas de flujo que son las bases de los bucles. 
Casi se nos inunda el laboratorio y se tuvo que desconectar las computadoras, reguladores y todo tipo se aparato electronico (estuvo cerca). 

## Jueves 26-06-2025

El día de hoy se volvio a comenzar con teoría de grafos. Donde se aprendío la definición de adyacencia, la vecindad o neingborhood (para un G dirigido o no dirigido), el grado de un vértice (directed or not) y el grado total. Además se realizó el ejercicio sig. demuestra "sea G un grafo no dirigido. El número de vértices de grado impar siempre es par", donde se demostro graficamente y por medio de inferencias que es cierto. Por ultimo de este tema, se realizó 
otro ejercicio similar "Sea un grafo G, el número n de vértices con grado par es impar" el cual se analizó y se respondió, sin embargo, se corriguió ya que la resulución correcta era falso y no se llego a esa conclusión. 
Por otra parte, se terminó de aprender Unix, ya que este se termino el temario. Se aprendió a hacer bucles (for), se aprendió a hacer scripts y a buscar archivos (grep y find).  Por ultimo se empezó a leer sobre los temas nuevos de teoria de grafos, siendo estos repasados y entendidos el día de mañana. 

## Viernes 27-06-2025

Hoy se comenzó con leer las definiciones de camino (path), ciclo (cycle), caminata (walk) y sendero (trail) en teoria de grafos. Se comprendieron y realizaron ejercicios sobre estas definiciones, despúes de esto se aprendió la demostración por inducción (caso base, paso inductivo y conclusión), con esto se realizó la proposición sobre las definiciones del principio.
Por último se empezó con un ejercicio de Unix, el cual consiste en organizar y encontrar las especies que transcriben ciertas proteínas post-lesión.

## Lunes 30-06-2025

El día de hoy se termino de ver teoría de grafos (la introducción). Se aprendio las definiciones de conexo, se resolvieron los proposiciones, una de conexion y otra sobre el tour de euler; además se aprendió la def. de este ultimo. Por ultimo se seguieron con los ejercicios prácticos de Unix,aunque por el momento no he avazado del  primer ejercicio, ya que no comprendo el ejercicio, mañana preguntare y pedire ayuda. 

## Martes 1-07-2025

El dia de hoy se terminaron varios ejercicios que ya se habian empezado de Unix. 

```bash
# Ejercicio 1 identificación de proteinas con genes
# Regeneración de la cola a las 48 hrs post-lesión
# ¿Cuántos genes expresados a la alta?
2327 datos_up_after_kallisto_output_filter.txt
# ¿Cuántos a la baja?
939 datos_down_after_kallisto_output_filter.txt
# Lista de comandos para el ejercicio 1
# Comparación de Up con entap_result
grep -F -f datos_up_after_kallisto_output_filter.txt entap_results.tsv >> ejercicio_1_up
# Comparación de Down con entap_result
grep -F -f datos_down_after_kallisto_output_filter.txt entap_results.tsv >> ejercicio_1_down

# Ejercicio 2
# Este ejercicio se usa el archivo fasta de D.laeve
# ¿Cuántas proteínas se predijieron  según el archivo?
   grep -c "TRINITY_DN*" Deroceras_laeve.fa
   grep  "TRINITY_DN*" Deroceras_laeve.fa | wc -l
      42742 proteínas predichas
# Lista de comandos para el ejercicio 2
# Archivo D.laeve.fa
# ¿Cuántas proteínas se predijieron?
grep  "TRINITY_DN*" Deroceras_laeve.fa | wc -l

# Ejercicio 5
# Extraer la fila de Database EggNOG Protein Domains de entap_results
    cat entap_results.tsv | tr -s [:space]  | cut -f 45 > Database_EggNOG_Protein_Dominias # tr -s da espacios
a un archivo que no los tenga o que no separe columnas
# Extraer los ids junto con su dominio
   cat entap_results.tsv | tr -s [:space]  | cut -f 1,45 > Database_EggNOG_Protein_Dominias

   cat Database_EggNOG_Protein_Dominias | tr "," "\v" > Database_EggNOG_Protein_Dominias

```

Además se aprendió lo básico para hacer un proyecto en Github, mañana se pondrá el codigo por que ya es tarde. 

# Miércoles 02-07-2025

El día de hoy se aprendió sobre teoria de graficas, donde se vieron las notaciones de mapeo de colores, la definición de un árbol  donde dontro de esta definición se vieron lo que es una raiz, un ancestro, un desendiente, un hijo y un progenitor, un ancestro incomprensible, extricto; la definición de hojas y un sub-árbol. 

Mañana se pegaron los comandos de Github y sobre los ejercicio de unix, y sobre la construcción de graficos de barras y radial en colab. 

## Jueves 03-07-2025

El día de hoy se aprendió sobre las *hojas* de los grafos (árboles) , los *sub-árboles*, el *ancestro mínimo común* (lca), como identificar  y calcular todos estos conceptos, y sobre una *raíz plantada*. 

En la parte de Unix, al fin de logró terminar los ejercicios 0,1 y 5 . 

```bash
# Para el ejercicio 0 y 1 se teinen dos archivos .txt con IDs de transcritos identificados como diferencialmente expredados (Up y Down) y otro .tsv con anotaciones (Entap_results)
# Ejercicio 0
# Regeneración de la cola a las 48 hrs post-lesión
# ¿Cuántos genes expresados a la alta?
2327 datos_up_after_kallisto_output_filter.txt
# ¿Cuántos a la baja?
939 datos_down_after_kallisto_output_filter.txt
#=====================================================
# Ejercicio 1 
# Para este ejercicio se utilizaron los comandos del dia 3
# link de repositorio Github (ponerlo despúes)

#====================================================
# Ejercicio 5 tener dos archivos donde se tengan los IDs de Up an Down con el respectivo dominio de proteína, se compararon los IDs de Up y Down con los de entap_results
# Lista de comandos para el ejercicio 5
# Extraer la fila de Database EggNOG Protein Domains de entap_results
    cat entap_results.tsv | tr -s [:space]  | cut -f 45 > Database_EggNOG_Protein_Dominias_temporal # tr -s da espacios
a un archivo que no los tenga o que no separe columnas
# Extraer los IDs junto con su dominio de las proteínas Up de kallisto del ejercicio 1
   cat ejercicio_1_Up | tr -s [:space]  | cut -f 1,45 > Temporal_Database_EggNOG_Protein_Dominance_Up_kallisto.txt
# Extraer los IDs junto con su dominio de las proteínas Down  de kallist del ejercicio 1
   cat ejercicio_1_down | tr -s [:space]  | cut -f 1,45 > Temporal_Database_EggNOG_Protein_Dominance_down_kallisto.txt
# Convertir Temporal_Database en separaciones por "\t"
  cat Temporal-entap | tr "," "\t" > Tab-Temporal-entap
# Comparar los IDs y juntarlos en un archivo .tsv
  grep -f Tab_Temporal_Database_EggNOG_Protein_Dominance_Up_kallisto.txt Tab-Temporal-entap > Real_Tab_Temporal_Database_EggNOG_Protein_Dominance_Up_kallisto.tsv
  grep -f Tab_Temporal_Database_EggNOG_Protein_Dominance_down_kallisto.txt Tab-Temporal-entap > Real_Tab_Temporal_Databas>
# Cambiar los tab en fila conservando el ID
  awk -F "\t" '{for(i=2;i<NF;i++) print$1"\t"$i}' Real_Tab_Temporal_Database_EggNOG_Protein_Dominance_Up_kallisto.tsv > Temp_Real_Tab_Temporal_Database_EggNOG_Protein_Dominance_Up_kallisto.tsv
  awk -F "\t" '{for(i=2;i<NF;i++) print$1"\t"$i}' Real_Tab_Temporal_Database_EggNOG_Protein_Dominance_down_kallisto.tsv > Temp_Real_Tab_Temporal_Database_EggNOG_Protein_Dominance_down_kallisto.tsv
# Agregamos los Headers perdidos en el paso anterior
  cat Temporal-entap | head -n 1 > head.tsv
  cat Temp_Real_Tab_Temporal_Database_EggNOG_Protein_Dominance_Up_kallisto.tsv >> head.tsv
  Temporal-entap | head -n 1 > Head_D.tsv
  cat Temp_Real_Tab_Temporal_Database_EggNOG_Protein_Dominance_down_kallisto.tsv >>Head_D.tsv
# Contamos los IDs
  cut -f 2 Up_Domeins_kallisto.tsv | sort | uniq -c
  cut -f 2 Down_Domeins_kallisto.tsv | sort | uniq -c
```

les sigo debiendo los comandos de GitHub, ya mañana queda 

## Viernes 04-07-2025

El día de hoy se comprendió de entender R en el entorno de google Colab. Aquí lo que se busca es graficar los datos obtenidos del ejercicio 5. 

```R
# Cargamos las librerias 
library (dplyr)
library (ggplot2)
library(stringr)
# Cargamos nuestro documento (Up_Kallisto)
kallisto_Up <- read.csv('Up_Domeins_Kallisto.tsv' , head = TRUE)
# Lo observamos
str(kallisto_Up)
kallisto_Up
# Extraemos la columna de los IDs y observamos
kallisto_Up$IDs <- as.factor(word(kallisto_Up$Query_Sequence.Database_EggNOG_Protein_Domains, 1 , sep = "\t" ))
kallisto_Up$IDs
# Extraemos la columna de los dominios y observamos
kallisto_Up$Domeins <- as.factor(word(kallisto_Up$Query_Sequence.Database_EggNOG_Protein_Domains, 2, sep = '\t'))
kallisto_Up$Domeins
```

Aun falta acabarlo y poner lo de GitHub

## Lunes 07-07-2025

El día de hoy se tomo la mitad del curso de metagenómica. Donde se está aprendiendo sobre como a partir de los datos obtenidos de la secuenciación se lee la calidad de las predicciones, se ensamblan (contigs y scaffolds ), se separan los MAGs y se lee la calidad de los MAGs. Todo esto se realizó en el entorno de R. 

### Flujo de trabajo 

El flujo de trabajo es: 

1. Sequence Reads
2. Quality control 
3. Assembly 
4. Binning
5. Taxonomy 

### *Evaluación de la calidad*

Para la evaluación de la calidad, se deberán de tener ya las secuencias (formato Fastq) y activar el entorno (el cual ya esta programado por defecto para este curso) 

```R
$ conda activate metagenomics 
# Observamos las opciones de fastqc 
$ fastqc -h
```

Evaluamos la calidad mediante FastQC "FastQC cuenta con varias funciones que le permiten obtener una idea rápida de cualquier problema que puedan tener sus datos, para que pueda considerarlos antes de continuar con sus análisis. En lugar de analizar las puntuaciones de calidad de cada lectura, FastQC analiza la calidad colectiva de todas las lecturas de una muestra."

```R
# Descomprimimos los archivos y los mandamos a una carpeta donde los podamos ubicar facilmente 
$ unzip [filename.fastq]
# Teniendo los archivos descomprimidos y ubicados en la carpeta donde se guardan 
$ fastqc *.fastq*
# FastQC nos creara archivos .zip y .htlm, donde podremos observar la grafíca en nuestro navegador 
```

*Recorte y filtrado*

Visualizamos gráficos de calidad por base que muestran la distribución de la calidad en cada base en todas las lecturas de nuestra muestra. Esta información nos ayuda a determinar el umbral de calidad que aceptaremos y, por lo tanto, obtuvimos información sobre qué muestras no superan los controles de calidad. Algunas de nuestras muestras no superan varias métricas de calidad utilizadas por FastQC. Sin embargo, esto no significa que debamos descartarlas. Es común que algunas métricas de calidad fallen, lo que puede o no ser un problema para su aplicación posterior. 

Para lograrlo, utilizaremos un programa llamado [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic) . Esta útil herramienta filtra las lecturas de baja calidad y elimina las bases de baja calidad de las muestras especificadas.

Trimmomatic necesita que les especifiquemos los datos de entrada (en pareja o en solitario, es decir, dos archivos a comparar o uno solo donde este sea comparado). Además de las siguiente condiciones 

| Paso          | Significado                                                  |
| ------------- | ------------------------------------------------------------ |
| ILLUMINACLIP  | Realizar la extracción del adaptador.                        |
| SLIDINGWINDOW | Realice el recorte de la ventana deslizante, cortándola una vez que la calidad promedio dentro de la ventana caiga por debajo de un umbral. |
| LEADING       | Cortar las bases al inicio de una lectura si la calidad está por debajo de un umbral. |
| TRAILING      | Cortar las bases del final de una lectura si la calidad está por debajo de un umbral. |
| CROP          | Cortar la lectura a una longitud específica.                 |
| HEADCROP      | Cortar el número especificado de bases desde el inicio de la lectura. |
| TOPHRED33     | Convertir puntuaciones de calidad a Phred-33.                |
| TOPHRED64     | Convertir puntuaciones de calidad a Phred-64.                |
| MINLEN        | Descartar una lectura completa si está por debajo de una longitud especificada. |

![img](https://carpentries-lab.github.io/metagenomics-analysis/fig/03-03-01.png)

```R
$ trimmomatic PE -threads4 SRR_1056_1.fastq SRR_1056_2.fastq \
              SRR_1056_1.trimmed.fastq SRR_1056_1un.trimmed.fastq \
              SRR_1056_2.trimmed.fastq SRR_1056_2un.trimmed.fastq \
              ILLUMINACLIP:SRR_adapters.fa SLIDINGWINDOW:4:20
# PE le indica a trimmomatic que va a tomar como pareja dos archivos como entrada
# SRR_1056_1.fastq SRR_1056_2.fastq son los dos archivos de entrada
# SRR_1056_1.trimmed.fastq SRR_1056_2.trimmed.fastq son los archivos donde se guarden las secuencias que cumplan con las condiciones 
# SRR_1056_1un.trimmed.fastq y SRR_1056_2un.trimmed.fastq son los archivos donde se guarden las secuencias que NO cumplan con las condiciones 
# ILLUMINACLIP:SRR_adapters.fa le indica a trimmomatic que deberá de cortar el adaptador utilizado
# SLIDINGWINDOW:4:20 le incica a trimmomatic que deberá de remover las bases si el PE tiene un valor abajo de 20 
```

### Ensamblado o Assembly

Una vez asegurados de tener una buena calidad en nuestras secuencias, se deberá a ensamblar, para ello de utiliza el algoritmo de MetaSPAdes, el cual nos ayuda a obtener Contig y Scaffolds

```R
# Ensamblaremos usando metaspades.py indicando el archivo forward como -1 y el archivo reverse como -2 
# Ubicamos los archivos que ya "trimmeamos" 
$ metaspades.py -1 JC1A_R1.trim.fastq.gz -2 JC1A_R2.trim.fastq.gz -o ../../results/assembly_JC1A
# Una vez teniendo esto, nos arrojara un directorio lleno de información uti, que nos servira despúes para agrupar  
assembly_graph_after_simplification.gfa  corrected/              K55/             scaffolds.fasta
assembly_graph.fastg                     dataset.info            misc/            scaffolds.paths
assembly_graph_with_scaffolds.gfa        first_pe_contigs.fasta  params.txt       spades.log
before_rr.fasta                          input_dataset.yaml      pipeline_state/  strain_graph.gfa
contigs.fasta                            K21/                    run_spades.sh    tmp/
contigs.paths                            K33/                    run_spades.yaml   
```

### Agrupamiento o Binning

Los genomas originales de la muestra pueden separarse mediante un proceso denominado binning. Este proceso permite el análisis por separado de cada especie del metagenoma, con suficientes lecturas para reconstruir un genoma. Los genomas reconstruidos a partir de ensambles metagenómicos se denominan MAG (Genomas Ensamblados por Metagenoma). En este proceso, los contigs ensamblados del metagenoma se asignan a diferentes bins (archivos FASTA que contienen ciertos contigs). Idealmente, cada bin corresponde a un solo genoma original (un MAG).

![El diagrama representa las secuencias de ADN de la muestra original como cromosomas circulares de tres taxones diferentes. Tras la secuenciación, las secuencias de ADN de los tres taxones se mezclan en pequeñas lecturas lineales; tras el ensamblaje, se obtienen contigs, cada uno correspondiente a un único taxón, excepto aquellos con un ensamblaje incorrecto que contienen secuencias de diferentes taxones en el mismo contig. Tras la clasificación de taxones, se separan los contigs.](https://carpentries-lab.github.io/metagenomics-analysis/fig/03-05-01.png)

Bineamos la muestra que acabamos de ensamblar. El comando para ejecutar MaxBin es `run_MaxBin.pl`, y los argumentos que necesita son el archivo FASTA del ensamblado, el FASTQ con las lecturas directas e inversas, el directorio de salida y el nombre.

```R
# Creamos un direcctorio especifico 
$ mkdir  MAXBIN
# corremos MaxBin en nuestros archivos ya ensamblados
$ run_MaxBin.pl -thread 8 -contig JP4D_contigs.fasta -reads ../data/trimmed_fastq/JP4D_R1.trim.fastq.gz -reads2 ../data/trimmed_fastq/JP4D_R2.trim.fastq.gz -out MAXBIN/JP4D
# Observamos las anotaciones que hizo MaxBin
$ cat MAXBIN/JP4D.summary
```

*Control de calidad*

La calidad de un MAG depende en gran medida del tamaño del genoma de la especie, su abundancia en la comunidad y la profundidad de su secuenciación. 

[CheckM](https://github.com/Ecogenomics/CheckM) es un excelente programa para evaluar la calidad de nuestros MAG. Mide la integridad y la contaminación mediante el recuento de genes marcadores en los MAG. El flujo de trabajo de linaje de CheckM coloca sus bins en un árbol de referencia para determinar a qué linaje corresponde y utilizar los genes marcadores adecuados para estimar los parámetros de calidad. Desafortunadamente, el flujo de trabajo de linaje consume mucha memoria, por lo que no puede ejecutarse en nuestros equipos. Sin embargo, podemos indicarle a CheckM que utilice solo genes marcadores de bacterias para reducir el consumo de memoria. Este método es menos preciso, pero también puede ser ventajoso si desea analizar todos sus bins con los mismos marcadores.

```R
# Creamos un directorio especifico para nuestro control de calidad 
$ mkdir CHECKM
# Corremos checkm en nuestros archivos ya agrupados, con la restricción de que lo haga con el linaje de bacteria
$ checkm taxonomy_wf domain Bacteria -x fasta MAXBIN/ CHECKM/ 
# Para obternerlo en una tabla "tsv" 
$ checkm qa CHECKM/Bacteria.ms CHECKM/ --file CHECKM/quality_JP4D.tsv --tab_table -o 2
```



### Comando Github

Para estos comandos es indispensable preguntarse, "¿Comó puedo compartir lo que estoy haciendo en una plataforma, para que todo aquel que quiera replicar mi trabajo lo haga de forma sencilla?", bueno la respuesta es que se puede ocupar Github, la cual su motivo principal es tener un repositorio donde se guarde tu trabajo, las anotaciones que hagas y el código que utilices. Esto lo puedes hacer desde su plataforma abriendo el navegador, sin embargo, se tiene una opción más fácil. 

Primero vamos a crear un repositorio 

![image-20250707130514814](C:\Users\Hp\AppData\Roaming\Typora\typora-user-images\image-20250707130514814.png)

En el inicio vamos a encontrar las opción de "new", donde crearemos un nuevo repositorio. Una vez creado, vamos a copiar el link de "clonación"

![image-20250707130644283](C:\Users\Hp\AppData\Roaming\Typora\typora-user-images\image-20250707130644283.png)

Le damos click en "code" y copiamos el link. Posteriormente abrimos nuestra terminal 

```bash
# Clonamos nuestro repositorio en nuestra computadora local 
git clone <nuestro link> # Bash nos debera de reportar como "enlazado" nuestro repositorio
# Abrimos nuestro repositorio 
cd Planets/
# Bajamos la información de nuestro repositorio online
git pull # Debera de decir 'Alredy up to date', lo cual significa que estamos actualizados
# Comprobamos el 'status' de nuestro repositorio
git status # Bash nos dirá el estado de nuestra carpeta, si no hay archivos pendientes por subir 
```

Aquí es importante saber como funciona todo esto

![unnamed](C:\Users\Hp\Downloads\unnamed.png)

Cuando creamos un archivo y lo queremos subir a Github, deberemos de seguir el flujo. Primero tenemos que subir el archivo a "Staging area"

```bash
git add <nombre del archivo>
# Podemos observar el posicionamiento de nuestro archivo con el comando de status
git status # Nos dira el paso siguente 
# bash On branch main
Your branch is up to date with 'origin/main'.
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   ejemplo
```

Una vez teniendo el archivo en el "Staging area" podemos agregar más archivos o subirlo al repositorio local 

```bash
git commit <nombre del archivo> -m "Agregamos un mensaje para que los demás puedan entender que subimos, modificamos, etc"
# Usamos -m para agregar el mensaje y podemos agregar todos los archivos de Staging area con -a
```

Por subimos el archivo a Github con push

```bash
git push 
# bash 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 328 bytes | 328.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/EsauVillanueva25/Planets.git
   911aee0..8d522c7  main -> main
```

Por ultimo volvemos a usar git status para observar que todos los archivos están ya en Github y no tengamos pendientes 

```bash
git status
# bash 
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
# Nos dice Bash que no tenemos pendientes 
```

Podemos Observar el archivo ya subido/modificado en Github. Es importante siempre empezar con  git pull para trabajar con la versión actualizada del repositorio. 



## Martes 08-07-2025

El día de hoy se avanzó con el ejercicio de R 

```R
# Añadimos el url de los datos raw 
url <- "https://raw.githubusercontent.com/EsauVillanueva25/Planets/refs/heads/main/Down_Domeins_kallisto.tsv"
Kallisto_Down <- read.table(url, head = TRUE)
# Observamos la tabla
str(Kallisto_Down)
# Convertimos nuestra tabla de varios IDs repetidos a una donde se tiene solo los IDs unicos junto con el numero de dominios que presenta
Kallisto_Down_new <- Kallisto_Down %>%
  group_by(Query_Sequence)%>%
  summarise (
  n= n()
  )
# Observamos la conversión
print(Kallisto_Down_new)
# Convertimos la tabla a vectores
Kallisto_Down_new$IDs <- as.factor(word(Kallisto_Down_new$Query_Sequence, 2, sep = "_c"))
# Observamos el Vector
(print(Kallisto_Down_new$IDs))

Kallisto_Down_new$Num <- Kallisto_Down_new$n
# Observamos la tabla
str(print(Kallisto_Down_new$Num))
# Calculamos el numero de dominios acumulados y la media de dominios por ID
plot_df <- Kallisto_Down_new %>%
  group_by (IDs)%>%
  summarise (
  sum_domeins = sum(Num),
  n = n()
  )
```

## Miercoles  09-07-2025

El día de hoy se terminó de graficar los datos del ejercicio de ayer 

```R
# Grafico de radar
plt <- ggplot(plot_df) +
  geom_hline(
  aes(yintercept = y),
    data.frame(y = c(0:45)),
    color = "red"
  ) +
    geom_col(
    aes(
      x = reorder (str_wrap(IDs, 10), sum_domeins),
      y = sum_domeins,
      fill = n
    ),
    position = "dodge2",
    show.legend = TRUE,
    alpha = .9
  ) +
    geom_point(
    aes(
      x = reorder (str_wrap(IDs, 10), sum_domeins),
      y = n
    ),
    size = 3,
    color = "green"
    ) +
  geom_segment (
      aes(
        x = reorder (str_wrap(IDs, 10), sum_domeins),
        y = 0,
        xend = reorder (str_wrap(IDs, 10), sum_domeins),
        yend = 45
      ),
      linetype = "dashed",
      color = "black"
      ) +
        coord_polar ()
      plt
```

Además se terminó de ver las definiciones de árboles filogenéticos. mañana se pondran. 

## Jueves 10-07-2025

El día de hoy se leyó sobre "INFERRING A TREE FROM LOWEST COMMON ANCESTORS WITH AN APPLICATION TO THE OPTIMIZATION OF RELATIONAL EXPRESSIONS*"

## Lunes 14-07-2025

El día de hoy se continuó leyendo el paper sobre  "INFERRING A TREE FROM LOWEST COMMON ANCESTORS WITH AN APPLICATION TO THE OPTIMIZATION OF RELATIONAL EXPRESSIONS"

Donde se aprendió sobre como se construye un algoritmo para encontrar un posible árbol filogenético con ciertas restricciones de ancestros y descendientes

```python
if S consists of a single node then 
	return the tree consisting of node alone
else 
	begin 
    	compute Zrc $1, $2, , Sr;
        if r = 1 then 
        return the null tree
    else 
    	form m:= 1 to r do
    		begin
            C. := {(i, j) < (k, l) in C]i,f,k,1 are in S.};
            Tn := BUILD(S,., C.);
            if T. the null tree then
            	return the null tree
            end;
/. if we reach here a tree exists ./
let T be the tree with a new node for its root and
	whose children are the roots of T,., 1 =< m -<_ r;
    return T
end
end BUILD	
```

## Martes 15-07-2025

El día de hoy de construyo un árbol conforme a las restricciones y el algoritmo del día de ayer. Donde las restricciones son: 

1. (1, 3) < (2, 5) 
2. (4, 5) < (1, 9)
3. (1, 4) < (3, 7)
4. (7, 8) < (2, 10)
5. (2, 6) < (4, 8)
6. (7, 8) < (7, 10)
7. (3, 4) < (2, 6)
8. (8,10) < (5, 9)

Dividimos las restricciones en progenitores e hijos 

| (i, j) | (k, l)  |
| :----: | :-----: |
| (1, 3) | (2, 5)  |
| (7, 8) | (2, 10) |
| (2, 6) | (4, 8)  |
| (7, 8) | (7, 10) |
| (3, 4) | (2, 6)  |
| (8,10) | (5, 9)  |
| (1, 4) | (3, 7)  |
| (4, 5) | (1, 9)  |

 Las restricciones son las anteriores y se basa conforme a las siguientes reglas 

1)  i and j must be in the same set. Otherwise (i, j) is the root of T, and the root
   cannot be a proper descendant of (k, l).
2) Either k and are in different sets, or i, j, k and l are all together in one set.
   Otherwise (i, j) cannot be a proper descendant of (k, l). 

Gracias a esto se tiene el siguiente árbol: 

1. Por la regla (1), se producen los siguientes conjuntos

   {1, 3, 4, 5}, {2, 6}, {7, 8, 10}, {9}

2. Por la regla (2),  k y l deben de estar en conjuntos diferentes o i, j, k y l deben de estar en el mismo conjunto. 
   $$
   [(3, 4) < (2, 6)], [(7, 8) < (7, 10)] ≠ [{k}, {l}]
   $$
   Entonces se tiene {1, 3, 4}, {2}, {5}, {6}, {7, 8}, {9}, {10}

3. Como ya no se tienen mas restricciones y estas cumplen con las reglas (1) y (2). Se concluye con el árbol 

   <img src="C:\Users\Hp\AppData\Roaming\Typora\typora-user-images\image-20250722162732330.png" alt="image-20250722162732330" style="zoom:50%;" />

## Miércoles 16-07-2025

## Jueves 17-07-2025

## Viernes 18-07-2025

## Lunes 21-07-2025

El día de hoy se enfoco en terminar (falta aun la ultima sección) del curso de metagenómica. Donde lo primero fue ver "Taxonomic assigment" donde se le asigna una predicción taxonómica a los datos previamente ya "agrupado" (en conting o reads ), estos datos se guardan en un archivo `.report` . Una vez teniendo ya estos archivos, se utiliza `Krona` la cual clasifica por jerarquía y nos arroga un grafo. 

```bash
# Cortamos la tabla del archivo para tener el ID y su información 
 $ cut -f2,3 JP4D.001.kraken > JP4D.001.krona.input
# Llamamos a Krona
$ ktImportTaxonomy JP4D.001.krona.input -o JP4D.001.krona.out.html
# Por ultimo vemos el grafíco en nuestro Browser
https://bioinformatica.matmor.unam.mx/rstudio/files/dc_workshop/taxonomy/mags_taxonomy/JP4D.001.krona.out.html
```

También podemos usar `Pavian` como herramienta visual. En este no es necesario usar lenguaje       de  programación   por que es una herramienta web y solo deberemos de cargar nuestro archivo. https://fbreitwieser.shinyapps.io/pavian/ 

 Por ultimo se aprendió sobre como explorar la taxonomía de nuestro datos utilizando R

Primero se creo una tabla con los linajes y su puntuación utilizando `kraken-biom` y guardándose en `cuatroc.biom`  

```bash
# Activamos el ambiente
$ conda activate metagenomics
# Creamos la tabla con los linajes 
$ kraken-biom JC1A.report JP4D.report JP41.report --fmt json -o cuatroc.biom
```

## Martes 22-07-2025

El día de hoy se siguió con el curso de metagenómica. 

Se empezó creando y manipulando 'Phyloseq Objects'.

Phyloseq es una biblioteca con herramientas para analizar y trazar la información de abundancia y asignación taxonómica de sus muestras metagenómicas. 

```R
# Carga de packages requeridos
> if (!requireNamespace("BiocManager", quietly = TRUE))
    	install.packages("BiocManager")
# Instalamos Phyloseq
> BiocManager::install("phyloseq")
> install.packages(c("RColorBrewer", "patchwork"))
# Cargamos las paqueterias 
> library("phyloseq")
> library("ggplot2")
> library("RColorBrewer")
> library("patchwork")
#===Creamos un Phyloseq Object===#
# Le indicamos a R donde vamos a trabajar
> setwd("~/dc_workshop/taxonomy/")
```

Creamos el objeto con el comando `import_biom`

```R
> merged_metagenomes <- import_biom("cuatroc.biom")
# Observamos nuestro objeto 
> class(merged_metagenomes)
```

Exploramos las etiquetas taxonómicas:

Intentemos acceder a los datos almacenados en nuestro objeto `merged_metagenomes`. Dado que un objeto phyloseq es un objeto especial en R, necesitamos usar el operador `@` para explorar las subsecciones de datos dentro de `merged_metagenomes`. Si escribimos `merged_metagenomes@`, se muestran cinco opciones; usamos `tax_table` y `otu_table`. Después de escribir `merged_metagenomes@otu_table `o `merged_metagenomes@tax_table`, se seleccionará la opción `.Data` en ambos casos. Vemos qué hay dentro de `tax_table`:

```R
> View(merged_metagenomes@tax_table@.Data)
```

Vimos que la tabla estaba llenan de información basura y se tenia de filtrar. Para ello se utilizó `substring()` 

```R
> merged_metagenomes@tax_table@.Data <- substring(merged_metagenomes@tax_table@.Data, 4)
> colnames(merged_metagenomes@tax_table@.Data)<- c("Kingdom", "Phylum", "Class", "Order", "Family", "Genus", "Species")
```

Usamos el comando `unique` para observar los filos presentes en nuestro vector de información sin observar los que están "repetidos" 

```R
> unique(merged_metagenomes@tax_table@.Data[,"Phylum"])
```

Además de saber la sumatoria de las especies que pertenecen al filo 'Firmicutes' con `sum` 

```R
> sum(merged_metagenomes@tax_table@.Data[,"Phylum"] == "Firmicutes")
# Por ultimo podemos saber cuales clases hay en este filo 
> unique(merged_metagenomes@tax_table@.Data[merged_metagenomes@tax_table@.Data[,"Phylum"] == "Firmicutes", "Class"])
```

## Miércoles 23-07-2025



 