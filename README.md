# analisisdesentimientos
En este repositorio se agrupan distintos diccionarios que pueden ser utilizados para el análisis de sentimientos.  En particular me interesa nuclear 
los distintos diccionarios que se van desarrollado para su posterior uso y la fuente.


## Tidytext libraries (English)

La libreria tidytext tiene algunos diccionarios en inglés que vienen por defecto. Desde R pueden obtenerse utilizando la función get_sentiments("lexicon"). donde lexicon es la abreviacion del dicionario que quiere utilizarse.  

**AFFIN from Finn Årup Nielsen** 

get_sentiments("affin")
[AFFIN diccionario](http://www2.imm.dtu.dk/pubdb/pubs/6010-full.html)

AFINN es una lista de palabras en inglés clasificadas con un número entero entre menos cinco (negativo) y más cinco (positivo). Las palabras tienen
ha sido etiquetado manualmente por Finn Årup Nielsen en 2009-2011. El archivo está separado por tabuladores. Hay dos versiones:

AFINN-111: Nueva versión con 2477 palabras y frases.

AFINN-96: 1468 palabras y frases únicas en 1480 líneas. Tenga en cuenta que hay 1480 líneas, ya que algunas palabras se enumeran dos veces. La lista de palabras en no
se encuentra enteramente en orden alfabético.


La versión en español de este diccioario se encuentra en el siguiente[link](https://raw.githubusercontent.com/jboscomendoza/rpubs/master/sentimientos_afinn/lexico_afinn.en.es.csv)
Para descargarlo directamente desde R  y luego leerlo


download.file("https://raw.githubusercontent.com/jboscomendoza/rpubs/master/sentimientos_afinn/lexico_afinn.en.es.csv",
              "lexico_afinn.en.es.csv")
 afinn_spanish <- read.csv("lexico_afinn.en.es.csv", stringsAsFactors = F, fileEncoding = "latin1") %>% 
tbl_df()

