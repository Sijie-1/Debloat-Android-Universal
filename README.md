# Universal Android Debloat Script

## ⚠️ Advertencia Importante

**Este script no funciona en Xiaomi, Redmi o POCO.** Estos dispositivos usan MIUI o HyperOS y entrarán en bootloop. No uses esta herramienta en ellos. **Asumes todo riesgo si modificas tu dispositivo.**

---

## Qué hace

Elimina aplicaciones preinstaladas (bloatware) de tu teléfono Android sin necesidad de acceso root. Usa ADB (Android Debug Bridge) para desinstalar paquetes desde tu computadora.

## Requisitos

**En tu computadora:**
- Python 3.6+
- Android SDK Platform-Tools (proporciona `adb`)

**En tu teléfono:**
- Opciones de desarrollador activadas
- Depuración USB activada
- Conectado por cable USB al computador
- Autorización RSA confirmada en pantalla

---

## Instalación

### Linux (Debian/Ubuntu)
```bash
sudo apt install python3 android-tools
```

### Linux (Arch)
```bash
sudo pacman -S python android-tools
```

### Linux (Fedora)
```bash
sudo dnf install python3 android-tools
```

### Windows
1. Descarga Python desde [python.org](https://www.python.org) y marca "Add Python to PATH"
2. Descarga [Platform-Tools](https://developer.android.com/studio/releases/platform-tools) y extrae en `C:\android-tools` (o similar)
3. Añade la carpeta a variables de entorno (PATH del sistema)

---

## Uso

### Método 1: Script Python (recomendado)

Verifica conexión:
```bash
adb devices
```

Confirma en pantalla del teléfono si aparece un diálogo de autorización. Luego ejecuta:

```bash
python3 apps.py
```

### Método 2: Línea de comandos (solo Linux)

1. Abre un emulador de terminal en tu entorno de trabajo.
2. Copia el contenido íntegro del archivo apps.txt.
3. Pega el contenido en la terminal.
4. Presiona Enter para ejecutar.

---

## Notas

- Usa `python3` en Linux. Si `python` no funciona, es normal; instala `python3` explícitamente.
- El script desinstala solo desde la cuenta de usuario; las aplicaciones del sistema permanecen.
- En Windows, evita ejecutar `apps.txt` directamente (congela cmd).
- Prueba con pocos paquetes primero si no reconoces ninguno.

---

## Responsabilidad

Eres responsable de cualquier daño. Haz backup de tus datos antes de proceder.
