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

## Equipo

| Integrante | Responsabilidad |
| :--- | :--- |
| BACA CALSIN, LEONARDO JUAN JOSE | Scrum Master, aseguramiento de la calidad y seguimiento del trabajo |
| CHIPANA JERONIMO, GERMAN ARTURO | Arquitectura de software, diccionario de datos y entorno técnico |
| MEJIA RONDAN, GIOVANNI PATRICK | Backend, diseño y revisión técnica de la base de datos |
| PALMA APAZA, SANTIAGO ENRIQUE | Product Owner, historias de usuario y frontend |

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

---

## Flujo de Colaboración

1. Seleccionar un issue y confirmar quién lo realizará y quién lo revisará.
2. Crear la rama de trabajo desde la versión actualizada de main.
3. Registrar cambios concretos mediante commits descriptivos.
4. Abrir un Pull Request hacia main, indicando el issue relacionado, los cambios y cómo se comprobaron.
5. Mover la tarea a En revisión y notificar al revisor con el enlace del Pull Request.
6. Atender las observaciones en la misma rama y agregar los commits de corrección.
7. Incorporar los cambios revisados a main y actualizar el estado de la tarea.

Las tareas técnicas se cierran al completar y revisar su entrega. Las historias de usuario se cierran cuando sus criterios de aceptación estén comprobados y el Product Owner acepte el resultado.

---

## Ramas

| Actividad | Rama sugerida |
| :--- | :--- |
| Preparación del repositorio | `chore/estructura-inicial` |
| Arquitectura y guía | `docs/arquitectura` |
| Base de datos | `feat/base-datos` |
| Backend | `feat/backend` |
| Frontend | `feat/frontend` |
| Pruebas | `test/flujo-principal` |

---

## Commits

Cada commit describe un cambio concreto según la convención estándar. Ejemplos:

* `docs: definir el flujo del programa y alcance de distribucion`
* `feat: crear las tablas de despachos y guias de remision`
* `feat: conectar la interfaz con los servicios de despacho`
* `test: comprobar la generacion de guia electronica y transicion de estados`
* `fix: validar el formato de placa y licencia de conducir antes de registrar`
