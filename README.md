FacturaYA para Android
=====================

APK oficial nativa de FacturaYA (https://facturaya-wbed.onrender.com),
escrita en Flutter: punto de venta, turnos e inventario para tu negocio,
con o sin internet.

Version actual: 1.0.3.2 (compilacion 2006 en arm64).

Descarga
--------

La APK recomendada para la mayoria de los telefonos es la arm64-v8a.
Las tres cubren las arquitecturas de Android que soporta Flutter (el
x86 de 32 bits fue retirado del SDK).

| Archivo | Arquitectura | Tamaño | versionCode | SHA-256 |
|---------|--------------|--------|-------------|---------|
| FacturaYA-v1.0.3.2-arm64-v8a.apk | arm64-v8a (recomendada) | 20,1 MB | 2006 | fb5118c77d611c2ccffe946cd6a1b69a318cef756894bef86dba325ffbb7606c |
| FacturaYA-v1.0.3.2-armeabi-v7a.apk | armeabi-v7a | 17,7 MB | 1006 | a7e811fa4aba25aeaced543a4f36bc8fbace5f05915f30efb64be655022e1931 |
| FacturaYA-v1.0.3.2-x86_64.apk | x86_64 | 21,6 MB | 4006 | 90fabd9c2cbe221b7255f08618b0c3c4dd4d98750ab5aeb5272dea3b7e1ac46c |

Descarga directa tambien desde la web oficial, en la seccion "App
nativa para Android" del landing (es una de las primeras secciones de
la pagina), y adjuntas al release v1.0.3.2 de este mismo repositorio.

Si ya tenias la 1.0.3 o la 1.0.3.1 instaladas, la arm64 se actualiza
sola encima (versionCode 2006 > 2005) sin desinstalar nada.

Requisitos
----------

Android 6.0 o superior. La app exige el Plan Pro de FacturaYA (el plan
gratuito sigue usando la web con la misma cuenta).

Que trae la 1.0.3.2
-------------------

- Abrir turno como cajero ya no falla con "Solo los cajeros y
  trabajadores abren turnos": la sesion del cajero por codigo viaja
  sobre la cuenta del dueno (es quien sostiene la integridad de las
  ventas) y el servidor la confundia con la del administrador. Ahora
  el turno se abre y se sincroniza sellado con el perfil del cajero
  (quien, cuando y en que sucursal).
- Los textos no se salen de sus contenedores: los importes grandes del
  calendario de ingresos (mes, ano e historico) y las celdas de los
  dias se encogen si no caben, los filtros de sucursal fluyen en
  varias lineas y las filas de totales de Ventas y Turnos aguantan la
  letra grande del telefono.
- La version de Ajustes ya no se queda atras: dice 1.0.3.2.
- La cantidad del carrito se escribe a mano en el punto de venta: se
  toca el numero entre los botones de sumar y restar y se teclea la
  cantidad exacta (1 a 10.000, el mismo limite del servidor).
- Todo lo de la 1.0.3.1 y la 1.0.3 sigue igual: calendario con filtro
  por sucursal, sesion real de cajero, cola offline sin perder ventas,
  impresion Bluetooth ESC/POS, exportacion del IPV, revocacion y
  recetas que descuentan stock.

Firma
-----

Todas las APKs estan firmadas con la clave de release de FacturaYA
(CN=FacturaYA, O=beto2-dev). El keystore NO vive en ningun
repositorio: se inyecta como secreto al compilar.
