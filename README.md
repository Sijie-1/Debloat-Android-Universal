# Universal Android Debloat Script

## Descripción General
Este repositorio proporciona una herramienta automatizada desarrollada en Python para eliminar paquetes preinstalados (bloatware) en dispositivos Android. El script opera a través del Android Debug Bridge (ADB) y ejecuta comandos de desinstalación en el entorno del usuario principal. Esta metodología permite limpiar el sistema operativo sin necesidad de obtener privilegios de superusuario (root). La matriz de eliminación incluye cientos de aplicaciones identificadas de diversos fabricantes y operadoras.

## Advertencia de Compatibilidad Crítica
La arquitectura de este script presenta restricciones funcionales importantes. Los sistemas operativos MIUI e HyperOS bloquean a nivel de núcleo la desinstalación de aplicaciones del sistema a través de ADB sin permisos elevados. Por lo tanto, esta herramienta no es funcional en dispositivos de las marcas Xiaomi, Redmi o POCO. Además, la eliminación indiscriminada de paquetes estructurales puede provocar inestabilidad del sistema o bucles de reinicio en otras marcas. El operador asume total responsabilidad por las modificaciones realizadas en su dispositivo.

## Requisitos Previos
1. Instalar un intérprete de Python 3 en la máquina anfitriona.
2. Instalar los binarios de Android SDK Platform-Tools para habilitar la interfaz ADB.
3. Habilitar el menú oculto de "Opciones de desarrollador" en el terminal Android.
4. Activar el interruptor de "Depuración USB" dentro del menú de desarrolladores.
5. Conectar el dispositivo al ordenador mediante un cable de datos y autorizar la huella de clave RSA en la pantalla del móvil.

## Guía de Ejecución: GNU/Linux
1. Abre un emulador de terminal en tu entorno de trabajo.
2. Instala las dependencias necesarias a través de tu gestor de paquetes utilizando comandos como `sudo pacman -S python android-tools`.
3. Inicia el demonio y verifica la conexión del dispositivo ejecutando `adb devices`.
4. Navega hacia el directorio de descarga del repositorio mediante el comando `cd`.
5. Inicia el proceso de limpieza ejecutando `python apps.py`.

## 1.1 Guía de Ejecución: GNU/Linux
1. Abre un emulador de terminal en tu entorno de trabajo.
3. Copia todo el texto de apps.txt
4. Pega el contenido copiado en tu terminal
5. Enter
6. Be happy

## Guía de Ejecución: Windows
1. Descarga el instalador de Python desde el portal oficial y marca la casilla "Add Python to PATH" antes de iniciar la instalación.
2. Extrae el archivo ZIP de las Platform-Tools de Android en una ruta accesible del disco duro.
3. Incorpora la ruta del directorio extraído a las variables de entorno (PATH) del sistema operativo.
4. Abre una instancia de PowerShell o del Símbolo del sistema.
5. Valida la comunicación con el teléfono introduciendo `adb devices` y confirmando el acceso en la pantalla.
6. Posiciónate en la carpeta del script y ejecuta `python apps.py`.
