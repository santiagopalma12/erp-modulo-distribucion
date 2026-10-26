# ERP FSI — Módulo de Distribución

Proyecto académico de la Escuela Profesional de Ingeniería de Sistemas de la Universidad Nacional de San Agustín de Arequipa, desarrollado para el curso de Fundamentos de Sistemas de Información.

Este repositorio reúne el trabajo del módulo de Distribución, perteneciente a la Tribu de Ingresos (Tribu 2 · Equipo 4). Su código se integrará posteriormente al repositorio común del ERP institucional, según la coordinación entre equipos.

---

## Objetivo

El objetivo del módulo de Distribución es planificar, programar, monitorear y liquidar la entrega física de bienes a los clientes a partir de órdenes de venta confirmadas, así como controlar los traslados internos de mercadería entre sedes y almacenes de la empresa.

Asimismo, el módulo asegura el cumplimiento de las normativas tributarias peruanas mediante la emisión y control de la Guía de Remisión Electrónica Remitente (GRE), conforme a las resoluciones de la Superintendencia Nacional de Aduanas y de Administración Tributaria (SUNAT), específicamente la Resolución de Superintendencia N.° 123-2022/SUNAT y sus disposiciones conexas.

---

## Primera Implementación

El bloque 3 contempla el diseño de la base de datos y un programa sencillo para comprobar el siguiente recorrido:

1. Registrar la orden de despacho a partir de una orden de venta y generar la Guía de Remisión Electrónica preliminar.
2. Consultar las órdenes de despacho programadas, transportistas asignados y estados en ruta.
3. Registrar la entrega conforme al cliente y actualizar el estado a entregado o registrar incidencias.

Las tecnologías y las instrucciones de ejecución se definirán en la guía de implementación.

---

## Organización y Estructura

El proyecto se organizará siguiendo los principios de Clean Architecture:

```text
/
├── backend/
├── frontend/
├── database/
├── docs/
└── tests/
```

---

## Propuesta de Tecnologías

Para la coordinación y votación inter-tribus, el equipo propone el uso del siguiente stack tecnológico:

* Frontend: React, TypeScript, Vite, Tailwind CSS
* Backend: Python + FastAPI (REST, JSON)
* Base de Datos: PostgreSQL (Relacional + JSONB, Esquema modular `distribucion`)
* Infraestructura: Docker y Docker Compose
* Pruebas (QA): pytest, HTTPX

---

## Historias de Usuario y Tareas

Las historias de usuario se registran como issues con la etiqueta `historia-usuario`:

* HU-01: Registrar una orden de despacho y generar Guía de Remisión Electrónica.
* HU-02: Consultar programación de entregas y estados en tránsito.
* HU-03: Registrar entrega en destino y actualizar estado.

Las actividades de arquitectura, scripts de base de datos, backend, frontend y pruebas se registran con la etiqueta `tarea-tecnica` y se relacionan con las historias correspondientes.

El tablero de trabajo organiza las tareas en los siguientes estados: Pendiente → En proceso → En revisión → Terminado.
