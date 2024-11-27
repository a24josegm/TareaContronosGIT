# Documentación del Proyecto

#He creado el repositorio y he hecho los cambios desde Terminal de Powershell.

#Primero instalo la herramienta de terminal de GIT
winget install --id GitHub.cli
![Captura instalando herramienta CLI](./images/1.png)

#Iniciamos sesion desde cli
gh auth login 
![Captura hacienda autenticación](./images/2.png)

#Selecionamos https y desde el navegador con la cuenta iniciada abrimos github y nos autorizamos.
![Captura hacienda autenticación 2](./images/3.png)

#ahora estamos authenticados vamos a crea un repo.
#Dentro de la carpeta en la que queremos crear el repositorio:
git init
![Captura de init repositorio](./images/4.png)

#Agregar un README.md y la Carpeta de Imágenes 
New-Item -Path . -Name "README.md" -ItemType "file"
New-Item -Path . -Name "images" -ItemType "directory" 
![Captura añadir carpeta de imagenes y readme.md](./images/5.png)

#Realizamos un commit
git add . 
git commit -m "Inicializa el proyecto con README.md y carpeta de imágenes” 
![Captura de commit](./images/6.png)

#Crear el repo en GitHub
gh repo create TareaContronosGIT --public --source . 
![Captura de creación de repositorio en GitHub](./images/7.png)

#Hacer la subida y definer el upstream.
git push --set-upstream origin master
![Captura de subida a GitHub](./images/8.png)
