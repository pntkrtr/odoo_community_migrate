# odoo_community_migrate
Migración incremental abierta entre versiones de odoo community

Hacer copia de seguridad de la base de datos de Odoo.

Leer muy bien la documentación del enlace siguiente: https://oca.github.io/OpenUpgrade/index.html

El repositorio con el código de Open Upgrade es: https://github.com/OCA/OpenUpgrade

Abrir CMD como administrador y...

pyton -m pip install --upgrade pip

pip install pywin32==255

pip install git+https://github.com/OCA/openupgradelib.git@master#egg=openupgradelib

git clone -b <Versión_destino> https://github.com/OCA/OpenUpgrade.git

python odoo-bin --db_user=<tu_usuario_db> --db_password=<tu_contraseña_db> --database=<nombre_db> \
--upgrade-path=<Directorio_Clonado>/OpenUpgrade/openupgrade_scripts/scripts --update all --stop-after-init \
--load=base,web,openupgrade_framework

Ajustar la configuración para Odoo y OpenUpgrade, editando los archivos de configuración y parámetros de línea de comandos para apuntar a la base de datos que debe ser actualizada. 
Los parámetros recomendados de línea de comandos son las banderas `--upgrade-path=<path_to_openupgrade>/openupgrade_scripts/scripts --update all --stop-after-init --load=base,web,openupgrade_framework`.
