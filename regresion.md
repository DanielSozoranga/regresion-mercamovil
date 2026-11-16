# Suite de regresión · Bug #482 · MercaMóvil

Cambio: se corrigió `recalcularTotal()`. Impacto: carrito, resumen de pago, cupones y persistencia (CarritoRepository).

| Caso | Descripción | Clasificación |
|---|---|---|
| C01 | Iniciar sesión con credenciales válidas | Smoke |
| C02 | Abrir el catálogo y ver la lista de productos | Smoke |
| C03 | Completar una compra de punta a punta | Smoke |
| C04 | Cambiar la cantidad y ver el total actualizado | Sanity |
| C05 | Eliminar un producto del carrito y ver el total recalculado | Sanity |
| C06 | Aplicar un cupón del 10% sobre el total | Regresión selectiva |
| C07 | El resumen de pago muestra el mismo total que el carrito | Regresión selectiva |
| C08 | El carrito conserva productos y total al cerrar y abrir la app | Regresión selectiva |
| C09 | Cambiar la foto de perfil | No ejecutar |
| C10 | Recibir una notificación push de promoción | No ejecutar |
| C11 | Cambiar el idioma de la app | No ejecutar |

## Veredicto

GO. La prueba sanity con Appium pasó en Android 14 con total 59.98 al subir la cantidad a 2. Riesgo restante: la regresión selectiva y la matriz en otros dispositivos aún no se ejecutaron.
