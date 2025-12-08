# Proyecto Urban Grocers 
📖 Descripción del Proyecto
Urban Grocers es un proyecto de testing de API desarrollado durante el Sprint 4 del bootcamp de QA en TripleTen. El objetivo principal fue probar las nuevas funcionalidades del back-end de una aplicación de delivery de comestibles, enfocándose en la gestión de kits de productos y servicios de entrega.

🎯 Objetivos del Proyecto
Analizar requisitos de nuevas funcionalidades del back-end
Diseñar casos de prueba para endpoints específicos de API
Ejecutar pruebas de API utilizando Postman
Documentar defectos encontrados en JIRA
Validar respuestas y códigos de estado HTTP
🔧 Funcionalidades Probadas
### 1. Gestión de Kits de Productos
- Endpoint: POST /api/v1/kits/{id}/products
- Funcionalidad: Agregar comestibles a un kit existente
- Validaciones principales:
  - Límite máximo de 30 productos por kit
  - Respuesta 400 Bad Request cuando se excede el límite
  - Estructura correcta del JSON de respuesta

### 2. Servicios de Entrega "Order and Go"
- Endpoint: POST /order-and-go/v1/delivery
- Funcionalidad: Verificar disponibilidad y calcular costo de entrega
- Validaciones principales:
  - Disponibilidad del servicio por ubicación
  - Cálculo correcto de precios de entrega
  - Manejo de errores para ubicaciones no válidas

🛠️ Herramientas Utilizadas
Herramienta	Propósito
Postman	Ejecución de pruebas de API y validación de endpoints
JIRA	Gestión y reporte de defectos encontrados
ApiDoc	Consulta de documentación técnica de la API
Google Sheets	Documentación de casos de prueba y resultados
JSON	Formato de datos para requests y responses
📊 Metodología de Testing
### Técnicas Aplicadas:
- Análisis de clases de equivalencia para parámetros de entrada
- Testing de valores límite (especialmente para el límite de 30 productos)
- Pruebas positivas y negativas para cada endpoint
- Validación de códigos de estado HTTP (200, 400, 404, etc.)
- Verificación de estructura JSON en respuestas

### Tipos de Pruebas Realizadas:
- ✅ Pruebas funcionales de endpoints
- ✅ Pruebas de validación de parámetros
- ✅ Pruebas de límites y restricciones
- ✅ Pruebas de manejo de errores
- ✅ Pruebas de formato de respuestas

📋 Casos de Prueba Principales
### Kit de Productos:
1. Agregar productos válidos a un kit existente
2. Exceder el límite de 30 productos y validar error 400
3. Agregar productos a kit inexistente y validar error 404
4. Enviar formato JSON inválido y validar manejo de
