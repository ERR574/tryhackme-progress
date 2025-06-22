# 🪟 TryHackMe - Windows Fundamentals: Día 1

## 🧠 Qué aprendí

- Diferencias clave entre Windows 11 Home y Pro:  
  - **Windows 11 Pro** tiene habilitado **BitLocker** (cifrado de disco).  
  - **Windows 11 Home** no incluye BitLocker.

- ¿Qué es BitLocker?  
  BitLocker es una funcionalidad de Windows que permite cifrar el disco duro para proteger los datos en caso de pérdida o robo. Utiliza TPM (Trusted Platform Module) y puede proteger tanto el sistema como volúmenes secundarios.

- Variables del sistema:  
  - `%windir%` representa la carpeta del sistema Windows (normalmente `C:\Windows`).

- **Sistema de archivos NTFS**:  
  - Aprendimos a ver las propiedades de archivos y carpetas en sistemas con NTFS.
  - Exploramos cómo ver los **usuarios y grupos** que tienen permisos sobre recursos del sistema.
  - También revisamos los **niveles de permisos** (lectura, escritura, control total, etc.).

- **Cuentas de usuario y privilegios**:
  - En equipos domésticos, los usuarios suelen iniciar sesión como **administradores locales**.
  - Esto representa un riesgo, ya que cualquier malware se ejecutaría con los **mismos privilegios elevados** del usuario activo.
  - Para mitigar esto, Microsoft introdujo el **UAC (User Account Control)**.

### 🛡️ ¿Cómo funciona el UAC?
- Aunque un usuario pertenezca al grupo de administradores, **las aplicaciones no se ejecutan automáticamente con privilegios elevados**.
- Cuando una acción requiere esos permisos (instalar, modificar archivos del sistema), **UAC muestra una ventana solicitando confirmación**.
- Esto ayuda a prevenir instalaciones maliciosas sin consentimiento.

- También aprendimos a revisar los **permisos que tienen las aplicaciones antes y después de instalarse**, especialmente si usamos una cuenta con rol de administrador.

## ⚙️ Comandos y herramientas exploradas

- `%windir%` → variable para acceder directamente al directorio del sistema
- Propiedades de archivos y carpetas
- Panel de control → Cuentas de usuario
- Explorador de archivos y pestaña de **seguridad**
- UAC en acción (confirmación de permisos)
- **Administrador de tareas**: navegación básica y revisión de procesos activos

## ✅ Lab completado
- Fecha: 22 de junio de 2025
- Nivel: Básico
- Estado: ✔️ Completado
- Plataforma: TryHackMe

#IMPORTANTE-NOTA:
> Este documento fue redactado con ayuda de inteligencia artificial a partir de mis notas personales.  
> El contenido refleja mi aprendizaje real; la IA fue utilizada únicamente para mejorar la organización, redacción y presentación con el objetivo de mayor legibilidad a futuro.
---

✍️ ERR574
