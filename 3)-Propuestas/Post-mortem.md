# Documento Post-Mortem

## 1. Resumen del incidente
Durante la primera semana de implementación del sistema digital, se detectó un desfase crítico en el inventario y una pérdida de pedidos recibidos vía WhatsApp. El incidente ocurrió debido a que el sistema no estaba sincronizado correctamente con la modalidad de **"entrega a domicilio"**.  

Mientras un encargado entregaba pedidos fuera del local, el sistema permitía seguir vendiendo productos que ya habían sido despachados físicamente pero no descargados del sistema, provocando que los clientes en el local no pudieran adquirir productos que figuraban *"en existencia"*.

---

## 2. Linea del tiempo

<img width="1147" height="392" alt="image" src="https://github.com/user-attachments/assets/edb34bcf-6994-44f1-a0d1-0e3fb07f7db8" />


---

## 3. Impacto
El impacto fue de gravedad **alta** para la operatividad del negocio:

- **Usuarios del sistema:**  
  Los dos encargados experimentaron frustración y una carga de trabajo doble al tener que verificar manualmente qué productos quedaban realmente.

- **Clientes:**  
  Varios clientes de WhatsApp recibieron sus pedidos con retraso y otros en el local no pudieron comprar productos específicos por errores de stock.

- **Negocio:**  
  Se perdió la trazabilidad de las cuentas del día, volviendo temporalmente al registro manual, lo que generó desorden en el cierre de caja.

---

## 4. Causa raíz (Análisis de los 5 porqués)

- **¿Por qué hubo desfase en el inventario?**  
  Porque el sistema no descontaba los productos en el momento que salían para entrega.

- **¿Por qué no se descontaban al salir?**  
  Porque no había una función de *"Pedido en tránsito"* que bloqueara el stock.

- **¿Por qué no existía esa función?**  
  Porque en el diseño inicial se priorizó la venta directa sobre el mostrador.

- **¿Por qué se priorizó el mostrador?**  
  Porque no se analizó a fondo que el encargado de entregas pasa mucho tiempo fuera del local sin acceso a la computadora principal.

- **¿Por qué no se consideró esto?**  
  Por una falta de comunicación sobre la dinámica real de movimiento del personal durante las horas pico.

---

## 5. Acciones tomadas para solucionarlo

- **Inmediata:**  
  Se habilitó un registro temporal en papel para las salidas a domicilio para ajustar el sistema manualmente cada hora.

- **Técnica:**  
  Se implementó una actualización en el módulo de inventario que permite marcar productos como *"Apartados para entrega"* desde el celular.

- **Proceso:**  
  El encargado de local ahora valida los pedidos de WhatsApp antes de confirmar cualquier venta física de productos con bajo stock.

---

## 6. Acciones a futuro

- **Sincronización Móvil:**  
  Instalar la aplicación del sistema en el teléfono del encargado que realiza las entregas para que pueda actualizar el estado del pedido en tiempo real.

- **Alertas de Stock Mínimo:**  
  Configurar notificaciones automáticas que avisen a ambos encargados cuando un producto de alta rotación (como aguas o papel bond) baje de cierta cantidad.

- **Capacitación:**  
  Realizar una sesión de repaso sobre el nuevo flujo de trabajo para asegurar que ambos dominen el registro de gastos de ruta y ventas híbridas.
