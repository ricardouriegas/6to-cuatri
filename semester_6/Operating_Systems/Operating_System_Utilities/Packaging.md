### 2.4 Comandos para Empaquetar y Comprimir Archivos y Directorios
- [x] Grabar el tema 2.4.1 📅 2024-06-20 ✅ 2024-06-20

#### 2.4.1 Describir el concepto y evidenciar el funcionamiento de empaquetado de archivos y directorios

El empaquetado agrupa varios archivos y/o directorios en un solo archivo. Esto facilita la transferencia y manejo de los datos.

#### `tar`

- **Crear un archivo**: `tar -c -f archivo.tar directorio/` o `tar --create --file=archivo.tar directorio/`
- **Extraer un archivo**: `tar -x -f archivo.tar` o `tar --extract --file=archivo.tar`
- **Listar contenidos**: `tar -t -f archivo.tar` o `tar --list --file=archivo.tar`
- **Modo detallado**: `tar -v` o `tar --verbose`

#### 2.4.2 Describir el concepto y evidenciar el funcionamiento de compresión de archivos y directorios

##### `gzip`

- **Comprimir**: `gzip archivo`
- **Descomprimir**: `gunzip archivo.gz`

##### `zip -r`

- **Comprimir**: `zip -r archivo.zip directorio/`
- **Descomprimir**: `unzip archivo.zip`

##### `tar -z`

- **Crear y comprimir**: `tar -cz -f archivo.tar.gz directorio/`
- **Extraer y descomprimir**: `tar -xz -f archivo.tar.gz`

#### 2.4.3 Describir las características de tipos de empaquetado y compresión de archivos y directorios

- **Empaquetado**: Agrupar archivos sin reducir su tamaño.
- **Compresión**: Reducir el tamaño de los archivos empaquetados.

#### 2.4.4 Explicar el funcionamiento de los comandos y parámetros de:

##### Empaquetado y desempaquetado

- `tar -c -f`: Crear un archivo empaquetado.
- `tar -x -f`: Extraer un archivo empaquetado.

##### Compresión y extracción

- `gzip`/`gunzip`: Comprimir y descomprimir archivos individuales.
- `zip -r`/`unzip`: Comprimir y descomprimir directorios.
- `tar -z`: Empaquetar y comprimir al mismo tiempo.

# English
- [ ] Write the English translation 🛫 2024-06-19 