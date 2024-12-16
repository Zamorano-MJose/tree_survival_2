# tree_survival_2

En este repositorio encontramos un análisis realizado con RMarkdown de los datos de supervivencia de árboles.  

Los archivos de los que disponemos son:

+ **LICENSE:** que es la información de la licencia que hemos seleccionado nosotros, la cual ha sido la licencia Apache. Hemos elegido esta ya que los datos originales no tenían licencias ni restricciones en su uso, por lo que hemos elegido esta.
+ **README_original.md:** Es el archivo de README que proporcionaban los autores al obtener los datos en la base de datos de [Dryad](https://datadryad.org/stash/dataset/doi:10.5061/dryad.7d7wm380b#usage), que es donde encontramos estos datos al hacer una búsqueda más avanzada.
+ **Tree_Data.csv:** son los datos proporcionados por los autores del artículo y con los que hemos trabajado nosotros posteriormente.
+ **Tree_seedling_shade_tolerance_arises_from_interact.pdf:** artículo que detalla el procedimiento utilizado y el que se analizo en el experimento original.
+ **facultad_de_ciencias.png:** imagen en formato PNG del logo de la Facultad de ciencias de la Universidad de Córdoba (UCO).
+ **logo_UCO.png:** imagen en formato PNG del logo de la UCO.
+ **predecir_supervivencia_definitivo.Rmd:** análisis realizado en formato RMarkdown.
+ **predecir_supervivencia_definitivo.html:** resultado en html del codigo que hemos realizado con RMarkdown.
+ **libraries.bib:** archivo para obtener las referencias, creado en la consola de RStudio.

<br>

En los datos utilizados (Tree_Data.csv) tenemos diferentes variables y son con las que realizaremos el análisis, estas variables son:

+ **No:** Identificador de las semillas.
+ **Species_** Especies utilizadas capaces de vivir en el mismo entorno, pero con diferente tolerancia a la luz. Las especies son:
  - Acsa = *Acer saccharum*
  - Acru = *Acer rubrum*
  - Acne = *Acer negundo*
+ **Ligth:** Niveles de luz utilizados en el experimento. Los niveles son:
  - Low = 2% luz directa
  - High = 30% luz directa
+ **Microbe:** Microorganismos utilizados, se obtuvo un filtrado de estos y se aplicaron tal que se obtuvieron 5 tratamientos, estos fueron:
  - Control: papel de filtro esterilizado
  - None: agua desionizada y papel de filtro.
  - Small: 20 µm filtrado en agua desionizada y papel de filtro.
  - Large: agua desionizada y 40-250 µm filtrado en papel de filtro.
  - Combined: Small + Large, es decir que el filtrado estaba tanto en agua desionizada como en papel de filtro.
+ **Adult:** Número de arboles adultos que se utilizaron para recoger el suelo donde plantaron las semillas.
+ **Bench:** Número de la maceta donde se cultivo cada semilla.
+ **Harvest:** En que semana fue cosechada la plántula para medir los datos. Pueden ser **3,6** o **9 semanas**.
+ **Time:** Día del experimento en el que la planta se cosechó, murió o terminó el experimento.
+ **Event:** Para analizar la supervivencia de las plantulas. Cada una se caracterizó como:
  - 0 = utilizada en el experimento.
  - 1 = muerta.
+ **AMF:** Porcentaje de colonización por los microorganimos. Calculado son los datos *AMFcount/AMFintersections*. Se basa es el número de colonias contadas en las raíces en 100 intersecciones.
+ **Phenolics:** Calculado como nmol de ácido gálico equivalentes por mg de peso seco.
+ **NSC:** Calculado como porcentaje de peso seco compuesto por carbohidratos no estructurales.
+ **Lignin:** Porcentaje de masa seca que corresponde a la lignina.
+ **AMF\_Imp:** Valores de *AMF* imputados.
+ **PHN\_Imp:** Valores de *Phenolics* imputados.
+ **NSC\_Imp:** Valores de *NSC* imputados.
+ **LIG\_Imp:** Valores de *Lignin* imputados.








La versión de R que hemos utilizado es la versión 4.4.2 de 64 bits para analizar los datos.
