> Spanish as usual
## 2.5 Conexión remota

### 2.5.1 Servicio de red de conexión remota

Los servicios de red de conexión remota permiten a los usuarios conectarse a un sistema informático desde una ubicación diferente a la de dicho sistema. Esto se realiza mediante una red, como Internet. Ejemplos comunes incluyen el Protocolo de Escritorio Remoto (RDP) y Secure Shell (SSH).

### 2.5.2 Características de servicios de red de conexión remota

Las características principales de los servicios de red de conexión remota incluyen:

- **Seguridad**: Implementación de mecanismos de cifrado para proteger los datos transmitidos.
- **Autenticación**: Uso de credenciales (usuario y contraseña) para verificar la identidad del usuario.
- **Accesibilidad**: Permite a los usuarios acceder a recursos y aplicaciones de forma remota.
- **Flexibilidad**: Compatibilidad con diferentes sistemas operativos y dispositivos.
- **Escalabilidad**: Capacidad de manejar múltiples conexiones simultáneas.

### 2.5.3 Tipos y características de conexiones remotas

Existen varios tipos de conexiones remotas, entre las que se incluyen:

- **Conexión SSH (Secure Shell)**:
  - Utiliza cifrado para garantizar la seguridad de los datos.
  - Proporciona acceso a la línea de comandos de un servidor remoto.
  - Soporta túneles SSH para proteger otras formas de tráfico de red.

- **Conexión RDP (Remote Desktop Protocol)**:
  - Permite el acceso a la interfaz gráfica de un sistema remoto.
  - Utilizado principalmente en sistemas Windows.
  - Soporta redirección de dispositivos y recursos locales.

- **VPN (Virtual Private Network)**:
  - Crea una conexión segura a través de una red pública.
  - Permite el acceso a recursos de red privados como si el usuario estuviera físicamente presente en la red local.
  - Utiliza protocolos de cifrado para proteger los datos.

### 2.5.4 Instalación o actualización para tener disponible el servicio de SSH

Para instalar o actualizar el servicio de SSH en un sistema operativo basado en Linux, se pueden seguir los siguientes pasos:

1. **Instalación de OpenSSH**:
   - En Debian/Ubuntu: `sudo apt-get install openssh-server`
   - En CentOS/Fedora: `sudo yum install openssh-server`

2. **Iniciar el servicio SSH**:
   - `sudo systemctl start sshd`

3. **Habilitar el servicio SSH para que se inicie automáticamente**:
   - `sudo systemctl enable sshd`

4. **Actualizar el servicio SSH**:
   - `sudo apt-get update && sudo apt-get upgrade openssh-server` (Debian/Ubuntu)
   - `sudo yum update openssh-server` (CentOS/Fedora)

### 2.5.5 Funcionamiento de los comandos y parámetros de conexión remota

Algunos de los comandos y parámetros comunes en SSH incluyen:

- **Conectar a un servidor remoto**:
  - `ssh usuario@servidor` (conexión estándar)
  - `ssh -p puerto usuario@servidor` (especificando un puerto diferente)

- **Copiar archivos entre el sistema local y remoto**:
  - `scp archivo_local usuario@servidor:/ruta/destino` (copiar desde local a remoto)
  - `scp usuario@servidor:/ruta/archivo_remoto /ruta/local` (copiar desde remoto a local)

- **Ejecutar comandos remotos**:
  - `ssh usuario@servidor "comando_a_ejecutar"`

### 2.5.6 Funcionamiento de los comandos de transferencia de archivos y directorios

SSH incluye herramientas para la transferencia de archivos y directorios de manera segura:

- **SCP (Secure Copy)**:
  - Copiar archivos desde local a remoto: `scp archivo usuario@servidor:/ruta/destino`
  - Copiar archivos desde remoto a local: `scp usuario@servidor:/ruta/archivo /ruta/local`

- **SFTP (SSH File Transfer Protocol)**:
  - Iniciar una sesión SFTP: `sftp usuario@servidor`
  - Comandos dentro de SFTP:
    - `put archivo_local` (subir archivo)
    - `get archivo_remoto` (descargar archivo)
    - `ls` (listar archivos en el servidor remoto)
    - `cd` (cambiar directorio en el servidor remoto)

### 2.5.7 Proceso de la ejecución de comandos en conexión remota

La ejecución de comandos en una conexión remota generalmente sigue estos pasos:

1. **Establecer la conexión**:
   - Utilizando SSH: `ssh usuario@servidor`
   
2. **Autenticación**:
   - Ingresar la contraseña o utilizar una clave SSH para autenticarse.

3. **Ejecutar comandos**:
   - Una vez autenticado, se puede ejecutar cualquier comando disponible en el sistema remoto.

4. **Finalizar la sesión**:
   - Salir de la sesión SSH utilizando el comando `exit` o cerrando la terminal.

- [ ] translate it to english ⏳ 2024-07-13 