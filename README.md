# Instrucciones
Introducción a Git y pasos para subir el programa a GitHub

# Instalando Git
Lo primero que se tiene que hacer es instalar Git en tu máquina virtual. Para ello tienen que visitar este [link](https://git-scm.com/download/win) para ello. 
**IMPORTANTE:** Van a usar todo por defecto en la instalación EXCEPTO cuando pida sobreescribir la rama principal como se ve en la imagen:
![Git override default branch name](https://miro.medium.com/max/1400/1*V6pyalT1ByXwdI0nxdLSGg.png)

# Iniciando el repositorio
Ahora con Git instalado, dirijanse a la carpeta de los proyectos de los robots. Cuando estén en dichas carpetas abrirán una terminal (CMD) en dicha carpeta y ejecutaran los siguientes comandos.

```bash
git init
git config --global user.name "MrKrrot" # Aquí va su nombre de usuario en GitHub
git config --global user.email "rafita.olguin@hotmail.com" # Aquí va su correo usado en GitHub
git add .
git commit -m "TMAT3 Robot15p" # En las comillas cambien dependiendo su equipo y tamaño del robot
git remote add origin git@github.com:utm-robotic/TMAT3-15p.git # Aquí también depende del equipo y el tamaño del robot
git push -u origin main
```
