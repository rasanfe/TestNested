# TestNested — Importar JSON en un Nested Report (que no Composite) 📰🧩

![PowerBuilder](https://img.shields.io/badge/PowerBuilder-2022%20R3-2D6CDF?style=flat-square)
![DataWindow](https://img.shields.io/badge/DataWindow-Nested%20Report-009688?style=flat-square)
![JSON](https://img.shields.io/badge/import-JSON-F0DB4F?style=flat-square&logo=json&logoColor=black)
![Blog](https://img.shields.io/badge/blog-rsrsystem-FF5722?style=flat-square&logo=blogger&logoColor=white)

## 📋 ¿Qué es esto?

Una prueba de concentración pura: **importar JSON dentro de un Nested Report** de PowerBuilder…
**y que no sea un Composite.** Que parece lo mismo, pero no lo es, y ahí está la gracia.

- Un **Composite** es un DataWindow que "pega" varios informes independientes.
- Un **Nested Report** es un informe **incrustado dentro de otro** (típicamente cabecera + detalle
  anidado), que comparte el flujo de datos del DataWindow padre.

El reto: cuando los datos no vienen de la base de datos sino de un **JSON** (como pasa cuando tiras
de una API REST, justo lo que monto en los ejemplos `Reports_*`), hay que conseguir que **el padre
y el informe anidado se rellenen bien** con `ImportString` / `ImportJSON`. Eso es lo que aquí
compruebo.

## ✨ Qué encontraréis

- Un DataWindow **padre con un Nested Report** dentro.
- Los datos de ejemplo en **JSON** listos para importar:
  - `data.json` → el grueso de los datos del informe.
  - `nested.json` → el trocito que alimenta la parte anidada (la lista de empresas de la demo).
- El proyecto **en modo solución** (`reports.pbsln`, `reportsapi.pbl`) para que lo abráis,
  compiléis y juguéis con ello.

## 🛠️ Requisitos

- **PowerBuilder 2022 R3** o superior (el ejemplo se ha recompilado también con runtime 2025).

## ▶️ Cómo probarlo

1. Clona el repo **en modo solución** y abre `reports.pbsln` en PowerBuilder.
2. Ejecuta la app: carga el JSON (`data.json` / `nested.json`) e impórtalo al DataWindow.
3. Fíjate en cómo el **Nested Report** se rellena junto con el padre a partir del JSON, sin pasar
   por la base de datos.

## 🔗 Repo PowerBuilder

<https://github.com/rasanfe/TestNested>

---

> ¡Nos vemos en el próximo artículo! Y recuerda: en PowerBuilder, los límites solo están en nuestra imaginación. 🚀

📨 **Blog:** <https://rsrsystem.blogspot.com/>
