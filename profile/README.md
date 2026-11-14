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

## Seguimiento de Cotización UVA: Inteligencia Financiera con Datos Oficiales

### El Desafío de Negocio
En el mercado argentino, miles de contratos comerciales, alquileres, presupuestos de construcción y créditos se ajustan por Unidad de Valor Adquisitivo (UVA). Consultar manualmente las series históricas del Banco Central o calcular variaciones interanuales y acumuladas en hojas de cálculo genera demoras y errores al momento de actualizar valores o proyectar costos.

### La Solución de Prisma DS
Diseñamos un tablero financiero interactivo conectado a los registros oficiales del Banco Central de la República Argentina (BCRA). Permite consultar de forma inmediata la evolución histórica desde 2016 hasta la actualidad, automatizando el cálculo de indicadores clave para la toma de decisiones financieras.

### Impacto y Funcionalidades Clave
* **Consulta histórica instantánea:** Navegación ágil por año, mes y día exacto para liquidaciones o actualizaciones contractuales sin depender de búsquedas manuales.
* **Análisis de variaciones automatizado:** Cálculo dinámico de variación mensual, interanual y acumulada mediante inteligencia de tiempo para evaluar el impacto real de la inflación en los costos o ingresos.
* **Experiencia de usuario intuitiva:** Títulos dinámicos que se adaptan automáticamente a los filtros seleccionados por el usuario, facilitando la lectura ejecutiva y la exportación de reportes.

![Tablero de Cotización UVA ](images/tablero.png)

### Arquitectura y Stack Tecnológico
* **Extracción y Transformación (ETL):** Power Query para la limpieza, estructuración y actualización de las series oficiales del BCRA.
* **Modelado y Analítica:** Power BI y DAX avanzado (creación de tabla calendario dedicada y medidas de inteligencia de tiempo).

🔗 **[Explorar el Repositorio]**

## 📱 Licitaciones del Día: Inteligencia Comercial y Alertas Automatizadas de Compras Públicas

### El Desafío de Negocio
Las empresas proveedoras del Estado y los socios de cámaras empresarias suelen recibir listados masivos y sin filtrar de las contrataciones públicas (como los del portal COMPR.AR). Revisar cientos de registros diarios de forma manual consume horas valiosas, hace que se pierdan oportunidades de negocio por falta de tiempo y expone a los equipos comerciales a no enterarse si una licitación de su interés sufrió una prórroga o cambio de fecha.

### La Solución de Prisma DS
Diseñamos un sistema integral de ingesta, clasificación inteligente y notificación móvil. La plataforma procesa diariamente los procesos de compra pública, los categoriza automáticamente por rubro y tipo (bien o servicio) y envía alertas personalizadas al celular de cada empresa únicamente sobre las licitaciones relevantes para su negocio.

![Nuevas oportunidades publicadas ](images/02_nuevos.png)

### Impacto y Funcionalidades Clave
* **Filtrado automático por rubro:** Cada empresa visualiza exclusivamente las oportunidades alineadas a su actividad comercial, eliminando el ruido operativo de revisar planillas interminables.
* **Alertas de vencimiento y prórrogas:** Monitoreo continuo de estados para avisar proactivamente qué licitaciones están próximas a abrir y notificar al instante si un proceso guardado como favorito cambia de fecha.
* **Consultas en lenguaje natural:** Integración opcional con modelos de lenguaje (IA) que permite a los usuarios consultar oportunidades en castellano cotidiano sin necesidad de filtros complejos.
* **Arquitectura escalable:** Pensado tanto para empresas individuales como para cámaras empresarias que desean ofrecer un servicio de valor agregado a sus socios.

### Arquitectura y Stack Tecnológico
* **Ingeniería de Datos y Backend:** Python, Pandas, PostgreSQL y SQLAlchemy para la extracción, limpieza, clasificación automatizada y almacenamiento estructurado de procesos.
* **Analítica y Prototipo Móvil:** HTML, JavaScript, Streamlit y Altair para la visualización de datos y la experiencia de usuario mobile-first.
* **Inteligencia Artificial:** Integración vía API de procesamiento de lenguaje natural para búsquedas conversacionales.

🔒 *Nota de confidencialidad: Este repositorio funciona como vitrina de arquitectura y producto. El código fuente completo se mantiene en un repositorio privado de Prisma DS.*


