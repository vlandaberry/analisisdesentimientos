# analisisdesentimientos
En este repositorio se agrupan distintos diccionarios que pueden ser utilizados para el análisis de sentimientos. En particular me interesa nuclear 
los distintos diccionarios que se van desarrollado para su posterior uso y la fuente. El desarrollo de diccionarios en idioma español no es tan frecuente como los de idioma inglés. Una alternativa que ha surgido recientemente es la de traducir los diccionarios existentes de inglés a español utilizando APIs como google translator. Si bien la traducción directa tiene algunas limitaciones, es una alternativa sencilla para obtener diccionarios en idioma español. 


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
Para descargarlo directamente desde R  y luego leerlo alcaza con correr las siguientes lineas de código:

download.file("https://raw.githubusercontent.com/jboscomendoza/rpubs/master/sentimientos_afinn/lexico_afinn.en.es.csv",
              "lexico_afinn.en.es.csv")
 afinn_spanish <- read.csv("lexico_afinn.en.es.csv", stringsAsFactors = F, fileEncoding = "latin1") %>% 
tbl_df()


**BING dictionary**
Bing fue desarrollado por  Bing Liu y colaboradores. Viene en inglés y se puede obtener directamente en R desde la librería tidytext  a travès de get_sentiments("bing"). 
Contiene un total de  6786 palabras clasificadas en positivas o negativas. 

Para obtener la traducción al español se utilizó la API de google translate y se obtuvo de esta forma el diccionario. El diccionario con la traducción al español se encuentra en el archivo bing_spa.csv.


**NRC dictionary**
Desarrollado por Saif Mohammad y Peter Turney. El diccionario en su version ingles viene en la librerıa tidytext. Es una lista de palabras y su asociacion con 8 emociones basicas (enojo, miedo,anticipaci ́on, confianza, sopresa, tristeza, alegr ́ıa y disgusto) y dos sentimientos:negativo y positivo.Al igual que para el diccionario bing utilizando la API de google translator y elpaquete translateR traduje el diccionario. Pueden encontrar el diccionario traducido en nrc_spa.csv


**Loughran and McDonald (2011)**

Diccionario que contiene 4150 palabras que se utilizan para anàlisis de textos financieros. Las palabras se pueden categorizar en 6 tipos "negativo" "positivo" "incertidumbre" "litigioso" "restrictivo" "superfluo". La traducción del diccionaro en español la pueden encontrar en lough_spa.csv



