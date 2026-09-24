FacturaYA para Android
=====================

APK oficial nativa de FacturaYA (https://facturaya-wbed.onrender.com),
escrita en Flutter: punto de venta, turnos e inventario para tu negocio,
con o sin internet.

Version actual: 1.0.2 (versionCode 2003, Android de 64 bits).

Descarga
--------

Archivo: FacturaYA-v1.0.2.apk
Tamano: 19,8 MB
SHA-256: 8a45a52d95e473a73c01df9418223a41196c0814f83f21c6ba93779f64da58d5
Descarga directa tambien desde la web oficial, en la seccion "App
nativa para Android" del landing (es una de las primeras secciones de
la pagina), y adjunta al release v1.0.2 de este mismo repositorio.

Requisitos
----------

- Android 6.0 o superior, telefono de 64 bits (2016 en adelante).
- Plan Pro de FacturaYA. La app nativa es exclusiva del plan Pro; la
  version web gratuita sigue disponible en el navegador con la misma
  cuenta.

Instalacion
-----------

1. Descarga el archivo FacturaYA-v1.0.2.apk.
2. Abre la descarga desde la barra de notificaciones o la carpeta
   Descargas.
3. Si Android lo pide, activa "Permitir de esta fuente" o "Instalar
   apps desconocidas" para tu navegador o gestor de archivos y
   confirma la instalacion.
4. Entra con tu cuenta (correo Gmail) o como cajero con tu codigo de 4
   digitos.

Novedades de la 1.0.2
---------------------

- Teclado del codigo de cajero corregido: en la 1.0.1 las teclas no
  llegaban a pintarse dentro de la pantalla de entrada (falla de
  maquetado con el scroll) y parecia que no habia teclado ni input.
  Ahora el pad numerico se dibuja siempre, dentro de un scroll o en
  pantalla fija.
- Equipo con cuentas de Gmail: agrega a tus trabajadores con su
  correo, contrasena inicial, rol (Cajero o Administrador) y sucursal;
  cada uno vende a su nombre, igual que en la web.
- Sucursales multiples (Plan Pro): crear, renombrar y activar o
  desactivar sucursales; el administrador elige en cual vende en el
  punto de venta, las ventas quedan selladas con su sucursal (tambien
  las cobradas sin internet) y el historial de ventas se filtra por
  sucursal.
- Enlace "No tienes cuenta? Registrate aca" en la pantalla de entrada,
  que abre el registro de la web en el navegador del telefono.
- La lista de cajeros distingue cargando, sin conexion y sin cajeros,
  con boton de reintentar.

La 1.0.1 corrigio el Panel (campos reales del servidor), convirtio el
chat de soporte en interruptor de un solo estado, añadio el icono y
splash oficiales, la entrada de cajero con teclado propio y la exigencia
del Plan Pro. La 1.0.0 fue la primera version publica.

Codigo fuente
-------------

Este repositorio publico distribuye solo la APK firmada. El codigo
fuente completo vive en el repositorio privado de FacturaYA.
