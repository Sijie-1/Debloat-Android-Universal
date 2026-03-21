# Universal Android Debloat

Este repositorio aloja secuencias de comandos ADB diseñadas para eliminar aplicaciones preinstaladas (bloatware) en dispositivos móviles Android. La ejecución selectiva de estos comandos optimiza el rendimiento del sistema, reduce el consumo de memoria RAM y libera espacio de almacenamiento local.

## Advertencia Crítica de Compatibilidad

Los métodos de desinstalación detallados en este repositorio **no funcionan en dispositivos con MIUI o HyperOS**. El entorno de Xiaomi bloquea activamente la desinstalación profunda de paquetes de sistema mediante el comando `pm uninstall --user 0`. Los usuarios de estos sistemas operativos requieren métodos alternativos o privilegios de superusuario (root) para alterar las aplicaciones preinstaladas.

## Instrucciones de Uso

1. Instale las herramientas de la plataforma Android (ADB) en su computadora.
2. Habilite las **Opciones de desarrollador** y la **Depuración USB** en su dispositivo móvil.
3. Conecte el dispositivo mediante un cable USB y autorice la conexión en la pantalla del teléfono.
4. Abra una terminal en su computadora y ejecute el script correspondiente a su fabricante.

> **Nota:** Revise el contenido de cada script antes de su ejecución. La eliminación de dependencias críticas del sistema causa inestabilidad operativa o fallos de arranque (bootloops).
