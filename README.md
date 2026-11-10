# TraceCode IA

Entorno de programación con seguimiento de integridad académica, integrado con la plataforma de la Facultad de Ingeniería Mochis. Es un editor de código completo (basado en Visual Studio Code) que registra cómo se construyó tu solución mientras programas, y entrega tu tarea directo a Moodle al terminar.

Funciona en **Windows** y en **Linux** de 64 bits: Ubuntu, Linux Mint, Debian, Fedora, openSUSE, Arch, Manjaro y demás.

## Windows

### Descargar e instalar

1. Descarga **[TraceCodeIA-Instalador.exe](https://github.com/Trace-AI-FIM/TraceAI/releases/download/v1.1.0/TraceCodeIA-Instalador.exe)** (pesa alrededor de 300 MB).
2. Corre el instalador. No pide permisos de administrador: se instala solo para tu usuario.
3. Sigue los pasos (Siguiente → Instalar). Al terminar se abre solo.
4. Si es tu primera instalación, aplica también la actualización más reciente (ver abajo).

### ¿Ya lo tenías instalado y hay una versión nueva?

1. Cierra TraceCode IA por completo (todas sus ventanas).
2. Descarga **[TraceCodeIA-Actualizacion.exe](https://github.com/Trace-AI-FIM/TraceAI/releases/download/v.1.2.0/TraceCodeIA-Actualizacion.exe)** y córrelo (Siguiente → Instalar). No pide permisos de administrador y no pierdes nada.
3. Abre TraceCode IA, ciérralo y ábrelo otra vez. Si te pide iniciar sesión de nuevo, es normal.

## Linux

Sirve en cualquier Linux de 64 bits con escritorio (prácticamente todas las distribuciones de 2019 en adelante). No funciona en equipos ARM, como Raspberry Pi o Chromebooks ARM, ni de 32 bits.


### Instalar (recomendado, sin contraseña de administrador)

1. Descarga **[TraceCodeIA-linux-x64.tar.gz](https://github.com/Trace-AI-FIM/TraceAI/releases/download/v1.3.1/TraceCodeIA-linux-x64.tar.gz)**.
2. Abre una terminal en la carpeta donde lo descargaste y ejecuta:

   ```bash
   tar -xzf TraceCodeIA-linux-x64.tar.gz
   cd TraceCodeIA
   ./install.sh --env /ruta/al/.env
   ```

3. Abre **TraceCode IA** desde el menú de aplicaciones, o con el comando `tracecode-ia`.

Se instala en `~/.local/share/TraceCodeIA`, solo para tu usuario.


### Desinstalar

- **Desinstalar:** `~/.local/share/TraceCodeIA/desinstalar.sh`. Tus sesiones y entregas pendientes se conservan.
- **Si algo falla:** ejecuta `sh ~/.local/share/TraceCodeIA/diagnostico.sh` y mándale la salida a tu profesor. No incluye tu contraseña ni la configuración del servidor.

Para verificar las descargas: `sha256sum -c SHA256SUMS.txt` en la carpeta donde están los archivos.

## Antes de usarlo: instala el lenguaje de tu materia

TraceCode IA no incluye compiladores ni intérpretes: necesitas tener instalado, aparte, el del lenguaje que uses en tu materia.

**Windows**

| Lenguaje | Qué instalar |
|---|---|
| C++ | Un compilador como [MinGW-w64](https://www.mingw-w64.org/) (da el comando `g++`) |
| Python | [Python](https://www.python.org/downloads/) (marca "Add to PATH" durante la instalación) |
| Java | [JDK](https://adoptium.net/) |
| C# | [.NET SDK](https://dotnet.microsoft.com/download) |
| JavaScript / TypeScript | [Node.js](https://nodejs.org/) |

**Linux** (C++, Python, Java y JavaScript en un solo comando; al instalar, TraceCode IA te muestra el de tu distribución)

| Distribución | Comando |
|---|---|
| Ubuntu, Linux Mint, Debian, Pop!_OS, Zorin | `sudo apt install g++ gdb python3 default-jdk nodejs` |
| Fedora | `sudo dnf install gcc-c++ gdb python3 java-devel nodejs` |
| openSUSE | `sudo zypper install gcc-c++ gdb python3 java-devel nodejs-default` |
| Arch, Manjaro, EndeavourOS | `sudo pacman -S gcc gdb python jdk-openjdk nodejs` |

Para C# en Linux instala el [.NET SDK](https://learn.microsoft.com/dotnet/core/install/linux) siguiendo las instrucciones de tu distribución.

Sin esto, TraceCode IA sigue funcionando, pero no puede registrar cuántas veces corriste tu programa mientras lo hacías.

## Cómo usarlo

1. Abre TraceCode IA (ícono en el Escritorio, en el menú de inicio o en el menú de aplicaciones de Linux).
2. En el panel de la izquierda, inicia sesión con tu usuario y contraseña de la universidad: los mismos con los que entras a Moodle.
3. Elige tu materia y la actividad en la que vas a trabajar.
4. Dale clic a **Iniciar sesión monitoreada**, resuelve tu tarea normalmente y, cuando termines, dale clic a **Finalizar sesión**: tu entrega se sube sola a Moodle.

Para la entrega cuentan los archivos que **creas durante la sesión**; editar uno que ya existía no cuenta. Tu sesión se queda iniciada aunque cierres el programa: no necesitas volver a escribir tu usuario y contraseña cada vez.

## Problemas

Si algo no funciona, avísale a tu profesor.
