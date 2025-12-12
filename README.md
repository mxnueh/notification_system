# Notification system
Aplicacion monolitica, realizada en python con una base de datos en SQL Server para administrar y monitorear las notificaciones de usuarios finales.
Esta aplicacion esta creada con el proposito de mostrar la seguridad de los datos y la persistencia de los mismos, tambien el uso basico de operaciones CRUD con una base de datos.

## 1.  Descripción
Es una aplicacion CLI implementada en python y SQL Server con la libreria **pyodbc**. La aplicacion permite crear usuarios, enviar notificaciones a usuarios existentes, 
consultar notificaciones de un usuario en especifico y marcar notificaciones como leídas.

## 2. Características
- **Gestión de usuarios:** Registro de usuarios con roles (administrador/usuario regular)
- **Creación de notificaciones:** Los administradores pueden crear y enviar notificaciones con título y mensaje
- **Envío selectivo:** Posibilidad de enviar una notificación a múltiples usuarios simultáneamente
- **Consulta de notificaciones:** Los usuarios pueden ver su bandeja de notificaciones ordenadas por fecha
- **Control de lectura:** Sistema de marcado de notificaciones como leídas/no leídas
- **Interfaz interactiva:** Menú de consola intuitivo para todas las operaciones

## 3. Estructura de la Base de Datos 
![alt text][logo]
[logo]: https://github.com/mxnueh/notification_system/blob/main/N_S%20diagram.png "Diagram Notification system"

## 4. Requisitos
- Python 3.14.0
- SQL Server (cualquier versión compatible con ODBC Driver 17)
- pyodbc

**Run:**
<pre>
  pip install pyodbc
</pre>

## 5. Configuración
⋅⋅⋅⋅* Crear el nombre de la base de datos en SQL Server:
⋅⋅⋅⋅* **Configurar la conexión**: Edita los parámetros de conexión en el código:

``` Python
   conn = pyodbc.connect(
       r'DRIVER={ODBC Driver 17 for SQL Server};'
       r'SERVER=TU_SERVIDOR;'
       r'DATABASE=notificaciones;'
       r'Trusted_Connection=yes;'
   )
```

## 6. Uso 
Ejecuta el archivo principal
<pre>
  python app.py
</pre>

**Menú de opciones:**
<pre>
  1. Agregar usuario - Registra un nuevo usuario en el sistema
  2. Crear y enviar notificación - Crea y envía una notificación a usuarios seleccionados
  3. Consultar notificaciones de un usuario - Ver bandeja de notificaciones
  4. Marcar notificación como leída - Actualiza el estado de lectura
  5. Salir - Cierra la aplicación
</pre>




