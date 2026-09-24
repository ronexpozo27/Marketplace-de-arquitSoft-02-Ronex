# EJERCICIO 06: Atributos de Calidad

## Objetivo
Determinar cómo debe comportarse el sistema, además de las funciones que debe realizar.

## Escenario analizado
Durante una campaña comercial, el marketplace podría recibir una gran cantidad de usuarios consultando productos y realizando compras simultáneamente. En este contexto, el sistema debe mantener un funcionamiento estable, rápido y seguro.

| Código | Atributo de calidad | Descripción |
|---|---|---|
| **AC-01** | **Rendimiento** | El sistema debe responder rápidamente a las solicitudes de los usuarios, incluso cuando exista una gran cantidad de consultas, búsquedas y compras simultáneas. |
| **AC-02** | **Disponibilidad** | El marketplace debe permanecer disponible durante la mayor parte del tiempo, especialmente en campañas comerciales, evitando interrupciones que impidan a los clientes realizar compras. |
| **AC-03** | **Escalabilidad** | El sistema debe poder aumentar su capacidad cuando crezca la cantidad de usuarios, productos, pedidos o transacciones, sin afectar significativamente su funcionamiento. |
| **AC-04** | **Seguridad** | El sistema debe proteger la información de los usuarios, pedidos y pagos, evitando accesos no autorizados y garantizando una comunicación segura con los servicios externos. |
| **AC-05** | **Mantenibilidad** | El sistema debe estar organizado de manera que sea posible corregir errores, modificar funcionalidades e incorporar nuevas características sin afectar innecesariamente otras partes de la plataforma. |
| **AC-06** | **Confiabilidad** | El sistema debe procesar correctamente las operaciones realizadas por los usuarios, evitando pérdidas, duplicaciones o inconsistencias en pedidos, pagos, stock y demás información importante. |

---

## Relación con el escenario

Durante una campaña comercial, el **rendimiento** permitirá atender muchas solicitudes sin generar tiempos de espera elevados. La **disponibilidad** permitirá que los usuarios puedan seguir utilizando la plataforma durante los periodos de mayor demanda.

La **escalabilidad** permitirá aumentar los recursos del sistema cuando crezca el número de usuarios. La **seguridad** protegerá las cuentas, pagos y datos personales. La **mantenibilidad** facilitará realizar mejoras o correcciones en el sistema, mientras que la **confiabilidad** ayudará a garantizar que pedidos, pagos y actualizaciones de stock se procesen correctamente.