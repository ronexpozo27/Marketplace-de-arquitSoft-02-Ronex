# EJERCICIO 05: Requisitos Funcionales

## Objetivo
Identificar las funciones principales que deberá realizar el sistema para satisfacer las necesidades de los usuarios y permitir la interacción con los servicios externos.

| Código | Requisito funcional |
|---|---|
| **RF-01** | El sistema deberá permitir al cliente buscar productos disponibles en el marketplace. |
| **RF-02** | El sistema deberá permitir al cliente consultar la información detallada de un producto, incluyendo nombre, descripción, precio y disponibilidad. |
| **RF-03** | El sistema deberá permitir al cliente agregar productos al carrito de compras. |
| **RF-04** | El sistema deberá permitir al cliente modificar o eliminar productos de su carrito de compras. |
| **RF-05** | El sistema deberá permitir al cliente generar un pedido con los productos seleccionados. |
| **RF-06** | El sistema deberá permitir al cliente realizar el pago de su pedido mediante una pasarela de pago. |
| **RF-07** | El sistema deberá registrar el resultado de la transacción de pago realizada por el cliente. |
| **RF-08** | El sistema deberá permitir al cliente consultar sus pedidos realizados y el estado de cada uno. |
| **RF-09** | El sistema deberá permitir al Seller registrar nuevos productos en el marketplace. |
| **RF-10** | El sistema deberá permitir al Seller actualizar la información de los productos que ofrece. |
| **RF-11** | El sistema deberá permitir al Seller consultar sus productos publicados. |
| **RF-12** | El sistema deberá permitir al Seller consultar la información relacionada con sus ventas. |
| **RF-13** | El sistema deberá permitir al Administrador gestionar los usuarios registrados en la plataforma. |
| **RF-14** | El sistema deberá permitir al Administrador supervisar los productos publicados en el marketplace. |
| **RF-15** | El sistema deberá permitir al Administrador gestionar la información general de la plataforma. |
| **RF-16** | El sistema deberá enviar la información del pago a la pasarela de pago y recibir el resultado de la transacción. |
| **RF-17** | El sistema deberá enviar la información necesaria del pedido al servicio de envío para gestionar la entrega. |
| **RF-18** | El sistema deberá consultar el estado del envío para informar al cliente sobre su pedido. |
| **RF-19** | El sistema deberá enviar la información de la compra al servicio de facturación para generar el comprobante de pago. |
| **RF-20** | El sistema deberá consultar al ERP la información de productos, precios y stock. |
| **RF-21** | El sistema deberá actualizar la disponibilidad de los productos utilizando la información proporcionada por el ERP. |
| **RF-22** | El sistema deberá permitir al Administrador consultar y supervisar las actividades realizadas dentro de la plataforma. |

---

# Relación entre Historias de Usuario y Requisitos Funcionales

## Objetivo
Relacionar las historias de usuario con los requisitos funcionales que permiten satisfacer las necesidades identificadas para cada actor del sistema.

| Historia de Usuario | Descripción resumida | Requisitos Funcionales relacionados |
|---|---|---|
| **HU-01** | Buscar productos. | RF-01 |
| **HU-02** | Consultar información de un producto. | RF-02 |
| **HU-03** | Agregar productos al carrito. | RF-03, RF-04 |
| **HU-04** | Realizar un pedido. | RF-05 |
| **HU-05** | Efectuar el pago del pedido. | RF-06, RF-07, RF-16, RF-19 |
| **HU-06** | Consultar pedidos y conocer su estado. | RF-08, RF-17, RF-18 |
| **HU-07** | Registrar productos. | RF-09 |
| **HU-08** | Actualizar información de productos. | RF-10, RF-20, RF-21 |
| **HU-09** | Consultar productos publicados. | RF-11 |
| **HU-10** | Consultar ventas realizadas. | RF-12 |
| **HU-11** | Gestionar información relacionada con las ventas. | RF-12, RF-17 |
| **HU-12** | Gestionar usuarios de la plataforma. | RF-13 |
| **HU-13** | Supervisar productos publicados. | RF-14 |
| **HU-14** | Administrar información general de la plataforma. | RF-15 |
| **HU-15** | Supervisar las actividades realizadas en la plataforma. | RF-22 |

---

## Requisitos de integración

Los siguientes requisitos funcionales permiten que el marketplace se comunique con sistemas y servicios externos.

| Sistema externo | Requisitos relacionados | Función |
|---|---|---|
| **Pasarela de pago** | RF-06, RF-07, RF-16 | Procesar el pago y comunicar el resultado de la transacción. |
| **Servicio de envío** | RF-17, RF-18 | Gestionar la entrega y proporcionar el estado del envío. |
| **Servicio de facturación** | RF-19 | Generar el comprobante correspondiente a la compra. |
| **ERP** | RF-20, RF-21 | Proporcionar información de productos, precios, disponibilidad y stock. |