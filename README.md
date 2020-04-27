# datos-cuarentenaBO

![](https://lab-tecnosocial.github.io/datos-cuarentenaBO/img/afiche.png)

## Propósito 

Con el crecimiento de los casos confirmados de coronavirus, desde el 22 de marzo rige en el país una cuarentena total dictada por el gobierno nacional, con limites finales inciertos. La medida tiene como objetivo frenar los contagios vía restricciones en el desplazamiento y las reuniones, pero al mismo tiempo existe cierta incertidumbre en cuanto al abastecimiento de productos alimenticios, la atención de servicios de salud y otros. Algunos ciudadanos no contamos con la suficiente información para viabilizar de forma más cercana y efectiva esas necesidades básicas. 

 * El objetivo de este repositorio consiste en recolectar datos georeferenciados de abastecimiento, servicios y salud en el contexto de la crisis del Covid-19 en Bolivia.
 * Y al mismo tiempo distribuir esos datos en formato abierto para que puedan ser utilizados por desarrolladores para crear apps informativas (vía una API estática de JSON que hemos preparado) o analistas y visualizadores de datos (mediante los datos en CSV).
 
## ¿Por qué datos abiertos?

Porque son la base para fomentar un ecosistema de actores que genere productos informativos como visualizaciones, apps, análisis de datos, investigaciones, toma de decisiones ciudadanas y políticas, planificación territorial, etc. En nuestro país aun no existen muchas iniciativas de datos abiertos por parte de los gobernantes. En nuestra búsqueda para hacer apps y analisis de datos no hemos encontrando disponibilidad de datos en repositorios gubernamentales, por lo que emprendimos esta iniciativa ciudadana. 

## Metodología

Hemos realizado tres formas de recolección de los datos. Primero, hemos transcrito manualmente los mensajes de ayuda e imagenes en Facebook, Twitter y WhatsApp que nos llegaban. Segundo, hemos buscado datos geográficos disponibles. Tercero, hemos hecho scraping de algunos sitios web con información pública relevante, cuando era posible. Posteriormente hemos limpiado un poco esa información y la hemos transformado en formatos abiertos para mayor fácilidad de uso de las diversas iniciativas ciudadanas. Las fuentes consultadas se enlistan al final.

Valga aclarar que este es un trabajo aún en curso, todo aporte o correcci[on es bienvenido.

## Versionado

La versión 1 (v1) de este repositorio tiene diferentes modelos de datos, pues los datos provienen de diversas fuentes. Si uno busca datos sobre mercados, por ejemplo, algunas fuentes estarán más completas que otras, tanto en atributos como en extensión. La versión 2 (v2) de la API cuenta con un sólo modelo general para todas la fuentes y es una base más limpia, aunque la cantidad de campos se reduce a 8. Pueden usar la versión que más les convenga, la v2 sin embargo es mucho más uniforme y clara.

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

Por ejemplo, para solicitar los datos de alimentos se agrega la terminación `/v1/web/alimentos.json` a la url de base. Notese que todos los *endpoints* empiezan con mayuscula y necesariamente deben contar con la extensión final `.json`. Para una explicación con más ejemplos puede verse la [documentación v1](https://lab-tecnosocial.github.io/datos-cuarentenaBO/docs/docs-v1.html). No todos los datos están georeferenciados o están completos; para los casos donde no se tienen los datos disponibles pusimos la marca de `NA`, mientras que para los datos no relevantes para un caso `null`. 

## API v2 (NUEVO!)

`7558` registros disponibles a nivel Bolivia. Esta es la versión más limpia y unificada de la API. Los campos para todas las fuentes disponibles son:

 * `Departamento`
 * `Tipo`
 * `Nombre`
 * `Direccion`
 * `Telefono`
 * `Latitud`
 * `Longitud`
 * `Fuente`
Y se usa `null` para los datos no disponibles, ya no `NA`.
 
Se ha simplificado las solicitudes a tres:
  * GET `/v2/all/all.json` para obtener todos los datos de todas las fuentes.
  * GET `/v2/all/{fuente}.json` devuelve todos los datos de una fuente especifica. Parametros: `gamlp`, `gamsc`, `geobo`, `osm`, `rmk`, `web`.
  * GET `/v2/serv/{servicio}.json` Devuelve servicios especificos de todas las fuentes. 34 parametros disponibles entre `Agua`, `Alimentos`, `CentroMedico`, `Mercado` y otros (ver documentación para más detalles).
  
Para más ejemplos: [Ver la documentación de la v2](https://lab-tecnosocial.github.io/datos-cuarentenaBO/docs/docs-v2.html).


## Proyectos que usan este repositorio

Los siguientes proyectos hacen uso de este repositorio:

* [Mapa de abastecimiento en La Paz](https://rafalopezv.io/static/sm/mapa_covid_lpz_abasto.html)

<img src="https://lab-tecnosocial.github.io/datos-cuarentenaBO/img/p1-lapazaba.jpg" width=400px>

Si estas utilizando los datos de este repositorio, avisanos para incluir un enlace a tu proyecto en este espacio y también te ayudaremos a promocionar tu proyecto en nuestros canales sociales. 

## Soporte y aporte

![](https://lab-tecnosocial.github.io/datos-cuarentenaBO/img/discord.png)

Si necesitas ayuda con estos datos para integrarlos a tu aplicación o análisis, o encuentras errores, bugs, o quieres aportar con más datos, ideas o código, nos encontramos en el siguiente [servidor de Discord](https://discord.gg/ahQntDk). Estaremos activos minimamente hasta que terminen las medidas de cuarentena. El repositorio se encuentra [aquí](https://github.com/lab-tecnosocial/datos-cuarentenaBO).

## Fuentes

* https://www.openstreetmap.org/. Requiere de la atribución de "© Colaboradores de OpenStreetMap". Más info [aquí](https://www.openstreetmap.org/copyright).
* http://sitservicios.lapaz.bo/mapas/abasto/
* https://www.lapaz.bo/
* https://guiaurbana.gmsantacruz.gob.bo/guiaurbana/
* https://geo.gob.bo/
* http://conectandobolivia.fepc.bo/
* Grupos de facebook
* Grupos de WhatsApp
