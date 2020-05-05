# Neo4j_PHP
Para establecer una conexión entre el motor neo4j se debe tener con aticipación instado composer(Composer es un manejador de paquetes para PHP que proporciona un estándar para administrar, descargar e instalar dependencias y librerías).

# Instalacion de librerias
Primero creamos el directorio el cual va a ser nuestro proyecto para establecer la conexión entre neo4j y php. Cuando se haya creado el directorio abrimos simbolo del sistema y nos hubicamos en nuestra carpeta con un cd, ya hubicados en nuestro directorio en simbolo del sistema digitamos el siguuiente comando.

```composer require neoxygen/neoclient```

# Conexión
Para la conexión creamos un archivo php y digitamos lo siguiente:

```
<?php

require_once 'vendor/autoload.php';

use Neoxygen\NeoClient\ClientBuilder;

$client = ClientBuilder::create()
    ->addConnection('default','http','localhost',7474)
    ->build();
```
