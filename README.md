# TraceCode IA

Entorno de programación con seguimiento de integridad académica, integrado con la plataforma de la Facultad de Ingeniería Mochis. Es un editor de código completo (basado en Visual Studio Code) que registra cómo se construyó tu solución mientras programas, y entrega tu tarea directo a Moodle al terminar.

## Descargar e instalar

1. Ve a la sección **[Releases](../../releases/latest)** de este repositorio y descarga `TraceCodeIA-Instalador.exe` (pesa alrededor de 310 MB).
2. Corre el instalador. No pide permisos de administrador — se instala solo para tu usuario.
3. Sigue los pasos (Siguiente → Instalar). Al terminar se abre solo.

## Antes de usarlo: instala el lenguaje de tu materia

TraceCode IA no incluye compiladores ni intérpretes — necesitas tener instalado, aparte, el del lenguaje que uses en tu materia:

| Lenguaje | Qué instalar |
|---|---|
| C++ | Un compilador como [MinGW-w64](https://www.mingw-w64.org/) (da el comando `g++`) |
| Python | [Python](https://www.python.org/downloads/) (marca "Add to PATH" durante la instalación) |
| Java | [JDK](https://adoptium.net/) |
| C# | [.NET SDK](https://dotnet.microsoft.com/download) |
| JavaScript / TypeScript | [Node.js](https://nodejs.org/) |

Sin esto, TraceCode IA sigue funcionando, pero no puede registrar cuántas veces corriste tu programa mientras lo hacías.

## Cómo usarlo

1. Abre TraceCode IA (ícono en el Escritorio o en el menú de inicio).
2. En el panel de la izquierda, inicia sesión con tu usuario y contraseña de la universidad — los mismos con los que entras a Moodle.
3. Elige tu materia y la actividad en la que vas a trabajar.
4. Dale clic a **Iniciar sesión de código**, resuelve tu tarea normalmente, y cuando termines dale clic a **Finalizar sesión** — tu entrega se sube sola a Moodle.

Tu sesión se queda iniciada aunque cierres el programa — no necesitas volver a escribir tu usuario y contraseña cada vez.

## ¿Ya lo tenías instalado y hay una versión nueva?

Descarga el instalador más reciente desde **[Releases](../../releases)** y córrelo igual que la primera vez — se actualiza solo encima de tu instalación anterior, sin perder nada.

## Problemas

Si algo no funciona, avísale a tu profesor.
