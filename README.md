# datos-cuarentenaBO

## Antecedentes

A partir del crecimiento de los casos confirmados de coronavirus, desde el 22 de marzo rige en el país una cuarentena total dictada por el gobierno nacional, con limites finales inciertos. La medida tiene como objetivo frenar los contagios por coronavirus vía restricciones en las reuniones y el desplazamiento, pero al mismo tiempo ha generado incertidumbre en cuanto al abastecimiento de productos alimenticios, la atención de servicios de salud y otros. Muchos ciudadanos no contamos con la suficiente información para viabilizar esas necesidades básicas. 

## Objetivos

 * El objetivo de este proyecto es recolectar y verificar datos de abastecimiento, servicios y salud en el contexto de la crisis del Covid-19 que sirvan como insumos de información para los ciudadanos.
 * Los datos están en formato abierto y pueden ser utilizados por desarrolladores para crear apps informativas (vía una API estática de JSON) o analistas (mediante los datos en CSV).

## Metodología

Hemos tomado tres estrategias de recolección. Primero hemos recolectado los mensajes de ayuda e imagenes en Facebook, Twitter y WhatsApp y los hemos transcrito manualmente. Segundo, hemos buscado la información georeferenciada disponible. Tercero, hemos hecho scraping de algunos sitios web con información pública relevante. Posteriormente hemos limpiado un poco esa información y la hemos transformado en formatos abiertos para mayor fácilidad de uso.

Valga aclarar que este es un trabajo aún en progreso.

## Versionado

La v1 (actual) tiene varios modelos de datos pues provienen de diversas fuentes (ver sus módelos y métodos en la documentación). En la v2 los integraremos en un sólo modelo de datos. 

## Documentación de la API 

La URL de base es `https://lab-tecnosocial.github.io/datos-cuarentenaBO/v1/`

Dado que es una API estática solo soporta GET requests.


## Soporte y aporte

Si tienes
