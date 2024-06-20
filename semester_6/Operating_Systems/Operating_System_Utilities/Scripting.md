# Spanish

## Scripts de la Interfaz de Línea de Comandos y Comandos para Empaquetar y Comprimir Archivos y Directorios

### 2.3 Scripts de la Interfaz de Línea de Comandos

#### 2.3.1 Definir el concepto de script
Un script es un archivo de texto que contiene una secuencia de comandos o instrucciones que pueden ser ejecutadas por un intérprete de línea de comandos. Los scripts se utilizan para automatizar tareas repetitivas y simplificar la ejecución de comandos complejos.

#### 2.3.2 Diferencia entre Shell y Bash
- **Shell**: Es un intérprete de comandos que permite a los usuarios interactuar con el sistema operativo. Existen varios tipos de shells, como Bourne Shell (sh), C Shell (csh), Korn Shell (ksh), entre otros.
- **Bash**: Es una versión mejorada del Bourne Shell, conocida como Bourne Again Shell. Bash es uno de los shells más populares y se usa comúnmente en sistemas operativos Unix y Linux.

#### 2.3.3 Describir las características de scripts
- **Automatización**: Permiten automatizar tareas repetitivas.
- **Portabilidad**: Los scripts pueden ejecutarse en diferentes sistemas con pocas o ninguna modificación.
- **Eficiencia**: Reducen el tiempo y esfuerzo necesario para ejecutar comandos manualmente.
- **Facilidad de Uso**: Son fáciles de escribir y mantener.

#### 2.3.4 Describir el proceso de construcción y ejecución de scripts
1. **Creación del Script**: Escribir comandos en un archivo de texto con extensión .sh.
2. **Asignar Permisos**: Hacer el script ejecutable usando `chmod +x script.sh`.
3. **Ejecución**: Ejecutar el script con `./script.sh`.

#### 2.3.5 Ejecutar script creado en Linux desde un lenguaje de programación
Para ejecutar un script desde Python, puedes usar el módulo `subprocess`:
```python
import subprocess

subprocess.run(['./script.sh'])
```

Para ejecutar un script desde Java, puedes usar la clase `ProcessBuilder`:
```java 
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try {
            ProcessBuilder pb = new ProcessBuilder("./script.sh");
            Process p = pb.start();
        } catch (IOException e) {
            e.printStackTrace();
	    }
	}
}
```

Para ejecutar un script desde C++, puedes usar la función `system`:
```cpp
#include <cstdlib>

int main() {
    system("./script.sh");
    return 0;
}
```

> Nota: Asegúrate de que el script tenga permisos de ejecución.
#### 2.3.6 Utilizar el comando cron para ejecutar un script en una hora especificada de forma diaria, semanal y mensual

- **Diariamente a las 7:00 AM**: `0 7 * * * /ruta/a/tu/script.sh`
- **Semanalmente los lunes a las 7:00 AM**: `0 7 * * 1 /ruta/a/tu/script.sh`
- **Mensualmente el primero de cada mes a las 7:00 AM**: `0 7 1 * * /ruta/a/tu/script.sh`

#### 2.3.7 Configurar la ejecución de un script para que se ejecute al iniciar el sistema operativo

Agregar el script al archivo `/etc/rc.local` (se necesita permisos de superusuario):

```bash
#!/bin/sh
# /etc/rc.local
/path/to/your/script.sh
exit 0
```

#### 2.3.8 Explicación de dos scripts por cada miembro del equipo

Cada miembro debe:

1. Explicar un script sin funciones.
```bash
#!/bin/sh
# Print today
echo "Today is: $(date)"

# get current directory
current_dir=$(pwd)

# Ask the user for a directory path 
read -p "Enter a directory path: " target_dir 
# Check if the target directory is the same as the current directory 

if [ "$current_dir" = "$target_dir" ]; then 
	echo "Yes, '$target_dir' is the same as '$current_dir'." 
else 
	echo "No, '$target_dir' is different from '$current_dir'." 
fi

```
1. Explicar un script con funciones, mostrando el uso de variables locales y globales. Referencia: [Funciones en Bash](https://linuxize.com/post/bash-functions/)
```bash
#!/bin/bash

# Function to get the current directory
get_current_dir() {
  current_dir=$(pwd)
  echo "$current_dir"
}

# Function to compare directories
compare_dirs() {
  local dir1="$1"
  local dir2="$2"
  if [ "$dir1" = "$dir2" ]; then
    echo "Yes, '$dir1' is the same as '$dir2'."
  else
    echo "No, '$dir1' is different from '$dir2'."
  fi
}

# Print today
echo "Today is: $(date)"

# Get the current directory
current_dir=$(get_current_dir)

# Ask the user for a directory path
read -p "Enter a directory path: " target_dir

# Compare directories
compare_dirs "$current_dir" "$target_dir"
```

# English
- [ ] Write the English translation 🛫 2024-06-19 