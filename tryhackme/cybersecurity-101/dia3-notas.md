✅ Estado: ✔️ Completado
📅 Fecha: 07-07-2025
🖥️ Plataforma: TryHackMe
#IMPORTANTE-NOTA: Este documento fue redactado con ayuda de inteligencia artificial a partir de mis notas personales. El contenido refleja mi aprendizaje real; la IA fue utilizada únicamente para mejorar la organización, redacción y presentación con el objetivo de mayor legibilidad a futuro.

✍️ ERR574.

🧠 Resumen general de lo aprendido
En esta etapa del módulo Cyber Security 101 dentro de TryHackMe, aprendí a utilizar tanto el Símbolo del sistema (cmd.exe) como PowerShell en Windows. Estos son fundamentales para tareas de administración, automatización y análisis dentro de ciberseguridad.

🖱️ Comandos aprendidos en Símbolo del sistema (cmd.exe):
ipconfig – Muestra información sobre la configuración de red.

systeminfo – Proporciona detalles del sistema operativo.

netstat – Muestra conexiones de red activas.

ping – Verifica conectividad con una IP o dominio.

tracert – Muestra la ruta hasta un host.

nslookup – Consulta servidores DNS.

cd – Cambia de directorio.

dir – Lista los archivos y carpetas de un directorio.

tree – Muestra la estructura de directorios.

copy – Copia archivos.

type – Muestra contenido de archivos de texto.

more – Muestra salida paginada de archivos o comandos largos.

🧾 Comandos extra útiles (no vistos a fondo, pero importantes):
chkdsk – Verifica errores en discos duros.

driverquery – Lista los controladores instalados.

sfc /scannow – Escanea y repara archivos de sistema dañados.

📝 Nota: En casi todos los comandos puedes usar /? al final para ver su ayuda (ej. ping /?).

⚙️ Introducción a PowerShell:
PowerShell es un entorno más potente que cmd. Combina:

Shell de línea de comandos.

Lenguaje de scripting.

Herramientas para administración de sistemas.

Usa cmdlets con la estructura Verbo-Sustantivo como Get-Process o Set-Location.

📂 Ejemplos básicos de cmdlets:
Get-Process – Muestra los procesos activos.

Get-Service – Lista servicios activos o detenidos.

Set-Location (cd) – Cambia de directorio.

Get-ChildItem (dir o ls) – Lista archivos y carpetas.

Get-FileHash – Genera hashes de archivos.

Invoke-Command – Ejecuta comandos de forma remota.

Select-Object – Permite mostrar propiedades específicas.

🔎 Operadores de comparación en PowerShell:
-eq → Igual a

-ne → Distinto de

-gt → Mayor que

-ge → Mayor o igual que

-lt → Menor que

-le → Menor o igual que

📌 Estos se usan comúnmente con Where-Object, por ejemplo:

powershell
Copiar
Editar
Get-ChildItem | Where-Object { $_.Length -gt 100 }
Esto filtra los archivos del directorio actual que pesen más de 100 bytes.

💡 Buenas prácticas aprendidas:
Siempre especificar -Path o -Property explícitamente es útil, incluso si no es obligatorio.

Se pueden combinar operadores, filtros y proyecciones (Select-Object) para mejorar búsquedas.

Aprender a navegar entre rutas absolutas (C:\Users\...) y relativas (.\mi-carpeta) es clave.

El uso de $_. representa el objeto actual en el pipeline (se usa mucho en Where-Object).
