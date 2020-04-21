# datos-cuarentenaBO

## Antecedentes

A partir del crecimiento de los casos confirmados de coronavirus, desde el 22 de marzo rige en el país una cuarentena total dictada por el gobierno nacional, con limites finales inciertos. La medida tiene como objetivo frenar los contagios por coronavirus vía restricciones en el desplazamiento y las reuniones, pero al mismo tiempo existe cierta incertidumbre en cuanto al abastecimiento de productos alimenticios, la atención de servicios de salud y otros. Muchos ciudadanos no contamos con la suficiente información para viabilizar esas necesidades básicas. 

## Objetivos

 * El objetivo de este proyecto consiste en recolectar y verificar datos georeferenciados de abastecimiento, servicios y salud en el contexto de la crisis del Covid-19 que sirvan como insumos de información.
 * Los datos están en formato abierto y pueden ser utilizados por desarrolladores para crear apps informativas (vía una API estática de JSON) o analistas (mediante los datos en CSV).
 
## ¿Por qué datos abiertos?

Porque es la base para construir otros productos informativos, como visualizaciones, apps, análisis de datos, etc. En nuestro país aun no existen muchas iniciativas de datos abiertos por parte de los gobernantes y es dificil encontrar un repositorio nacional sobre esta temática, por lo que nace esta iniciativa ciudadana.

## Metodología

Hemos realizado tres formas de recolección de los datos. Primero hemos recolectado los mensajes de ayuda e imagenes en Facebook, Twitter y WhatsApp y los hemos transcrito manualmente. Segundo, hemos buscado la información geográfica disponible. Tercero, hemos hecho scraping de algunos sitios web con información pública relevante. Posteriormente hemos limpiado un poco esa información y la hemos transformado en formatos abiertos para mayor fácilidad de uso.

Valga aclarar que este es un trabajo aún en progreso.

## Versionado

La v1 (actual) tiene diferentes modelos de datos pues provienen de diversas fuentes (verla documentación). En el mismo apartado, por ejemplo mercados, algunos fuentes estarán más completas que otras. En la v2 estamos pensando integrarlo en un sólo modelo de datos. 

## Documentación de la API 

La URL de base es `https://lab-tecnosocial.github.io/datos-cuarentenaBO/`. Dado que es una API estática solo soporta GET requests.

La /v1/ tiene la siguiente estructura con sus respectivos endpoints:

```
.
├── gamcb
├── gamlp
│   ├── Abasto.csv
│   ├── Abasto.json
│   ├── CentrosDesarrolloSocial.csv
│   ├── CentrosDesarrolloSocial.json
│   ├── EntidadesFinancieras.csv
│   ├── EntidadesFinancieras.json
│   ├── EstacionesServicio.csv
│   ├── EstacionesServicio.json
│   ├── Farmacias.csv
│   ├── Farmacias.json
│   ├── Mercados.csv
│   ├── Mercados.json
│   ├── ModulosPoliciales.csv
│   ├── ModulosPoliciales.json
│   ├── PuntosVerdes.csv
│   ├── PuntosVerdes.json
│   ├── Salud.csv
│   ├── Salud.json
│   ├── Supermercados.csv
│   └── Supermercados.json
├── gamsc
│   ├── abastecimiento-emergencia
│   │   ├── Mercados.csv
│   │   ├── Mercados.json
│   │   ├── MercadosMovil.csv
│   │   ├── MercadosMovil.json
│   │   ├── Supermercados.csv
│   │   └── Supermercados.json
│   ├── centro-abastecimiento
│   │   └── Mercados.json
│   ├── edificios-administrativos
│   │   ├── Edificio_adm_salud.json
│   │   └── Sub_alcaldias_distritales.json
│   ├── infraestructura-social
│   │   ├── CentroAdultoMayor.csv
│   │   ├── CentroAdultoMayor.json
│   │   ├── GuarderiaMunicipal.csv
│   │   └── GuarderiaMunicipal.json
│   ├── salud
│   │   ├── Centro_salud_12hrs.csv
│   │   ├── Centro_salud_12hrs.json
│   │   ├── Centro_salud_24hrs.csv
│   │   ├── Centro_salud_24hrs.json
│   │   ├── Hospital_2do_nivel.csv
│   │   └── Hospital_2do_nivel.json
│   ├── secretaria-municipal
│   │   └── Secretarias_municipales.json
│   └── seguridad-ciudadana
│       ├── CentroSeguridad.csv
│       ├── CentroSeguridad.json
│       ├── EstacionesPoliciales.csv
│       └── EstacionesPoliciales.json
├── geobo
│   ├── Mercados2017.csv
│   └── Mercados2017.json
├── osm
│   ├── Bank.csv
│   ├── Bank.json
│   ├── Clinic.csv
│   ├── Clinic.json
│   ├── Doctors.csv
│   ├── Doctors.json
│   ├── Hospital.csv
│   ├── Hospital.json
│   ├── Pharmacy.csv
│   └── Pharmacy.json
├── rmk
│   ├── Mercados.csv
│   ├── Mercados.json
│   ├── Salud.csv
│   └── Salud.json
└── web
    ├── Alimentos.csv
    ├── Alimentos.json
    ├── Salud.csv
    ├── Salud.json
    ├── Servicios.csv
    └── Servicios.json
```

Por ejemplo, para solicitar los datos de alimentos se agrega la terminación `/v1/web/alimentos.json` a la url de base. Notese que todos los endpoints empiezan con mayuscula. Para una explicación más detallada y ejemplos ver la documentación. 

## Soporte y aporte

Si necesitas ayuda con los datos, encuentras errores, o quieres aportar con datos, ideas o código, estamos en el siguiente [servidor de Discord](https://discord.gg/ahQntDk), activos minimamente hasta que terminan las medidas de cuarentena y restricción de movimientos y reuniones.


## Fuentes

https://www.openstreetmap.org/
https://www.cochabamba.bo/application/municipio/mapa
http://sitservicios.lapaz.bo/mapas/abasto/
https://www.lapaz.bo/
https://guiaurbana.gmsantacruz.gob.bo/guiaurbana/
https://geo.gob.bo/
http://conectandobolivia.fepc.bo/
Grupos de facebook
Grupos de WhatsApp


**Con el apoyo de Hivos Bolivia**

