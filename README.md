![BrightCoders Logo](img/logo-bc.png)

# Denuncia ciudadana

![cover](img/cover.jpg)
> Photo by <a href="https://unsplash.com/@koshuuu?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Koshu Kunii</a> on <a href="https://unsplash.com/s/photos/citizen-rights?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

## Requerimientos
Una organización civil requiere de una aplicación web mediante la cual se puedan registrar y consultar denuncias ciudadanas

La aplicación web deberá complir con las siguientes funciones:

### Registro de usuario
- Permite a cualquier ciudadano registrarse proporcionando la siguiente información:
  - `Usuario`. Campo alfanumérico que permite identificar de manera única a cada persona registrada.
  - `E-mail`. Correo electrónico que sirve de contacto con el usuario.
  - `Clave`. Campo alfanumérico para la clave de acceso del usuario.

**BONUS POINTS** el `e-mail` debe ser verificado por algún mecanismo, por ejemplo, enviando algún código de confirmación al correo

### Inicio de sesión
- Permite a los usuarios registrados y al administrador iniciar sesión. Para iniciar sesión deberán capturar su `e-mail` y `clave`

### Home
- [`Inicio`](https://github.com/bright-coders/proyecto-denuncia-ciudadana-web/blob/main/README.md#inicio). Muestra un listado de las denuncias presentadas en los `lugares de interés` que el usuario tiene registrados, ordenado cronológicamente de la más reciente a la más antigua. 
-  `Configuración`. Esta opción o pantalla permite al usuario:
  - cambiar su nombre de usuario.
  - cambiar su correo electrónico.
  - cambiar su clave de acceso.
  - agregar `lugares de interés`. Los lugares de interés se  componen por los campos `código postal` y `asentamiento`.
- [`Mis denuncias`](https://github.com/bright-coders/proyecto-denuncia-ciudadana-web/blob/main/README.md#mis-denuncias). Esta opción muestra un listado de las denuncias que se han presentado ordenadas cronológicamente de la más reciente a la más antigua. 
- [`Agregar denuncia`](https://github.com/bright-coders/proyecto-denuncia-ciudadana-web/blob/main/README.md#agregar-denuncia). Esta opción permite agregar una nueva denuncia.

## Inicio
El listado de la pantalla de inicio, muestra las denuncias presentadas en los lugares de interés aue el usuario tiene registrados, ordenado cronológicamente de la más reciente a la más antigua. La información que el usuario puede ver es:
  - Usuario que hizo la denuncia
  - Area 
  - Título
  - Descripción
  - Evidencia(s)
  - Botón que permite otros usuarios manifestar su apoyo a esa denuncia (like) 

## Agregar denuncia
Permite agregar una nueva denuncia. Para agregar una denuncia el usuario deberá registrarse la siguiente información:
  - `usuario` [requerido] El usuario que realiza la denuncia, **debe existir la opción de hacer denuncias de manera anónima**
  - `fecha de registro` fecha en que se registra o publica la denuncia
  - `fecha de hechos` fecha en la que ocurrieron los hechos o denuncia
  - `área` [requerido] El área de la denuncia, por ejemplo, seguridad, servicios, infraestructura, etc. Se toman de un catálogo definido en la base de datos
  - `titulo` [requerido] [Un título que identifica a la denuncia 
  - `descripción` [requerido] Descripción de los hechos o denuncia
  - `ubicación` [requerido] Dirección de los hechos o denuncia. Esta integrado por lo siguientes campos:
    - `Estado`[requerido]
    - `Municipio` [requerido]
    - `Código postal` [requerido]
    - `Asentamiento`[requerido]
    - `Calle` [no requerido]
    -  `Número` [no requerido]
    -  La información se toma de un catálogo almacenado en la base de datos el cual puede llenarse con información [obtenida de esta página](https://www.correosdemexico.gob.mx/SSLServicios/ConsultaCP/Descarga.aspx)
   -  `evidancia` Inageb que se agrega como evidencia. **BONUS POINTS** Permite agregar más de una imagen o documento PDF.

## Mis denuncias
Permite ver un listado de las denuncias que el usuario ha registrado presentado ordenadas cronológicamente de la más reciente a la más antigua y le permite modificar o eliminar denuncias.

## Requerimientos no-funcionales
- Calidad
  - Utilizar estilo de código definido por la comunidad (apoyarse en Rubocop)
  - Pruebas unitarias
  - Puntuación en Rubycritic: por lo menos 90 en la carpeta de la App y por lo menos 65 en la carpeta de pruebas
  - Utilizar SandiMeter para analizar el código y utilizar el resultado para hacer mejoras
  - Presentación correcta en las versiones más recientes de los principales navegadores: Edge, Chrome, Safari y Firefox
- Deployment
  - Configuración de un servidor web (heroku o similar) para el deployment automático de actualizaciones de la app
  - [Configuración de un servidor de integración continua como Travis CI o Circle CI](https://circleci.com/features/ruby/)
- Frontend
  - CSS: libertad para utilizar cuaquier framework o librería, preferentemente SASS
    - Por ejemplo puedes utilizar Bootsrap junto con [bootstrap_form](https://github.com/bootstrap-ruby/bootstrap_form) para tus formularios

## Tecnologías
- Ruby on Rails en el backend
- PostgreSQL como base de datos principal
- CSS: libertad para utilizar cuaquier framework o librería, preferentemente SASS
  - Por ejemplo puedes utilizar Bootsrap y junto con [bootstrap_form](https://github.com/bootstrap-ruby/bootstrap_form) para tus formularios
- Javascript: libertad para utilizar cualquier framework o librería, preferentemente sin jQuery
- Framework para pruebas [Rspec](https://rspec.info/) ó [Minitest](https://github.com/seattlerb/minitest)

## Entregable
- Código fuente en Github 
  - Debe incluir README con información sobre como configurar el proyecto
  - Los commits de Git deben ser significativos
- Demo de la App correndo en heroku o similar
- Libertad para utilizar cualquier diseño, imágenes, etc, que considere necesarios y apropiados

## Setup
En [este elnace](setup/README.md) se describen los pasos necesarios para ejecutar/probar este proyecto, así como los integrantes de este equipo

## Enlaces
[Encuentra aquí una lista completa de recursos de ayuda](https://github.com/bright-coders/commons/tree/master/topics/resources)

 
 

