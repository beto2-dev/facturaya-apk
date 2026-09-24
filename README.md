FacturaYA para Android
=====================

APK oficial nativa de FacturaYA (https://facturaya-wbed.onrender.com),
escrita en Flutter: punto de venta, turnos e inventario para tu negocio,
con o sin internet.

Version actual: 1.0.3 (compilacion 2004 en arm64).

Descarga
--------

La APK recomendada para la mayoria de los telefonos es la arm64-v8a.
Las tres cubren las arquitecturas de Android que soporta Flutter (el
x86 de 32 bits fue retirado del SDK).

| Archivo | Arquitectura | Tamaño | versionCode | SHA-256 |
|---------|--------------|--------|-------------|---------|
| FacturaYA-v1.0.3-arm64-v8a.apk | arm64-v8a (recomendada) | 19,1 MB | 2004 | 5c0589e97ea5fcf7b3bbd93c1b3a7473b89a4892b55192af57a41b872386cd02 |
| FacturaYA-v1.0.3-armeabi-v7a.apk | armeabi-v7a | 16,9 MB | 1004 | c164019fa32a770be885113f29388228b16fdbba0b318c6f7e8e92881466fdd7 |
| FacturaYA-v1.0.3-x86_64.apk | x86_64 | 20,6 MB | 4004 | 02a15f4919fff9859572ea05ea2161c97a447a1793bf69273be00a625931fa3c |

Descarga directa tambien desde la web oficial, en la seccion "App
nativa para Android" del landing (es una de las primeras secciones de
la pagina), y adjuntas al release v1.0.3 de este mismo repositorio.

Si ya tenias la 1.0.2 instalada, la arm64 se actualiza sola encima
(versionCode 2004 > 2003) sin desinstalar nada.

Requisitos
----------

Android 6.0 o superior. La app exige el Plan Pro de FacturaYA (el plan
gratuito sigue usando la web con la misma cuenta).

Que trae la 1.0.3
------------------

- Entrada del cajero con SESION REAL emitida por el servidor (nunca
  la sesion del dueno de la cuenta).
- La cola offline ya no pierde las ventas rechazadas: se quedan con su
  error hasta corregirlas.
- Impresion de tickets por Bluetooth (ESC/POS 58/80 mm) como la web.
- Exportacion del IPV a Excel (dia, mes y turno), calendario de
  ingresos y revocacion de ventas.
- Recetas de ingredientes que descuentan stock al vender.
- Tema claro/oscuro manual y Ajustes sin la seccion Servidor.

Firma
-----

Todas las APKs estan firmadas con la clave de release de FacturaYA
(CN=FacturaYA, O=beto2-dev). El keystore NO vive en ningun
repositorio: se inyecta como secreto al compilar.
