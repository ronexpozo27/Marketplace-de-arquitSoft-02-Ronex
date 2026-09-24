# Arquitectura inicial del sistema

## Descripción general

La arquitectura inicial del **Marketplace de productos para mascotas** se plantea mediante una arquitectura en capas, separando la interacción con los usuarios, la lógica de negocio, el acceso a datos y la integración con servicios externos.

Esta separación permite organizar mejor las responsabilidades del sistema y facilita su mantenimiento, crecimiento e integración con otros servicios.

---

## Diagrama de arquitectura

```mermaid
flowchart TB

    %% =========================
    %% ACTORES
    %% =========================

    subgraph ACTORES["ACTORES"]
        direction LR
        Cliente["Cliente"]
        Seller["Seller"]
        Admin["Administrador"]
    end

    %% =========================
    %% PRESENTACIÓN
    %% =========================

    subgraph PRESENTACION["CAPA DE PRESENTACIÓN"]
        Web["Aplicación Web"]
    end

    %% =========================
    %% API
    %% =========================

    subgraph API["CAPA DE SERVICIOS / API"]
        Rest["API REST"]
    end

    %% =========================
    %% LÓGICA DE NEGOCIO
    %% =========================

    subgraph NEGOCIO["CAPA DE LÓGICA DE NEGOCIO"]
        direction LR

        Usuarios["Gestión de Usuarios"]
        Sellers["Gestión de Sellers"]
        Catalogo["Catálogo de Productos"]
        Carrito["Carrito de Compras"]
        Pedidos["Gestión de Pedidos"]
    end

    %% =========================
    %% DATOS
    %% =========================

    subgraph DATOS["CAPA DE DATOS"]
        BD[("Base de Datos")]
    end

    %% =========================
    %% SISTEMAS EXTERNOS
    %% =========================

    subgraph EXTERNOS["SISTEMAS EXTERNOS"]
        direction LR

        Pago["Pasarela de Pago"]
        ERP["ERP"]
        Envio["Servicio de Envío"]
        Facturacion["Servicio de Facturación"]
    end

    %% =========================
    %% FLUJO PRINCIPAL
    %% =========================

    Cliente --> Web
    Seller --> Web
    Admin --> Web

    Web --> Rest

    Rest --> Usuarios
    Rest --> Sellers
    Rest --> Catalogo
    Rest --> Carrito
    Rest --> Pedidos

    Usuarios --> BD
    Sellers --> BD
    Catalogo --> BD
    Carrito --> BD
    Pedidos --> BD

    %% =========================
    %% INTEGRACIONES EXTERNAS
    %% =========================

    Pedidos -->|"Procesar pago"| Pago
    Pedidos -->|"Gestionar entrega"| Envio
    Pedidos -->|"Generar comprobante"| Facturacion

    Catalogo -->|"Consultar productos y stock"| ERP
    Pedidos -->|"Actualizar stock"| ERP

    %% =========================
    %% ESTILOS
    %% =========================

    classDef actor fill:#1f2937,stroke:#ffffff,color:#ffffff,stroke-width:1px;
    classDef presentation fill:#1e3a5f,stroke:#ffffff,color:#ffffff,stroke-width:1px;
    classDef api fill:#374151,stroke:#ffffff,color:#ffffff,stroke-width:1px;
    classDef business fill:#264653,stroke:#ffffff,color:#ffffff,stroke-width:1px;
    classDef data fill:#3f3f46,stroke:#ffffff,color:#ffffff,stroke-width:1px;
    classDef external fill:#4b5563,stroke:#ffffff,color:#ffffff,stroke-width:1px;

    class Cliente,Seller,Admin actor;
    class Web presentation;
    class Rest api;
    class Usuarios,Sellers,Catalogo,Carrito,Pedidos business;
    class BD data;
    class Pago,ERP,Envio,Facturacion external;