# odoo_community_migrate
Migración incremental abierta entre versiones de odoo community

Hacer copia de seguridad de la base de datos de Odoo.

Leer muy bien la documentación del enlace siguiente: https://oca.github.io/OpenUpgrade/index.html

Abrir CMD como administrador y...

pyton -m pip install --upgrade pip

pip install pywin32==255

pip install git+https://github.com/OCA/openupgradelib.git@master#egg=openupgradelib


Ajustar la configuración para Odoo y OpenUpgrade, editando los archivos de configuración y parámetros de línea de comandos para apuntar a la base de datos que debe ser actualizada. 
The recommended command line parameters are the --upgrade-path=<path_to_openupgrade>/openupgrade_scripts/scripts --update all --stop-after-init --load=base,web,openupgrade_framework flags.
