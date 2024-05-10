[[Terminal]]

Python Package Index - PyPI: Sistema de gestion de paquetes de python

```bash
# Administración de paquetes python
pip install <nombre_del_paquete> # Instalar un paquete
pip uninstall <nombre_del_paquete> # Desinstalar un paquete
pip show <nombre_del_paquete> # Mostrar información sobre un paquete instalado
pip list # Listar todos los paquetes instalados
pip install --upgrade <nombre_paquete> # Actualizar un paquete a la última versión
pip search <término_de_búsqueda> # Buscar paquetes
pip show -f <nombre_del_paquete> # Mostrar la ubicación de un paquete instalado
pip list --outdated # Listar los paquetes obsoletos
pip freeze | ForEach-Object {pip uninstall -y $_.split('==')[0]} # Desinstalar todas las librerias listadas en pip

# Creación e intalación de dependencias con archivo requirements
pip freeze > requirements.txt # Crear un archivo de requisitos (requirements.txt)
pip install -r requirements.txt # Instalar paquetes desde un archivo de requisitos
```