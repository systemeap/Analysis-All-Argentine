# Analysis-All-Argentina
![Logo del proyecto](Assets/All_Argentina.jpg)

Este proyecto ha sido desarrollado para ALL ARGENTINA, una empresa que brinda servicios de análisis de datos a nivel nacional. Me contrato a mi como DATA ANALITICS. El objetivo principal es analizar datos de ENACOM (Ente Nacional de Comunicaciones), enfocados en los servicios de internet en Argentina. El análisis de datos busca identificar patrones clave de conectividad y calidad del servicio, con el fin de proporcionar información valiosa que pueda apoyar en la toma de decisiones estratégicas para mejorar la infraestructura de telecomunicaciones. con respecto a la provincia que lo solicite.

# APERTURA
Las telecomunicaciones en Argentina han experimentado una transformación significativa en las últimas décadas, impulsadas por el avance tecnológico y la creciente demanda de conectividad en un mundo cada vez más digitalizado. Desde la expansión de las redes de banda ancha y la adopción masiva de dispositivos móviles, hasta la implementación de tecnologías emergentes como la fibra óptica y el 5G, el sector se ha convertido en un pilar fundamental para el desarrollo económico y social del país.

En este contexto, la industria de las telecomunicaciones enfrenta tanto oportunidades como desafíos. La necesidad de garantizar el acceso a servicios de calidad en todas las regiones, incluidas las más remotas, sigue siendo un objetivo primordial. Al mismo tiempo, la pandemia de COVID-19 ha evidenciado la importancia crítica de la infraestructura de telecomunicaciones para asegurar la continuidad de actividades esenciales como la educación, el trabajo remoto y la atención médica a distancia.

Este informe tiene como objetivo proporcionar una visión integral del estado actual de las telecomunicaciones en Argentina. Se analizarán las principales tendencias del mercado, la evolución de la infraestructura y los servicios, así como los desafíos regulatorios y tecnológicos que enfrenta el sector. Además, se explorarán las expectativas futuras en términos de innovación y expansión de la red, con el fin de entender el papel que jugará este sector en la transformación digital del país.

# OBJETIVOS
<li>Realizar un estudio general sobre los datos brindados por la empresa ALL ARGENTINE, relacionados a los distintas tecnicas de comunicacion en ARGENTINA, centrandose en la INTERNET y sus distintas tecnologias</li>
<li>Aplicar o crear indicadores claves de rendimientos (KPIs), para medir la eficacia e eficiencia de los servicios.</li>
<li>Analizar la calidad del servicio de internet (velocidad, estabilidad, latencia) y telefonía móvil (cobertura, calidad de llamadas) en distintas regiones del país e
identificar áreas con problemas recurrentes de conectividad y proponer posibles soluciones.</li>
<li>Crear e implementar un DASHBOARD, que muestre en forma dinamica, los datos importantes estudiados, para la toma de desiciones.</li>

# ESTUDIOS
Para dicho proyecto, se recibe como datos primarios los brindados por la empresa ALL ARGENTINE, https://indicadores.enacom.gob.ar/datos-abiertos, viendo que los mismos estaban formados por archivos en formato xlsx (excel), algunos con pocas paginas y otros como "internet", con 15 paginas, se elige como tipo de archivo el formato xlsx.
Archivos Utilizados
1) Internet.xlsx - Este archivo contiene 15 hojas, cada una representando diferentes aspectos de la conectividad en Argentina. Se analizaron y graficaron 7 hojas específicas que ofrecen una visión integral sobre la calidad y el acceso a internet:
Velocidad sin rangos: Información cruda de las velocidades de internet por provincia y trimestre.

Accesos tecnología localidad: Desglose de accesos a internet por tipo de tecnología (ADSL, Cablemódem, Fibra Óptica, etc.) a nivel de localidad.

Velocidad % por provincia: Distribución porcentual de las velocidades de conexión en cada provincia.

Accesos por tecnología: Número de accesos por cada tipo de tecnología a nivel nacional.

Penetración población: Penetración del servicio de internet en la población general.

Penetración hogares: Nivel de penetración del servicio de internet en los hogares.

Accesos por velocidad: Desglose de los accesos según el rango de velocidad contratado.

2) Archivo mapa_conectividad.xlsx
Contiene datos geoespaciales que relacionan la ubicación geográfica con la conectividad, permitiendo un análisis territorial del acceso a internet:

Provincia: Nombre de la provincia en Argentina.

Localidad: Localidad correspondiente a cada registro.

Partido: División administrativa.

Tecnologias de conectividad: Como ADSL, Fibra Optica, Cablemodem, Satelital, 4G, 5G, etc.

Latitud y Longitud: Coordenadas geográficas que permiten la visualización espacial de la conectividad. 

<b>Primero</b> se hizo uso del proceso de ETL (Extraccion, Transformacion y Limpieza), cuidando de preservar la estructura original para asegurar la integridad en el análisis posterior, una vez analizados, limpieza de valores nulos, se hicieron transformaciones de tipos de datos, normalizaciones de las columnas y de las filas y se validaron los datos para garantizar su calidad, eliminando duplicados, gestionando valores faltantes y corrigiendo inconsistencias.

<b>En segundo lugar</b> Se utilizo la tecnica del (EDA - Analisis Exploratorio de los Datos). Se exploraron y se hicieron graficas, para ver valores atipicos o fuera de rango, analisis atravez de graficos 
que me muestran las tendencias y las bajas en los usos de las distintas tecnologias y velocidades.

# DETALLES MAS RELEVANTES
Segmentación Geográfica: Los datos fueron organizados por provincias, localidades y partidos para realizar un análisis territorial detallado.

Comparación de Tecnologías: Se evaluaron las diferencias en la penetración de tecnologías como Fibra Óptica, ADSL y Satelital en diferentes regiones.

Análisis Temporal: Se observó la evolución de los accesos a internet por tecnología y velocidad durante varios trimestres.

Detección de Disparidades: Se identificaron las áreas más y menos conectadas, con un enfoque en zonas rurales y provincias con menor infraestructura tecnológica.

Se generaron múltiples gráficos para respaldar el análisis:
Gráfico de barras: Comparación de accesos a internet por tecnología en las diferentes provincias.
Graficos de barras apiladas: 
GRaficos de areas y areas apiladas:
Mapas de calor: Representación geoespacial de las velocidades de internet en cada región.
Gráfico de líneas: Evolución temporal de la penetración de internet en la población y los hogares.
Gráficos circulares (pastel): Distribución porcentual de los accesos por velocidad y tecnología.
# KPIs ANALIZADOS
Para dicho estudio se nos solicito el sigueinte KPIs
1) Aumentar en un 2% el acceso al servicio de internet para el próximo trimestre, cada 100 hogares, por provincia. La fórmula es la siguiente:
 KPI = ((Nuevoacceso - AccesoActual / AccesoActual)*100)

2) Penetracion de internet en un 2% por hogares. Este KPI mide el porcentaje de hogares que tienen acceso a Internet en comparación con el total de hogares de la provincia.
O sea la meta objetiva es incrementar en un 2%.
PorcentajePenetracion = AVERAGE([Acceso por cada 100 hogares])   # PorcetajePenetracion o Total de hogares por prov.
TotalAcceso = ((TotalHogaresProv*100)/Acceso cada 100 hogares).

3) Crecimiento anual del acceso a Internet. Este KPIs mide el porcentaje de crecimiento en el acceso a Internet en cada provincia comparando el trimestre actual con el mismo trimestre del año anterior.

Crea una medida para calcular el acceso en el trimestre del año pasado (asegúrate de tener el dato disponible):    
Acceso_AñoAnterior = CALCULATE([AccesoActual], SAMEPERIODLASTYEAR(Fecha[Fecha]))    
Donde acceso actual, ya lo tenemos de la tabla, penetraccion por hogares, es la llamada "Acceso por cada 100 hogares".
KPI_CrecimientoAnual = (([AccesoActual] - [Acceso_AñoAnterior]) / [Acceso_AñoAnterior]) * 100




# DASHBOARD 
Link de donde se encuentra el DASHBOARD. 
Proyecto_All Argentina.pbix

# INTERPRETACION DE LOS RESULTADOS
<b>Velocidad de Conexión</b>
Las provincias con mayores accesos a tecnologías avanzadas, como la Fibra Óptica, presentan mejores velocidades de conexión. Sin embargo, aún persisten áreas rurales donde la penetración de internet es baja o inexistente.

<b>Acceso por Tecnología</b>
El ADSL sigue siendo la tecnología más utilizada a nivel nacional, aunque hay un crecimiento considerable en la adopción de Cablemódem y Fibra Óptica en zonas urbanas. En las áreas más aisladas, la tecnología satelital es la única opción viable.

<b>Penetración en Hogares y Población</b>
Se identificaron provincias con tasas de penetración en hogares superiores al 80%, mientras que en otras regiones, esta cifra no supera el 40%, destacando una fuerte brecha digital.

# CONCLUSIONES Y RECOMENDACIONES
<b>Conclusiones</b>
Existe una notable desigualdad en el acceso a internet entre las distintas provincias, especialmente en relación con la velocidad y el tipo de tecnología disponible.
Las provincias con mayor acceso a tecnologías avanzadas (Fibra Óptica y Cablemódem) tienden a concentrarse en zonas urbanas y de mayor desarrollo económico.
Las regiones rurales requieren mayor inversión en infraestructura para mejorar la conectividad, lo que podría cerrar la brecha digital y aumentar las oportunidades económicas.

<b>Recomendaciones</b>
Inversión en Infraestructura: Es crucial expandir el acceso a tecnologías de alta velocidad, como la Fibra Óptica, en zonas rurales y provincias menos conectadas.
Estrategias de Inclusión Digital: Implementar políticas de subsidios o incentivos para llevar internet a hogares en áreas de baja penetración.
Monitoreo y Actualización de Datos: Continuar monitoreando la evolución del acceso a internet y actualizar los datos regularmente para tomar decisiones basadas en evidencia.
Incorporación de Datos Demográficos: Propon que se integre el análisis con datos demográficos adicionales, como niveles de ingreso por provincia o partido, que podrían proporcionar una visión más completa sobre la penetración tecnológica.

<b>Recomendaciones en relacion a la presentacion de los informes</b>
Integración con APIs Externas: Si los usuarios desean obtener datos más recientes o actualizados, puedes recomendar la integración con APIs públicas de datos abiertos. Por ejemplo, se podría sugerir el uso de la API del Indec o la API de ENACOM (si estuviera disponible) para enriquecer los datos.
Análisis Espacial Más Completo: Si se trabaja con datos geográficos, podrías recomendar utilizar librerías como <b>Folium</b> para generar mapas interactivos. Esto puede ser útil para la parte de conectividad por provincia o localidad.

# 


# CONTACTO Y LINKS 
Medios de contactos
Email: systemeap@gmail.com
