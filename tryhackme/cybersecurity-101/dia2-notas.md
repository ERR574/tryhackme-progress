🧠 Active Directory & Dominios – Notas Personales
🧩 ¿Qué es un dominio en Windows?
Un dominio de Windows es un grupo de usuarios y equipos administrados de forma centralizada por una empresa. Su propósito es unificar la administración de dispositivos, usuarios y recursos comunes de una red en un entorno Windows.

El dominio se administra a través de Active Directory (AD), y el servidor que ejecuta este servicio se llama Controlador de Dominio (DC).

📚 Active Directory Domain Services (AD DS)
El AD DS actúa como un catálogo que contiene información de todos los objetos dentro de una red. Algunos de los objetos comunes son:

👤 Usuarios

💻 Máquinas

🖨️ Impresoras

📁 Recursos compartidos

🛡️ Grupos de seguridad

👥 Tipos de usuarios en AD
Los usuarios son entidades de seguridad (security principals), lo que significa que pueden autenticarse y tener privilegios sobre recursos de red.

Pueden representar:

Personas (como empleados)

Servicios (como IIS o MSSQL)

⚠️ Los servicios solo tienen los privilegios mínimos necesarios para funcionar, a diferencia de un usuario humano.

🖥️ Máquinas como objetos
Cada máquina que se une al dominio tiene una cuenta como objeto en AD.

Se identifican con un nombre seguido de $, por ejemplo: TOM-PC$.

Estas cuentas son también entidades de seguridad.

🧱 Grupos de seguridad y UO
Característica	Grupos de Seguridad	Unidades Organizativas (OU)
Aplicación de permisos	✅ Sí	🚫 No
Aplicación de políticas (GPO)	🚫 No	✅ Sí
Puede tener varios	✅ Sí	🚫 No (solo una OU por usuario/máquina)

Además, aprendimos sobre la delegación, que consiste en otorgar a ciertos usuarios permisos sobre una OU sin que sean administradores del dominio.

🧑‍⚖️ GPO (Group Policy Objects)
Los GPOs permiten aplicar configuraciones de forma masiva a los objetos dentro de una OU.

Pueden estar dirigidos a usuarios o equipos.

Se almacenan y distribuyen desde un recurso clave: SYSVOL.

🗃️ ¿Qué es SYSVOL?
SYSVOL (System Volume) es una carpeta compartida en todos los DCs del dominio.

Es el punto de encuentro entre los Domain Controllers y las máquinas cliente.

Almacena los GPOs y otros archivos necesarios para políticas de red.

🔁 Replicación de SYSVOL
🧓 NTFRS: método antiguo.

🆕 DFSR: más moderno, eficiente y recomendado.

🔐 Métodos de autenticación
✅ Kerberos (actual)
Se envía usuario + marca de tiempo cifrada con una clave derivada de la contraseña al KDC (en el DC).

El KDC devuelve un TGT (Ticket Granting Ticket) y una clave de sesión.

Con ese TGT se puede pedir acceso a recursos (archivos, impresoras, servicios...).

Se genera un TGS (Ticket de Servicio) y una nueva clave.

El recurso descifra el TGS y se establece conexión.

🔐 El TGT está cifrado con el hash de la cuenta krbtgt y no puede ser accedido directamente por el usuario.

⚠️ NetNTLM (obsoleto pero aún disponible)
Utiliza desafíos y respuestas.

No se transmite la contraseña, pero es vulnerable a ataques modernos.

🌐 Dominio, Árbol y Bosque
Dominio: red privada con administración centralizada.

Árbol: conjunto de dominios con una jerarquía y confianza establecida.

Bosque: conjunto de árboles que comparten un esquema y pueden confiar entre sí.

Ejemplo real:

Bosque: BlackRock

Árbol: cada empresa subsidiaria

Dominio: cada sede o sucursal

🤝 Relaciones de confianza (Trust Relationships)
Permiten que un usuario de un dominio (A) acceda a recursos de otro dominio (B).

Se configuran entre dominios.

Pueden ser unidireccionales o bidireccionales.


