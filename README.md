🌲 SAR INSIGHTS: Detección de Degradación Forestal Sutil (Amazonía)
Hackathon: 14 Horas de Ejecución Impecable
🌐 PLATAFORMA MVP (Demo): https://www.sar-insights.lat
🎯 EL PROBLEMA Y LA SOLUCIÓN
| Área | Descripción |
|---|---|
| Problema Central | La degradación forestal sutil y la tala selectiva en Madre de Dios, Perú, ocultas por la nubosidad constante. |
| Solución | Sistema de Alerta Temprana basado en la fusión de Radar (Sentinel-1 SAR) y Random Forest para un monitoreo 24/7. |
| Entregable | Plataforma Web (MVP) que visualiza el Mapa de Degradación Sutil y Pitch Deck de alto impacto. |
🛠️ STACK TÉCNICO Y METODOLOGÍA CLAVE
Este proyecto depende de una ejecución secuencial y paralela de tres componentes críticos.
1. Datos Base
 * Fuente: Serie temporal de Sentinel-1 (SLC).
 * Polarizaciones: VV y VH.
 * Plataforma de Procesamiento: Google Earth Engine (GEE).
2. Detección de Cambios (Métrica SAR)
Utilizamos el algoritmo Cumulative Sum (CuSum) sobre las series de tiempo SAR para generar una métrica de cambio robusta, $$Rsum_{max}$$.

$$ \text{Rsum}_{\text{max}} = \max\left(\sum_{t=1}^{T} (S_t - \mu)\right) $$

 * Responsable: Irving (Ing. de Datos).
 * Función: Pre-procesamiento rápido para identificar áreas de potencial cambio.
3. Modelo de Clasificación (Random Forest)
Un modelo de Red Neuronal Convolucional (CNN) para la segmentación semántica fina.
 * Arquitectura: Random Forest.
 * Objetivo: Mapear las 3 clases: (1) Bosque Intacto, (2) Bosque Degradado (Sutil), (3) Deforestación/No Bosque.
 * Métrica de Éxito: IoU para la clase 'Bosque Degradado'.
 * Responsable: Benjamín (Líder/Arquitecto IA).
⚙️ FLUJO DE TRABAJO (PIPELINE DE 14 HORAS).

El trabajo se organiza en 3 Fases con paralelización obligatoria en la Fase 2.

| Fase | Tarea Crítica | Rol Principal | Duración Est. |
|---|---|---|---|
| 1. Cimientos y Datos (0-3h) | Pipeline de Datos SAR en GEE (Acceso, Pre-procesamiento, AOI). | Irving / Cristhian | 3h |
| 2. Modelado y Desarrollo (3-9h) | Modelado CuSum (Irving) + Modelado U-TAE (Benjamín). Esqueleto App (Diego). | Paralelo: Benjamín, Irving, Diego | 6h |
| 3. Integración y Pitch (9-14h) | Integración de GeoTIFFs (Mapas) a la App. Finalización y Ensayos del Pitch. | Integración: Benjamín, Irwin, Diego. Pitch: Edú | 5h |
Puntos de Contacto Críticos:
 * Hora 3: Entrega del dataset limpio y la AOI validada (Cristhian a Benjamín/Irving).
 * Hora 9: Generación del Mapa de Degradación Final (Benjamín/Irving) e Inicio de Integración (Diego).

🧑‍💻 CONTACTOS RÁPIDOS (Roles de Ejecución)

| Nombre | Rol Asignado (Hackathon) | Preguntar por... |
|---|---|---|
| Benjamín S. | Líder/Arquitecto IA | Hyperparámetros U-TAE, Estrategia General. |
| Irving | Ing. de Datos/CuSum | Series temporales SAR, Salida de $$Rsum_{max}$$. |
| Cristhian F. | Experto GIS/Ground Truth | Validación de datos, Geometrías (AOI), Calibración. |
| Diego O. | Ing. Producto/Backend | APIs de Integración, Despliegue del Mapa. |
| Edú O. | Director de Narrativa | Storytelling, Guion del Pitch, Mensaje Clave. |

