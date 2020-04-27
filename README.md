# datos-cuarentenaBO

![](https://lab-tecnosocial.github.io/datos-cuarentenaBO/img/afiche.png)

## Propósito 

Con el crecimiento de los casos confirmados de coronavirus, desde el 22 de marzo rige en el país una cuarentena total dictada por el gobierno nacional, con limites finales inciertos. La medida tiene como objetivo frenar los contagios vía restricciones en el desplazamiento y las reuniones, pero al mismo tiempo existe cierta incertidumbre en cuanto al abastecimiento de productos alimenticios, la atención de servicios de salud y otros. Algunos ciudadanos no contamos con la suficiente información para viabilizar de forma más cercana y efectiva esas necesidades básicas. 

 * El objetivo de este repositorio consiste en recolectar y verificar datos georeferenciados de abastecimiento, servicios y salud en el contexto de la crisis del Covid-19 en Bolivia.
 * Al mismo tiempo es importante que esos  datos estén en formato abierto y pueden ser utilizados por desarrolladores para crear apps informativas (vía una API estática de JSON que hemos preparado) o analistas y visualizadores de datos (mediante los datos en CSV).
 
## ¿Por qué datos abiertos?

Porque son la base para fomentar un ecosistema de actores que genere productos informativos como visualizaciones, apps, análisis de datos, investigaciones, toma de decisiones ciudadanas y políticas, planificación territorial, etc. En nuestro país aun no existen muchas iniciativas de datos abiertos por parte de los gobernantes y en nuestra búsqueda para hacer apps y analisis de datos por nosotros mismos no hemos encontrando mucha disponibilidad de datos en repositorios gubernamentales, por lo que emprendimos esta iniciativa ciudadana. 

## Metodología

Hemos realizado tres formas de recolección de los datos. Primero, hemos transcrito manualmente los mensajes de ayuda e imagenes en Facebook, Twitter y WhatsApp que nos llegaban. Segundo, hemos buscado datos geográficos disponibles. Tercero, hemos hecho scraping de algunos sitios web con información pública relevante, cuando era posible. Posteriormente hemos limpiado un poco esa información y la hemos transformado en formatos abiertos para mayor fácilidad de uso de las diversas iniciativas ciudadanas.

Valga aclarar que este es un trabajo aún en curso, todo aporte es bienvenido.

## Versionado

La versión 1 (v1) de este repositorio tiene diferentes modelos de datos, pues los datos provienen de diversas fuentes. Si uno busca datos sobre mercados, por ejemplo, algunas fuentes estarán más completas que otras, tanto en atributos como en extensión. La versión 2 (v2) de la API cuenta con un sólo modelo general para todas la fuentes y es una base más limpia, aunque la cantidad de campos se reduce a 8. Pueden usar la versión que más les convenga, la v2 es mucho más uniforme y clara, no obstante. 

## API v1

### Cantidad de registros

|Departamento|Número de registros    |
|------------|-----------------------|
|La Paz      | Abastecimiento: 150 |
|            | Entidades financieras: 779 |
|            | Farmacias: 470 |
|            |Servicios de salud: 202 |
|Santa Cruz  | Abastecimiento: 331|
|            |   Servicios de salud: 77|
|Cochabamba  | Mercados: 112 |
|            | Servicios de salud: 152 |
|Bolivia     | Mercados en Bolivia (GeoBolivia 2017): 629 |
|            | Farmacias, bancos, servicios de salud (OpenStreetMap): 3680 |
|            |Alimentos (diversas fuentes web): 381|
|            | Servicios(diversas fuentes web): 367|
|            |Salud (diversas fuentes web) :129 |

### Uso 

La URL de base es `https://lab-tecnosocial.github.io/datos-cuarentenaBO`. Dado que es una API estática solo soporta solicitudes `GET` sin parametros.

La /v1/ tiene la siguiente estructura con sus respectivos *endpoints*:

```
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

Por ejemplo, para solicitar los datos de alimentos se agrega la terminación `/v1/web/alimentos.json` a la url de base. Notese que todos los *endpoints* empiezan con mayuscula. Para una explicación con más ejemplos puede verse la [documentación](https://lab-tecnosocial.github.io/datos-cuarentenaBO/docs/docs-v1.html). No todos los datos están georeferenciados o están completos; para los casos donde no se tienen los datos disponibles pusimos la marca de `NA`, mientras que para los datos no relevantes para un caso `null`. 

## API v2 (NUEVO!)

Esta es la versión más limpia y unificada de la API. Los campos para todas las fuentes disponibles son:

 * `Departamento`
 * `Tipo`
 * `Nombre`
 * `Direccion`
 * `Telefono`
 * `Latitud`
 * `Longitud`
 * `Fuente`
 
[Ver la documentación de la v2](https://lab-tecnosocial.github.io/datos-cuarentenaBO/docs/docs-v2.html) para más ejemplos. 


## Uso en proyectos

Si estas utilizando los datos de este repositorio, avisanos para incluir un enlace a tu proyecto en este espacio y también te ayudaremos a promocionar tu proyecto en nuestros canales sociales. 

## Soporte y aporte

![](https://lab-tecnosocial.github.io/datos-cuarentenaBO/img/discord.png)

Si necesitas ayuda con estos datos para integrarlos a tu aplicación o análisis, o encuentras errores, bugs, o quieres aportar con más datos, ideas o código, nos encontramos en el siguiente [servidor de Discord](https://discord.gg/ahQntDk). Estaremos activos minimamente hasta que terminen las medidas de cuarentena. El repositorio se encuentra [aquí](https://github.com/lab-tecnosocial/datos-cuarentenaBO).

## Fuentes

* https://www.openstreetmap.org/. Requiere de la atribución de "© Colaboradores de OpenStreetMap". Más info [aquí](https://www.openstreetmap.org/copyright).
* https://www.cochabamba.bo/application/municipio/mapa
* http://sitservicios.lapaz.bo/mapas/abasto/
* https://www.lapaz.bo/
* https://guiaurbana.gmsantacruz.gob.bo/guiaurbana/
* https://geo.gob.bo/
* http://conectandobolivia.fepc.bo/
* Grupos de facebook
* Grupos de WhatsApp
