# EJERCICIO 07: Restricciones

## Objetivo
Identificar las restricciones que condicionan las decisiones de diseño y arquitectura del sistema.

| Código | Restricción | Descripción |
|---|---|---|
| **R-01** | **Plataforma web** | El sistema deberá implementarse como una aplicación web accesible desde navegadores modernos, tanto en computadoras como en dispositivos móviles. |
| **R-02** | **Integración con pasarela de pago** | El sistema deberá utilizar un servicio externo de pago para procesar las transacciones realizadas por los clientes. |
| **R-03** | **Integración con servicios externos** | El marketplace deberá comunicarse con servicios de envío, facturación y ERP para obtener o enviar información relacionada con pedidos, comprobantes, productos y stock. |
| **R-04** | **Base de datos centralizada** | La información principal del marketplace, como usuarios, productos, pedidos y ventas, deberá almacenarse en una base de datos centralizada. |
| **R-05** | **Seguridad de las comunicaciones** | La comunicación entre el cliente, el marketplace y los servicios externos deberá realizarse mediante conexiones seguras utilizando HTTPS. |
| **R-06** | **Dependencia de servicios externos** | Algunas funcionalidades del sistema dependerán de la disponibilidad de la pasarela de pago, servicio de envío, servicio de facturación y ERP. |
| **R-07** | **Recursos limitados del proyecto** | Al tratarse de un proyecto académico, el desarrollo deberá realizarse considerando recursos limitados de infraestructura, tiempo y presupuesto. |
| **R-08** | **Compatibilidad** | El sistema deberá ser compatible con los principales navegadores web actuales para permitir el acceso de diferentes tipos de usuarios. |

---

## Impacto de las restricciones en la arquitectura

Estas restricciones condicionan diferentes decisiones arquitectónicas. Por ejemplo, al tratarse de una aplicación web será necesario separar la interfaz de usuario de la lógica del sistema. La integración con servicios externos requerirá mecanismos de comunicación mediante APIs.

Asimismo, la dependencia de servicios como la pasarela de pago, facturación, ERP y envío implica que el sistema debe estar preparado para manejar posibles fallos o interrupciones externas. Las limitaciones de tiempo y recursos también deberán considerarse al seleccionar tecnologías e infraestructura.