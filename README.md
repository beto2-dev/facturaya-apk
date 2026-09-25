FacturaYA para Android
=====================

APK oficial nativa de FacturaYA (https://facturaya-wbed.onrender.com),
escrita en Flutter: punto de venta, turnos e inventario para tu negocio,
con o sin internet.

Version actual: 1.0.3.4 (compilacion 2008 en arm64).

Descarga
--------

La APK recomendada para la mayoria de los telefonos es la arm64-v8a.
Las tres cubren las arquitecturas de Android que soporta Flutter (el
x86 de 32 bits fue retirado del SDK).

| Archivo | Arquitectura | Tamaño | versionCode | SHA-256 |
|---------|--------------|--------|-------------|---------|
| FacturaYA-v1.0.3.4-arm64-v8a.apk | arm64-v8a (recomendada) | 20,1 MB | 2008 | 6a24015e60435366146b4e0e3d985728161cd93acfb7add4391307be1520f234 |
| FacturaYA-v1.0.3.4-armeabi-v7a.apk | armeabi-v7a | 17,7 MB | 1008 | 9a75982bf7330e2cdf6e771e60e9f9364c323c6fcbb9aac73ae73e544efd9d21 |
| FacturaYA-v1.0.3.4-x86_64.apk | x86_64 | 21,6 MB | 4008 | 7fd2f9be947306259feb4137cb39ed4fea9d7e833d2c7908eedde89dc475427a |

Descarga directa tambien desde la web oficial, en la seccion "App
nativa para Android" del landing (es una de las primeras secciones de
la pagina), y adjuntas al release v1.0.3.4 de este mismo repositorio.

Si ya tenias la 1.0.3.3 (o cualquier version anterior) instalada, la
arm64 se actualiza sola encima (versionCode 2008 > 2007) sin
desinstalar nada.

Requisitos
----------

Android 6.0 o superior. La app exige el Plan Pro de FacturaYA (el plan
gratuito sigue usando la web con la misma cuenta).

Que trae la 1.0.3.4
-------------------

- RESPALDO DEL SERVIDOR (FAILOVER): el servidor de FacturaYA corre
  ahora SIMULTANEAMENTE en Render (el oficial) y en un servidor de
  respaldo contra la MISMA base de datos y la misma logica de negocio.
  Si la red del principal cae (timeout, DNS, conexion rota), la MISMA
  peticion se reintenta en el respaldo: una venta en curso no se pierde
  nunca por una caida de Render. Un 5xx se reintenta una vez en el
  mismo servidor antes de conmutar; los 4xx del negocio (stock,
  permisos, validaciones) NUNCA conmutan. Mientras se usa el respaldo,
  el principal se sondea cada 10 minutos y la app vuelve sola en
  cuanto responde. La web hace lo mismo a nivel de pagina.
- Nuevo GET /api/health: sonda de salud sin sesion que responde
  version y estado de la base; es la que usan la app, la web y el
  monitor del respaldo.
- Todo lo de la 1.0.3.3 y anteriores sigue igual: cierre de turno como
  cajero, stock sin sobrevender, anti-fraude, verificacion de firma de
  la APK, apertura del turno, textos sin desbordes, cantidad a mano en
  el carrito, calendario con filtro por sucursal, sesion real de
  cajero, cola offline sin perder ventas, impresion Bluetooth ESC/POS,
  exportacion del IPV, revocacion y recetas que descuentan stock.

Firma
-----

Todas las APKs estan firmadas con la clave de release de FacturaYA
(CN=FacturaYA, O=beto2-dev; huella SHA-256 del certificado
c74407bb7cca04019b361951d5cf4b2ae29ba19ed79b566ac335d9a4a9ed508f).
El keystore NO vive en ningun repositorio: se inyecta como secreto al
compilar.
