# datos-cuarentenaBO

## Antecedentes

A partir del crecimiento de los casos confirmados de coronavirus, desde el 22 de marzo rige en el país una cuarentena total dictada por el gobierno nacional, con limites finales inciertos. La medida tiene como objetivo frenar los contagios por coronavirus vía restricciones en las reuniones y el desplazamiento, pero al mismo tiempo ha generado incertidumbre en cuanto al abastecimiento de productos alimenticios, la atención de servicios de salud y otros. Muchos ciudadanos no contamos con la suficiente información para viabilizar esas necesidades básicas. 

## Objetivos

 * El objetivo de este proyecto es recolectar y verificar datos de abastecimiento, servicios y salud en el contexto de la crisis del Covid-19 que sirvan como insumos de información para los ciudadanos.
 * Los datos están en formato abierto y pueden ser utilizados por desarrolladores para crear apps informativas (vía una API estática de JSON) o analistas (mediante los datos en CSV).
 
## ¿Por qué datos abiertos?

Porque es la base para construir otros productos para los ciudadanos, como visualizaciones, apps, análisis de datos, etc. En nuestro país aun no existen muchas iniciativas de datos abiertos por parte de los gobernantes, por lo que nace esta iniciativa ciudadana.

## Metodología

Hemos tomado tres estrategias de recolección. Primero hemos recolectado los mensajes de ayuda e imagenes en Facebook, Twitter y WhatsApp y los hemos transcrito manualmente. Segundo, hemos buscado la información georeferenciada disponible. Tercero, hemos hecho scraping de algunos sitios web con información pública relevante. Posteriormente hemos limpiado un poco esa información y la hemos transformado en formatos abiertos para mayor fácilidad de uso.

Valga aclarar que este es un trabajo aún en progreso.

## Versionado

La v1 (actual) tiene varios modelos de datos pues provienen de diversas fuentes (ver sus módelos y métodos en la documentación). En la v2 los integraremos en un sólo modelo de datos. 

## Documentación de la API 

La URL de base es `https://lab-tecnosocial.github.io/datos-cuarentenaBO/`. Dado que es una API estática solo soporta GET requests.

La /v1/ tiene la siguiente estructura y sus respectivos endpoints:

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
│   ├── salud.csv
│   └── salud.json
└── web
    ├── Alimentos.csv
    ├── Alimentos.json
    ├── Salud.csv
    ├── Salud.json
    ├── Servicios.csv
```

Por ejemplo, para solicitar los datos de alimentos se agrega la terminación `/v1/web/alimentos.json` a la url de base. Notar que todos los endpoints empiezan con mayuscula. Para una explicación más detallada y ejemplos ver la documentación. 

## Soporte y aporte



## Fuentes



Si tienes
