# magento2
Proyecto para customizar completamente un magento2

LO QUE DEBES SABER ANTES DE INSTALAR:
http://devdocs.magento.com/guides/v2.2/install-gde/system-requirements-tech.html

BAJAR MAGENTO 2 CE:
composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition NOMBRE-PROYECTO

INSTALAR MAGENTO POR CONSOLA (despues de haberlo bajado):
    php bin/magento setup:install --admin-firstname=TUNOMBRE --admin-lastname=TUAPELLIDO --admin-email=TUMAILPARALOGUEARTEALADMIN --admin-user=ADMINUSER --admin-password=PASSWORD --base-url=http://localhost/NOMBREPROYECTO/ --db-host=localhost --db-name=BASEDEDATOS --db-user=root --db-password=TUPASSDEPHPMYADMIN --language=es_AR --currency=ARS --timezone=America/Argentina/Buenos_Aires --use-rewrites=1
    
CAMBIAR A MODO DEVELOPER PARA PODER INSTALAR EL SAMPLE DATA Y DESARROLLAR:
    php bin/magento deploy:mode:set developer

BAJAR SAMPLE DATA:
    php bin/magento sampledata:deploy

APLICAR EL SAMPLE DATA:
    php bin/magento setup:upgrade
    
BORRAR CACHE:
    php bin/magento c:f

VER COMO ES LA URL DEL ADMIN:
    está en  app/etc/env.php y buscar al principio:
        <?php
            return array (
              'backend' =>
              array (
                'frontName' => 'admin',
              ),

        ?>
 
 LISTO! TENES UN MAGENTO 2 + SAMPLEDATA ANDANDO.
