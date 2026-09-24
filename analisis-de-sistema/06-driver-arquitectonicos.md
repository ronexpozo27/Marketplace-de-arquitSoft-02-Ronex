# EJERCICIO 08: Drivers Arquitectónicos

## Objetivo
Integrar los elementos identificados anteriormente y determinar cuáles tienen una influencia significativa en las decisiones de arquitectura del sistema.

## ¿Qué es un driver arquitectónico?

Un driver arquitectónico es un requisito, atributo de calidad o restricción que tiene un impacto importante en la forma en que se diseña la arquitectura del sistema.

Para el marketplace de productos para mascotas, los principales drivers arquitectónicos son los siguientes:

| Código | Driver arquitectónico | Tipo | Influencia en la arquitectura |
|---|---|---|---|
| **DA-01** | **Alta concurrencia de usuarios** | Atributo de calidad | El sistema debe soportar una gran cantidad de usuarios consultando productos y realizando compras al mismo tiempo, por lo que la arquitectura debe permitir distribuir la carga de trabajo. |
| **DA-02** | **Escalabilidad** | Atributo de calidad | La arquitectura debe permitir aumentar la capacidad del sistema cuando crezca la cantidad de usuarios, productos, pedidos y transacciones. |
| **DA-03** | **Disponibilidad** | Atributo de calidad | El marketplace debe permanecer disponible incluso durante campañas comerciales o periodos de alta demanda, reduciendo al mínimo las interrupciones del servicio. |
| **DA-04** | **Seguridad de pagos y datos** | Atributo de calidad | La arquitectura debe proteger los datos de usuarios, pedidos y pagos, utilizando comunicaciones seguras y mecanismos de control de acceso. |
| **DA-05** | **Integración con servicios externos** | Requisito funcional / Restricción | El sistema debe integrarse con la pasarela de pago, servicio de envío, servicio de facturación y ERP mediante APIs u otros mecanismos de comunicación. |
| **DA-06** | **Confiabilidad de pedidos y pagos** | Atributo de calidad | La arquitectura debe evitar duplicaciones, pérdida de información o inconsistencias durante el registro de pedidos, pagos y actualización de stock. |
| **DA-07** | **Mantenibilidad** | Atributo de calidad | El sistema debe permitir modificar o agregar funcionalidades sin afectar innecesariamente otras partes del marketplace. |
| **DA-08** | **Recursos limitados del proyecto** | Restricción | Al tratarse de un proyecto académico, la arquitectura debe evitar soluciones innecesariamente complejas o costosas y utilizar tecnologías accesibles. |

---

## Drivers funcionales principales

Entre los requisitos funcionales, los que tienen mayor influencia en la arquitectura son:

| Requisito | Influencia |
|---|---|
| **RF-05 - Generar pedidos** | Requiere coordinar productos, stock, cliente y datos del pedido. |
| **RF-06 - Realizar pagos** | Requiere integración segura con una pasarela de pago externa. |
| **RF-17 - Gestionar envíos** | Requiere comunicación con un servicio externo de entrega. |
| **RF-19 - Generar comprobantes** | Requiere integración con un servicio de facturación. |
| **RF-20 y RF-21 - Consultar y actualizar stock** | Requiere comunicación con el ERP y mantener sincronizada la disponibilidad de productos. |

---

## Drivers de calidad principales

Los atributos de calidad con mayor impacto en la arquitectura son:

- **Rendimiento:** responder rápidamente ante múltiples solicitudes.
- **Escalabilidad:** soportar el crecimiento de usuarios y transacciones.
- **Disponibilidad:** mantener el sistema operativo durante periodos de alta demanda.
- **Seguridad:** proteger datos, cuentas y operaciones de pago.
- **Confiabilidad:** asegurar que pedidos, pagos y stock sean procesados correctamente.
- **Mantenibilidad:** facilitar cambios, correcciones y nuevas funcionalidades.

---

## Restricciones principales

Las restricciones que más condicionan la arquitectura son:

- El sistema debe funcionar como una **aplicación web**.
- Debe comunicarse con servicios externos mediante **APIs**.
- Las comunicaciones deben utilizar **HTTPS**.
- El sistema depende de servicios externos como pasarela de pago, facturación, envío y ERP.
- El proyecto cuenta con **recursos limitados de tiempo, infraestructura y presupuesto**.

---

## Conclusión

Los drivers arquitectónicos más importantes del marketplace son la escalabilidad, disponibilidad, seguridad, confiabilidad e integración con servicios externos. Estos elementos deben considerarse al momento de definir la arquitectura inicial, ya que influyen directamente en la forma en que se organizarán los componentes, servicios y mecanismos de comunicación del sistema.