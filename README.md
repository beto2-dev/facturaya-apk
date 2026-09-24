FacturaYA para Android
=====================

APK oficial nativa de FacturaYA (https://facturaya-wbed.onrender.com),
escrita en Flutter: punto de venta, turnos e inventario para tu negocio,
con o sin internet.

Version actual: 1.0.3.1 (compilacion 2005 en arm64).

Descarga
--------

La APK recomendada para la mayoria de los telefonos es la arm64-v8a.
Las tres cubren las arquitecturas de Android que soporta Flutter (el
x86 de 32 bits fue retirado del SDK).

| Archivo | Arquitectura | Tamaño | versionCode | SHA-256 |
|---------|--------------|--------|-------------|---------|
| FacturaYA-v1.0.3.1-arm64-v8a.apk | arm64-v8a (recomendada) | 19,1 MB | 2005 | 493162a37d8d78aa4e5b24181f8115a86c0aff25a80baef042626f95156709a1 |
| FacturaYA-v1.0.3.1-armeabi-v7a.apk | armeabi-v7a | 16,9 MB | 1005 | c5689fb44f46e1aad064095122ffd2b0e3116e97223e2e99be181da1a1e28eab |
| FacturaYA-v1.0.3.1-x86_64.apk | x86_64 | 20,6 MB | 4005 | 45d3f82fbfd9a43bddd4da694f13370190088095b8f65f6bc16cd5c842cdbb57 |

Descarga directa tambien desde la web oficial, en la seccion "App
nativa para Android" del landing (es una de las primeras secciones de
la pagina), y adjuntas al release v1.0.3.1 de este mismo repositorio.

Si ya tenias la 1.0.3 instalada, la arm64 se actualiza sola encima
(versionCode 2005 > 2004) sin desinstalar nada.

Requisitos
----------

Android 6.0 o superior. La app exige el Plan Pro de FacturaYA (el plan
gratuito sigue usando la web con la misma cuenta).

Que trae la 1.0.3.1
-------------------

- El calendario de ingresos por fin carga: se acabo el "Rango de
  fechas no valido". Los bordes del mes se piden como dias de
  calendario y el servidor los convierte a la medianoche de la zona
  del negocio (America/Havana), igual que hace la web.
- El dia de cada venta lo calcula el SERVIDOR en la zona del negocio:
  la cuadricula cuadra con la jornada real aunque el telefono este en
  otra zona horaria.
- El calendario se filtra por sucursal con los mismos chips de
  Ventas (antes solo existia en la web).
- Todo lo de la 1.0.3 sigue igual: sesion real de cajero, cola offline
  sin perder ventas, impresion Bluetooth ESC/POS, exportacion del
  IPV, revocacion y recetas que descuentan stock.

Firma
-----

Todas las APKs estan firmadas con la clave de release de FacturaYA
(CN=FacturaYA, O=beto2-dev). El keystore NO vive en ningun
repositorio: se inyecta como secreto al compilar.
