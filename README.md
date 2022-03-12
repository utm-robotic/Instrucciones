# Instrucciones
Introducción a Git y pasos para subir el programa a GitHub

# Instalando Git
Lo primero que se tiene que hacer es instalar Git en tu máquina virtual. Para ello tienen que visitar este [link](https://git-scm.com/download/win) para ello. 
**IMPORTANTE:** Van a usar todo por defecto en la instalación EXCEPTO cuando pida sobreescribir la rama principal como se ve en la imagen. **TAMBIÉN SELECCIONAR Use External OpenSSH**


![Git override default branch name](https://miro.medium.com/max/1400/1*V6pyalT1ByXwdI0nxdLSGg.png)

![Git use OpenSSH](https://user-images.githubusercontent.com/191109/148549844-fe4404e2-46f5-4efc-8a84-95982991e9d9.png)

# Usar SSH para autenticarte con GitHub
Ahora abre una terminal y ejecuta el siguiente comando
```bash
ssh-keygen -t ed25519 -C "your_email@example.com" # Aquí debes poner tu correo entre las comillas
```
Ahora te preguntará dónde deseas guardar la clave SSH, elige el lugar predeterminado presionando Enter y ahora te pedirá una contraseña llamada passphrase, aquí queda a tu gusto si quieres omitir dando enter o insertando una (no aparecerá en la consola).

Antes de continuar, abre una terminal de Windows PowerShell en modo Administrador para ejecutar este comando que activará los usos de SSH
```bash
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
```

Ahora ejecuta estos dos comandos:
```bash
ssh-agent -s
ssh-add ~/.ssh/id_ed25519
```

Ya hiciste todo para generar la clave SSH, ahora conectala a GitHub, para ello tienes que copiarla, para eso usa este comando
```bash
clip < ~/.ssh/id_ed25519.pub
```

Ahora dirigite a GitHub y sigue los pasos de las imagenes
![Settings](https://docs.github.com/assets/cb-34573/images/help/settings/userbar-account-settings.png)

![Configuración ssh keys](https://docs.github.com/assets/cb-17145/images/help/settings/settings-sidebar-ssh-keys.png)

![Pegar la clave SSH](https://docs.github.com/assets/cb-24796/images/help/settings/ssh-key-paste.png)

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
