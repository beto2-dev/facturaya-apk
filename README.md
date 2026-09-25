FacturaYA para Android
=====================

APK oficial nativa de FacturaYA (https://facturaya-wbed.onrender.com),
escrita en Flutter: punto de venta, turnos e inventario para tu negocio,
con o sin internet.

Version actual: 1.0.3.3 (compilacion 2007 en arm64).

Descarga
--------

La APK recomendada para la mayoria de los telefonos es la arm64-v8a.
Las tres cubren las arquitecturas de Android que soporta Flutter (el
x86 de 32 bits fue retirado del SDK).

| Archivo | Arquitectura | Tamaño | versionCode | SHA-256 |
|---------|--------------|--------|-------------|---------|
| FacturaYA-v1.0.3.3-arm64-v8a.apk | arm64-v8a (recomendada) | 20,1 MB | 2007 | fa4bbe806bd0e53ec3c79c89a2942c88262013a9de1f100fff55279c0632db1b |
| FacturaYA-v1.0.3.3-armeabi-v7a.apk | armeabi-v7a | 17,7 MB | 1007 | 1e9e2a19e4b0e53fc33cd8132c6db130ff62f18f3299204e4b835932bba161d7 |
| FacturaYA-v1.0.3.3-x86_64.apk | x86_64 | 21,6 MB | 4007 | 94b5cdcca67043545038372959b73ca4653ee08e03b199a97fb66d73c681b3d7 |

Descarga directa tambien desde la web oficial, en la seccion "App
nativa para Android" del landing (es una de las primeras secciones de
la pagina), y adjuntas al release v1.0.3.3 de este mismo repositorio.

Si ya tenias la 1.0.3.2 (o cualquier version anterior) instalada, la
arm64 se actualiza sola encima (versionCode 2007 > 2006) sin
desinstalar nada.

Requisitos
----------

Android 6.0 o superior. La app exige el Plan Pro de FacturaYA (el plan
gratuito sigue usando la web con la misma cuenta).

Que trae la 1.0.3.3
-------------------

- Cerrar turno como cajero ya no se rechaza: el servidor encuentra el
  turno ABIERTO sellado con el perfil del cajero autenticado por
  codigo (y por el turno del dispositivo, con cierre idempotente:
  reintentar tras perder la respuesta devuelve el turno ya cerrado).
  El cajero tambien VE su turno abierto en la lista de turnos.
- El stock no se sobrevende: imposible cobrar mas unidades de las
  disponibles (si hay 45, no se puede vender 76). El carrito ajusta la
  cantidad al maximo disponible y lo avisa al agregar, al escribir la
  cantidad, al recargar la pantalla y antes de cobrar; el servidor
  valida lo mismo al cobrar y al sincronizar la cola offline (con el
  motivo del rechazo visible en el Panel).
- Protecciones anti-abuso y anti-fraude: el codigo PIN del cajero
  bloquea el perfil 15 minutos tras 3 intentos fallidos, las ventas
  duplicadas en pocos segundos se rechazan (con exencion de los
  reintentos reales) y el vendedor reincidente queda suspendido unos
  minutos, los carritos con precios manipulados desde el cliente se
  rechazan al momento (los precios SIEMPRE salen del servidor) y los
  limites de peticiones son mas estrictos en login, cobros,
  sincronizacion y turnos.
- Verificacion de firma de la APK: al arrancar, la app compara el
  certificado de la copia instalada contra el ORIGINAL de FacturaYA
  (huella SHA-256), comprueba el nombre del paquete, que sea un build
  de produccion y la integridad del propio APK por su hash. Una copia
  reempaquetada o alterada muestra el aviso de seguridad, cierra la
  sesion y borra los datos del telefono.
- Todo lo de la 1.0.3.2 y anteriores sigue igual: el turno abre,
  textos sin desbordes, cantidad a mano en el carrito, calendario con
  filtro por sucursal, sesion real de cajero, cola offline sin perder
  ventas, impresion Bluetooth ESC/POS, exportacion del IPV, revocacion
  y recetas que descuentan stock.

Firma
-----

Todas las APKs estan firmadas con la clave de release de FacturaYA
(CN=FacturaYA, O=beto2-dev). El keystore NO vive en ningun
repositorio: se inyecta como secreto al compilar.
