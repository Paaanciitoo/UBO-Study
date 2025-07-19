# UBO Study – Plataforma de Estudio Radiológico (Tórax & Sistema Osteomuscular)

> **Estado del proyecto:** En desarrollo (v0.1.0)

## Tabla de Contenidos
1. [Descripción General](#descripción-general)
2. [Objetivos del Proyecto](#objetivos-del-proyecto)
3. [Alcance Académico](#alcance-académico)
4. [Características Principales](#características-principales)
5. [Estructura del Contenido Radiológico](#estructura-del-contenido-radiológico)
6. [Plantilla para Casos / Estudios](#plantilla-para-casos--estudios)
7. [Modelo de Metadatos (Opcional)](#modelo-de-metadatos-opcional)
8. [Tecnologías Utilizadas](#tecnologías-utilizadas)
9. [Arquitectura del Sitio](#arquitectura-del-sitio)
10. [Estructura de Carpetas Sugerida](#estructura-de-carpetas-sugerida)
11. [Guía de Desarrollo Local](#guía-de-desarrollo-local)
12. [Despliegue en GitHub Pages](#despliegue-en-github-pages)
13. [Buenas Prácticas (Código, Accesibilidad & Rendimiento)](#buenas-prácticas-código-accesibilidad--rendimiento)
14. [Convenciones de Nomenclatura](#convenciones-de-nomenclatura)
15. [SEO y Metadatos](#seo-y-metadatos)
16. [Roadmap](#roadmap)
17. [Contribuciones](#contribuciones)
18. [Licencia](#licencia)
19. [Descargo de Responsabilidad](#descargo-de-responsabilidad)
20. [Créditos y Referencias](#créditos-y-referencias)

---
## Descripción General
**UBO Study** es una plataforma estática de estudio y referencia radiológica orientada a la visualización, descripción y sistematización de hallazgos en **Tórax** y **Sistema Osteomuscular**, principalmente en el contexto de **Tomografía Computarizada (TC)** y **Resonancia Magnética (RM)**. El sitio organiza los contenidos en secciones temáticas y casos individuales, cada uno con componentes clínicos e imagenológicos clave.

## Objetivos del Proyecto
- Centralizar material visual y descripciones estandarizadas de hallazgos radiológicos.  
- Facilitar el aprendizaje estructurado mediante segmentación por región anatómica y modalidad.  
- Proveer una plantilla homogénea para la documentación de casos.  
- Servir como base extensible para futuras áreas (abdomen, neurología, etc.).

## Alcance Académico
El proyecto está dirigido a **estudiantes de tecnología médica / radiología**, **residentes** y **profesionales en formación**. No reemplaza material oficial ni orientación clínica especializada. Su foco es reforzar correlaciones entre:  
**Factores de riesgo → Signos imagenológicos → Síntomas clínicos**.

## Características Principales
- Navegación por pestañas / secciones (ej: *Tórax*, *Osteomuscular*).  
- Casos con imagen principal + descripciones estructuradas.  
- Componentes modulares reutilizables para listas y paneles informativos.  
- Diseño simple optimizado para expandirse con estilos escalables (BEM / Utility-first).  
- Compatible con despliegue inmediato en **GitHub Pages** (sin backend).  
- Posibilidad de evolución hacia *Single Page Application* ligera (añadiendo routing en JS o framework posterior).  

## Estructura del Contenido Radiológico
Cada estudio / caso debe incluir, como mínimo:
| Sección | Descripción | Ejemplos |
|---------|-------------|----------|
| **Título** | Nombre descriptivo del hallazgo o patología | "Neumonía Lobar Derecha", "Fractura Diafisaria de Húmero" |
| **Modalidad** | TC / RM / RX / Otra | "TC de tórax contrastada" |
| **Región Anatómica** | Segmento específico | Lóbulo superior derecho, rodilla, columna dorsal |
| **Imagen(es)** | Archivo(s) principal(es) con alt text | `imagenes/torax/neumonia_lobar_01.png` |
| **Factores de Riesgo** | Condiciones predisponentes | Tabaquismo, inmunosupresión |
| **Signos Imagenológicos en TC** | Hallazgos objetivos en la imagen | Consolidación segmentaria, vidrio esmerilado peribroncovascular |
| **Síntomas** | Manifestaciones clínicas comunes | Fiebre, disnea, dolor local |
| **Descripción / Comentario** | Texto integrador opcional | Contexto, evolución, diagnóstico diferencial breve |
| **Referencias** | Bibliografía / enlaces confiables | Libros, artículos, guías |

## Plantilla para Casos / Estudios
Ejemplo en **Markdown** (recomendado para versionado):
```markdown
---
id: neumonia_lobar_derecha
modalidad: TC
region: Torax
categoria: Infeccioso
fecha_revision: 2025-07-15
version: 1.0
---
# Neumonía Lobar Derecha

**Modalidad:** TC de tórax contrastada  
**Región anatómica:** Lóbulo superior derecho  

## Imagen
![TC axial lóbulo superior derecho](../imagenes/torax/neumonia_lobar_01.png "Consolidación lobar")

## Factores de Riesgo
- Tabaquismo crónico
- EPOC
- Edad > 65 años

## Signos Imagenológicos en TC
- Consolidación homogénea segmentaria
- Broncograma aéreo presente
- Discreto engrosamiento peribronquial

## Síntomas
- Fiebre (38–39 °C)
- Tos productiva
- Disnea leve de esfuerzo

## Comentario
La consolidación pulmonar con broncograma aéreo sugiere proceso alveolar infeccioso agudo. Correlacionar con laboratorio (PCR, leucocitosis) y evolución clínica.

## Referencias
1. XYZ Manual de Radiología Torácica, 2023.
2. Guías clínicas neumonía adquirida en la comunidad.
