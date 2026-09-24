FacturaYA para Android
=====================

APK oficial nativa de FacturaYA (https://facturaya-wbed.onrender.com),
escrita en Flutter: punto de venta, turnos e inventario para tu negocio,
con o sin internet.

Version actual: 1.0.1 (versionCode 2002, Android de 64 bits).

Descarga
--------

Archivo: FacturaYA-v1.0.1.apk
Tamano: 19,7 MB
SHA-256: 9ecd1ad6a0ee2fd43c36f28d4acfca511f4e59bcedd5637237d2b8d573d72349
Descarga directa tambien desde la web oficial, en la seccion "App
nativa para Android" del landing, y adjunta al release v1.0.1 de este
mismo repositorio.

Requisitos
----------

- Android 6.0 o superior, telefono de 64 bits (2016 en adelante).
- Plan Pro de FacturaYA. La app nativa es exclusiva del plan Pro; la
  version web gratuita sigue disponible en el navegador con la misma
  cuenta.

Instalacion
-----------

1. Descarga el archivo FacturaYA-v1.0.1.apk.
2. Abre la descarga desde la barra de notificaciones o la carpeta
   Descargas.
3. Si Android lo pide, activa "Permitir de esta fuente" o "Instalar
   apps desconocidas" para tu navegador o gestor de archivos y
   confirma la instalacion.
4. Entra con tu cuenta (correo Gmail) o como cajero con tu codigo de 4
   digitos.

Novedades de la 1.0.1
---------------------

- Chat de soporte convertido en interruptor de un solo estado: el mismo
  boton abre y cierra, con boton visible para cerrar y el boton Atras
  de Android tambien lo cierra.
- Panel corregido: ventas y netos de hoy y del mes, conteo de productos
  y equipo leyendo los campos reales del servidor, con calculo offline
  (cache + cola de ventas pendientes) y refresco automatico tras cada
  venta, sincronizacion o cambio de inventario. Avisos con singular y
  plural correctos y badge de sincronizacion al dia.
- Icono y splash oficiales de la web (recibo sobre zinc-950), con icono
  adaptativo foreground, background y monocromo para Android 13+.
- Entrada "Entrar como cajero" con teclado numerico propio, indicadores
  animados, vibracion haptica, sacudida en el error y bloqueo temporal
  tras varios intentos. Funciona sin internet con el hash del PIN
  guardado cifrado tras el primer inicio de sesion del dueno.
- La app nativa exige Plan Pro, con validacion al entrar y cada 6 horas
  y 72 horas de gracia sin conexion; pantalla de bloqueo con campo de
  clave de licencia y acceso a soporte.
- Contador de dinero rehecho: sin filas tapadas por la barra inferior,
  campo de cantidad fijo con teclado numerico, subtotales en una linea
  y textos con singular y plural correctos.
- Punto de venta rehecho: tarjetas con nombre a 2 lineas, precio en una
  linea y stock dentro; chips de categoria sin cortes y aviso de
  productos que viven en el almacen.
- Animaciones sutiles que respetan la opcion de reducir animaciones del
  sistema, y ortografia revisada con tildes en toda la interfaz.

La 1.0.0 fue la primera version publica (punto de venta completo,
turnos, almacen, contador de dinero, venta offline del plan Pro y
sonido de transaccion finalizada).

Codigo fuente
-------------

Este repositorio publico distribuye solo la APK firmada. El codigo
fuente completo vive en el repositorio privado de FacturaYA.
