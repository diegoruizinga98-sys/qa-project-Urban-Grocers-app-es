# 🛒 Urban Grocers — API Testing & Automation

Proyecto de testing de API REST para **Urban Grocers**, una plataforma de delivery de comestibles que expone endpoints para la gestión de usuarios, kits de productos y carritos de compra.

El proyecto abarca dos fases: validación manual exhaustiva con Postman para asegurar la estabilidad de los endpoints antes del go-live, y automatización con Python/Pytest para reducir el tiempo de regresión en la validación de datos de entrada.

**Stack:** Python 3.11 · Pytest · Requests · Postman · API REST · Parametrized Testing

---

## 📋 Contexto del proyecto

**Urban Grocers** es una aplicación de delivery que permite a usuarios crear cuentas, armar kits de productos y realizar pedidos. Su API REST expone endpoints críticos que deben validarse ante distintos tipos de entrada: valores límite, datos inválidos, campos faltantes y tipos incorrectos.

La fase de automatización se centró en el endpoint de creación de kits, validando el campo `name` con un conjunto parametrizado de 9 casos de prueba que cubre análisis de valores límite, clases de equivalencia y escenarios negativos.

**Resultado clave:** ⬇️ **90%+ de reducción en tiempo de ejecución** de pruebas de API vs. ejecución manual

---

## 🧪 Cobertura de pruebas

### 📬 Validación manual con Postman

| Métrica | Valor |
|---|---|
| Total de solicitudes API probadas | 50 |
| Tasa de aprobación antes del go-live | **100%** |
| Casos de prueba funcionales | 71 |
| Casos aprobados | 46 |
| Casos fallidos (defectos detectados) | 25 |
| Tasa de defectos | **35%** |

### 🤖 Automatización Python/Pytest

| Métrica | Valor |
|---|---|
| Casos automatizados | 9 (parametrizados) |
| Campo validado | name (creación de kits) |
| Tipos de prueba | Fronteras, valores inválidos, positivos |
| Reducción de tiempo de ejecución | **+90%** vs. manual |

---

## 🏗️ Estructura del proyecto

| Archivo | Responsabilidad |
|---|---|
| create_kit_name_kit_test.py | Suite parametrizada de pruebas del campo name |
| configuration.py | URL base y endpoints de la API |
| data.py | Datos de prueba por caso |
| sender_stand_methods.py | Métodos auxiliares para llamadas HTTP |

---

## ✅ Casos de prueba automatizados (campo name)

| # | Caso | Tipo | Resultado esperado |
|---|------|------|-------------------|
| 1 | 1 carácter | Frontera inferior | ✅ Aprobado |
| 2 | 511 caracteres | Frontera superior | ✅ Aprobado |
| 3 | 512 caracteres | Fuera de frontera | ❌ Rechazado |
| 4 | String vacío | Inválido | ❌ Rechazado |
| 5 | Solo espacios | Inválido | ❌ Rechazado |
| 6 | Caracteres especiales | Válido | ✅ Aprobado |
| 7 | Números en string | Válido | ✅ Aprobado |
| 8 | Campo ausente | Inválido | ❌ Rechazado |
| 9 | Tipo incorrecto (int) | Inválido | ❌ Rechazado |

---

## 💻 Tecnologías utilizadas

| Herramienta | Uso |
|---|---|
| **Python 3.11** | Lenguaje principal |
| **Pytest** | Framework + parametrización de pruebas |
| **Requests** | Cliente HTTP para llamadas a la API |
| **Postman** | Validación manual de endpoints de la API |
| **API REST** | Protocolo de comunicación probado |

---

## 🚀 Cómo ejecutar

1. Clonar el repositorio: git clone https://github.com/diegoruizinga98-sys/qa-project-Urban-Grocers-app-es.git
2. Instalar dependencias: pip install pytest requests
3. Ejecutar la suite: pytest create_kit_name_kit_test.py -v

---

## 👤 Autor

**Diego Ruiz Inga** · QA Automation Engineer  
🌐 [Portafolio](https://diegoruizinga98-sys.github.io/diego-ruiz-inga-qa/) · [LinkedIn](https://www.linkedin.com/in/diego-ruiz-inga/) · 📧 diegori466@gmail.com
