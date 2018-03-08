# magento2
Proyecto para customizar completamente un magento2

## Lo que debes saber antes de instalar:
--------------------

### Requerimientos minimos:
+ http://devdocs.magento.com/guides/v2.2/install-gde/system-requirements-tech.html

### Bajar magento 2 CE:
+ `composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition NOMBRE-PROYECTO`

### Ver el memory_limit del php que esta tomando la consola cli, hay que setearle 2000M en el php.ini que este usando la cli:
+ `php -r "echo ini_get('memory_limit').PHP_EOL;"`

### Instalar magento por consola *(despues de haberlo bajado)*:
+ `php bin/magento setup:install --admin-firstname=TUNOMBRE --admin-lastname=TUAPELLIDO --admin-email=TUMAILPARALOGUEARTEALADMIN --admin-user=ADMINUSER --admin-password=PASSWORD --base-url=http://localhost/NOMBREPROYECTO/ --db-host=localhost --db-name=BASEDEDATOS --db-user=root --db-password=TUPASSDEPHPMYADMIN --language=es_AR --currency=ARS --timezone=America/Argentina/Buenos_Aires --use-rewrites=1`

### Cambiar a modo developer para poder instalar el Sample data y desarrollar:
+ `php bin/magento deploy:mode:set developer`

### Bajar sample data:
+ `php bin/magento sampledata:deploy`

### Aplicar el sample data:
+ `php bin/magento setup:upgrade`

### Borrar cache:
+ `php bin/magento c:f`

### Ver como es la url del admin:
+ está en  `app/etc/env.php` y buscar al principio:
```php
  <?php
      return array (
        'backend' =>
        array (
          'frontName' => 'admin',
        ),

  ?>
```


 LISTO! TENES UN MAGENTO 2 + SAMPLEDATA ANDANDO.
--------------------
