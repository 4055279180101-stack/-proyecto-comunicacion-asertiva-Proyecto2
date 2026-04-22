# Flujo de Negocio — Centrocolor Librería y Abarrotería
**Encargada:** Claudia | **Fecha:** 12/04/2026

---

## Actores
- **Claudia** — Encargada del local
- **Segunda persona** — Compras y entregas
- **Cliente** — Presencial, por teléfono, correo o WhatsApp
- **SAT** — Facturación electrónica

---

## 1. Recepción de Pedidos
1. El cliente contacta por teléfono, WhatsApp o correo.
2. Se registra el pedido en un lugar centralizado.
3. Se verifica si el producto está disponible.
4. Si no hay stock, se activa una alerta para reabastecerse.

## 2. Control de Inventario
1. El sistema lleva el registro del stock.
2. Cuando un producto está por agotarse, genera una alerta.
3. La segunda persona sale a comprar lo que falta.
4. Al regresar, se actualiza el inventario.

## 3. Pedidos de Productos Generales
1. Se verifica el stock.
2. Se empaca el pedido.
3. Si el cliente pide entrega a domicilio, se registra como pendiente.
4. Si no, se entrega en el mostrador.

## 4. Trabajos de Impresión y Encuadernación
1. El cliente solicita el trabajo.
2. Se registran las especificaciones: tamaño, color, tipo de documento y cantidad.
3. Se verifica que el archivo esté bien configurado.
4. Si hay un problema, se notifica al cliente para que lo corrija.
5. Se ejecuta el trabajo y se entrega.

## 5. Entregas a Domicilio
1. El pedido se registra con los datos del cliente y la dirección.
2. El estado inicia como **Pendiente**.
3. La segunda persona sale a entregar: estado **En proceso**.
4. Al confirmar la entrega: estado **Completada**.

## 6. Facturación
1. Se genera la factura electrónica a través de la SAT.
2. El cliente paga.
3. La venta queda registrada en el historial.

## 7. Clientes Frecuentes
1. Cuando un cliente hace un pedido recurrente, se busca si ya está registrado.
2. Si no está, se registra su nombre, contacto y preferencias de entrega.
3. La próxima vez, sus datos se cargan automáticamente para agilizar la atención.

## 8. Historial de Ventas
1. La encargada consulta el historial cuando necesita tomar decisiones de compra.
2. Puede filtrar por producto, fecha o cantidad vendida.
3. Identifica qué productos se venden más y en qué momentos.

---

## Requisitos No Funcionales

**Facilidad de uso:** El sistema debe ser simple de usar, sin requerir capacitación técnica extensa.

**Disponibilidad:** La solución debe estar disponible de lunes a sábado de 6:00 am a 9:00 pm sin interrupciones.

**Multiplataforma:** Debe poder consultarse desde el celular o cualquier dispositivo con acceso a internet.
