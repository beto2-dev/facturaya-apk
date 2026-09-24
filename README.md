<div align="center">

# FacturaYA para Android

**El punto de venta de tu negocio, con o sin internet.**

APK oficial de FacturaYA · Versión **1.0.0**

</div>

---

## Descargar e instalar

1. Descarga el archivo **`FacturaYA-v1.0.0.apk`** (está en este repositorio y también en [Releases](https://github.com/beto2-dev/facturaya-apk/releases)).
2. Ábrelo desde la barra de notificaciones o desde la app **Archivos** de tu teléfono.
3. Si Android pregunta *"Instalar apps desconocidas"*, dale permiso a **Archivos** o a **Chrome** (es normal: la app no viene de Play Store).
4. Toca **Instalar** y ábrela.

> **Requisitos:** Android de 64 bits (cualquier teléfono de 2016 en adelante) con Android 7.0 o superior. Nada de pagos ni cuentas raras: entras con el correo y la contraseña de tu cuenta de FacturaYA.

## Qué hace la app

Es la misma FacturaYA de la web, en tu teléfono:

- **Punto de venta**: toca los productos, cobra con el importe recibido y te dice el cambio, con el sonido de *transacción finalizada* al completar cada venta.
- **Venta sin internet (plan Pro)**: si se cae la red, las ventas se guardan en el teléfono y se suben solas cuando vuelve la conexión.
- **Turnos de caja**: abre y cierra tu turno con cuadre de efectivo, y respeta el turno automático del negocio (bares y restaurantes).
- **Cajeros con código**: hasta 3 cajeros entran con su nombre y su código de 4 dígitos; funciona incluso **sin internet**.
- **Contador de dinero**: billetes de 1 a 5000 CUP con cantidades, total en vivo y desglose (gratis hasta 500; 1000+ es del plan Pro).
- **Administración completa**: productos, entradas de mercancía con almacenes, equipo, panel con los números del día y del mes, chat con soporte y ajustes del negocio.
- **Tus datos van siempre al mismo servidor de la web**: lo que vendes en el teléfono se ve en la web al instante.

## Seguridad

- Conexión **solamente por HTTPS** al servidor oficial; nada de HTTP sin cifrar.
- La sesión se guarda cifrada en el almacen privado de la app (no en la galería ni en archivos visibles).
- **Sin permisos** de contactos, ubicación, cámara ni almacenamiento.
- El código del cajero se verifica en el servidor y, sin internet, con un comprobador criptográfico local (sha256) con bloqueo de 5 intentos por 10 minutos.
- Respaldos del teléfono desactivados para la app: la sesión y la cola de ventas no se copian a otros equipos.

## Versiones

| Versión | Qué trae |
|---------|----------|
| **1.0.0** | Primera versión: punto de venta, venta sin internet (Pro), turnos con cuadre y turno automático, cajeros con código (hasta 3, con entrada offline), contador de dinero, productos y almacenes, entradas de mercancía, equipo, panel, chat con soporte, feedback, conversor USD/CUP y sonido al cobrar. |

## Sobre este repositorio

Aquí vive **solo el APK compilado** (sin código fuente). El código fuente de FacturaYA es privado. Si encuentras un problema o quieres sugerir algo, escríbenos desde la app: **Ajustes → Enviar feedback** o el chat de soporte.

**FacturaYA** · Hecho con ❤️ para los negocios cubanos.
