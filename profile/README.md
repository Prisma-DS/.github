# Quienes Somos
En Prisma DS ayudamos a las empresas a tomar decisiones con información clara y confiable. 

Somos una consultoría de datos especializada en reportes, modelado y automatización con Power BI, apoyada en bases de datos SQL (PostgreSQL, SQLServer, Oracle) y Python.

# Qué hacemos
- Dashboards e informes en Power BI a medida
- Integración y organización de datos desde bases de datos, Excel y otras fuentes
- Automatización de reportes y pipelines de datos
- Capacitación para equipos que quieren usar sus propios reportes

# Proyectos

## Informe de gestión de ventas (Power BI)

### El Desafío de Negocio
Las empresas con múltiples puntos de venta suelen acumular años de registros históricos en archivos sueltos (CSV/Excel) sin poder cruzarlos. Esto impide detectar qué sucursales son realmente rentables, qué productos inmovilizan capital y cómo evolucionan los hábitos de pago de los clientes.

### La Solución de Prisma DS
Diseñamos un ecosistema de análisis de datos de extremo a extremo que consolida una década de operaciones en un tablero ejecutivo interactivo. Permite a la gerencia tomar decisiones basadas en evidencia en cuestión de segundos.

### Impacto y Hallazgos Clave (Resultados)

- **Detección de concentración de riesgo:** Se identificó que una sola sucursal concentra el 44,45% de la facturación total, permitiendo diseñar estrategias para equilibrar el rendimiento del resto de las sedes.
- **Optimización de inventario:** Se aislaron los productos de baja rotación para sugerir su discontinuación y liberar capital de trabajo.
- **Estrategia financiera:** El análisis de medios de pago evidenció la necesidad de impulsar canales electrónicos para agilizar el flujo de caja.

![Total de ventas](images/00-total-ventas.png)

### Arquitectura y Stack Tecnológico

- **ETL y Análisis Exploratorio:** Python (Pandas, Matplotlib, Seaborn) para la limpieza, unificación y validación de registros históricos.
- **Modelado y Optimización:** Power BI y DAX Studio para la creación de métricas de negocio complejas y tiempos de respuesta rápidos.


## Control de Monotributo: Analítica Predictiva y Automatización para Estudios Contables

### El Desafío de Negocio
Los estudios contables suelen gestionar decenas o cientos de clientes monotributistas revisando manualmente planillas descargadas de ARCA. Este proceso consume horas administrativas críticas y expone a los clientes a recategorizaciones de oficio o exclusiones inesperadas del régimen por superar los topes de facturación.

### La Solución de Prisma DS
Desarrollamos una aplicación web interactiva que automatiza el control de facturación de múltiples clientes en segundos. Procesa directamente los archivos CSV de *Mis Comprobantes* (ARCA), aplica las reglas fiscales vigentes y proyecta el comportamiento futuro de cada contribuyente para anticiparse a los vencimientos.

![Resumen de clientes del tablero de Monotributo](images/captura-resumen.png)

### Impacto y Funcionalidades Clave
* **Ahorro de tiempo operativo:** Procesamiento masivo y simultáneo de comprobantes (restando notas de crédito y excluyendo recibos automáticamente) sin almacenamiento en servidor para garantizar la privacidad de los datos.
* **Alertas tempranas con semáforo:** Clasificación automática de clientes según el porcentaje de consumo de su tope anual (*En rango, Atención, Alerta, Superado*).
* **Proyección inteligente:** Cálculo de ventana móvil a 12 meses que estima exactamente en qué mes el cliente superaría su categoría actual según su ritmo de facturación reciente (3, 6 o 12 meses) y cuánto tiene disponible para facturar sin pasarse.
* **Reportes listos para gestión:** Sugerencia de categoría correspondiente y exportación inmediata del resumen ejecutivo a CSV.

### Arquitectura y Stack Tecnológico
* **Procesamiento y Lógica de Negocio:** Python y Pandas con arquitectura modular separada de la interfaz y cubierta con pruebas automatizadas (`pytest`).
* **Interfaz y Visualización:** Streamlit y Plotly para una experiencia de usuario ágil, interactiva y sin necesidad de instalación local para el cliente final.

🔗 **[Explorar el Repositorio y Código](https://github.com/jesitm/tablero-monotributo-streamlit)**

