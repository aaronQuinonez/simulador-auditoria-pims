# Simulador de Evaluación PIMS & Auditoría de Sistemas
### Unidad 2 — Preparación para el Examen Parcial (8vo Ciclo FIIS)

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub_Pages-blue?style=for-the-badge&logo=github)](https://aaronquinonez.github.io/simulador-auditoria-pims/)
[![Standard](https://img.shields.io/badge/Norma-ISO%2FIEC_27701%3A2025-06b6d4?style=for-the-badge)](https://www.iso.org/standard/83647.html)
[![Compliance](https://img.shields.io/badge/Reglamento-GDPR_%2F_RGPD-10b981?style=for-the-badge)](https://gdpr.eu/)
[![Architecture](https://img.shields.io/badge/Arch-Single_File_Vanilla-8b5cf6?style=for-the-badge)]()

Plataforma web interactiva, moderna y completamente responsiva (*Mobile-First*) diseñada para estudiantes y profesionales de Auditoría de Sistemas y Seguridad de la Información. Permite simular y validar conocimientos técnicos de los marcos normativos evaluados en la **Unidad 2: Sistema de Gestión de Privacidad de la Información (PIMS) y Marcos de Privacidad**.

---

## 🎯 Marcos Normativos Evaluados

El simulador contiene una base de datos de **60 preguntas de auditoría técnica** (30 teóricas y 30 casos prácticos situacionales) fundamentadas en:

1. **ISO/IEC 27701:2025 (Edición 2):** Cláusulas 4 a 10 y Anexos normativos A, B, C, D y E.
2. **ISO/IEC 27001 / ISO/IEC 27002:** Controles organizacionales y técnicos de seguridad de la información.
3. **ISO/IEC 29100:** Marco y los 11 Principios de Privacidad.
4. **Reglamento General de Protección de Datos (GDPR / RGPD):** Artículos 5, 28, 30 (ROPA), 32 y 33 (Notificación de brechas de seguridad dentro de las 72 horas).
5. **ISO/IEC 27018:** Código de prácticas para protección de PII en servicios de nube pública para encargados (*PII Processors*).
6. **ISO/IEC 29151:** Código de prácticas de controles extendidos para responsables (*PII Controllers*).
7. **Guía Técnica SoftExpert GRC:** Automatización del flujo de gestión de incidentes y brechas (*Data Breach*).

---

## 🧭 Estructura de Navegación del Proyecto

El proyecto está organizado de forma estandarizada y modular en archivos autónomos (*Single File HTML* con CSS moderno y JavaScript Vanilla incrustados):

| Archivo | Módulo / Semana | Descripción Temática | Preguntas |
| :--- | :--- | :--- | :---: |
| **[`index.html`](index.html)** | **Portal Hub Central** | Dashboard de navegación interactivo, hoja de ruta del sílabo y acceso directo a todos los bloques. | — |
| **[`bloque1.html`](bloque1.html)** | **Semana 07 (Tema 07)** | **Objetivos y Controles Anexo A (ISO/IEC 27701:2025):** Segregación de roles (Controller vs Processor), Declaración de Aplicabilidad (SoA), justificación de exclusiones y controles organizacionales A.1 a A.3. | 12 |
| **[`bloque2.html`](bloque2.html)** | **Semana 08 (Tema 08)** | **Directrices de Implementación Anexo B:** Guías B.1 (Controllers), B.2 (Processors) y B.3 (Controles comunes). Paridad en retiro de consentimiento, DPIA/PIA y contratos de encargo. | 12 |
| **[`bloque3.html`](bloque3.html)** | **Semana 09 (Tema 09)** | **Correspondencia con ISO/IEC 29100 y 11 Principios:** Mapeo formal de Tablas C.1 y C.2, principios no aplicables (N/A) a encargados y criterios de accountability. | 12 |
| **[`bloque4.html`](bloque4.html)** | **Semana 10 (Tema 10)** | **GDPR / RGPD y Herramientas SoftExpert:** Mapeo de Anexo D, Registro de Tratamientos (ROPA Art. 30), notificación de brechas en 72h (Art. 33) y gestión de incidentes. | 12 |
| **[`bloque5.html`](bloque5.html)** | **Semana 11 (Tema 11)** | **ISO/IEC 27018 e ISO/IEC 29151 (Anexo E):** Cloud Processors, control de requerimientos judiciales, cifrado en tránsito VPC y eliminación segura de datos. | 12 |
| **[`integral.html`](integral.html)** | **Examen Integral** | **Simulador Completo Unidad 2:** Las 60 preguntas integradas en una sola sesión continua con cronómetro general y emisión del Dictamen de Auditor Líder. | 60 |

---

## ⚡ Características Técnicas y de UI/UX

- **Diseño Mobile-First y Totalmente Responsivo:** Optimizado para smartphones (320px) hasta pantallas 4K (`overflow-x: hidden`).
- **Touch-Friendly Targets:** Botones y opciones de respuesta con altura mínima de `48px` - `52px` para evitar pulsaciones erróneas en pantallas táctiles.
- **Tipografía Escalable:** Escalado fluido con funciones CSS `clamp()` (`clamp(1rem, 2.5vw, 1.25rem)`).
- **Retroalimentación Inmediata de Auditoría:**
  - ✅ **Acierto:** Opción seleccionada resaltada en verde (`#10b981`).
  - ❌ **Fallo:** Opción seleccionada en rojo (`#ef4444`) e indicación inmediata de la opción correcta en verde.
  - 📋 **Justificación Auditora y Cita Normativa:** Contenedor desplegable con el código exacto de la cláusula o control ISO/GDPR correspondiente.
- **Doble Modalidad de Interacción:** Alternador rápido entre **Modo Examen (Focus)** (pregunta por tarjeta con paleta de salto rápido) y **Modo Lista Completa** (vista corrida de auditoría).
- **Audio Sintetizado Nativo:** Sonidos de acierto, error y fanfarria final generados en tiempo real mediante *Web Audio API* sin dependencias de red ni latencia, con opción de silenciar.
- **Dictamen Vigesimal Automatizado:** Pantalla de resumen final con cálculo en escala vigesimal peruana (0 a 20), porcentaje de efectividad, desglose por categoría y veredicto formal (**CONFORME / NO CONFORME**; aprobatorio $\ge 14.0$).
- **Filtros Dinámicos:** Selector para alternar entre `[Todos]`, `[Teoría Normativa]` y `[Casos Prácticos de Auditoría]`.

---

## 🚀 Despliegue en GitHub Pages

Este repositorio está preparado para funcionar sin proceso de construcción (*zero build steps*):

1. Ingresa a tu repositorio en GitHub: `https://github.com/aaronQuinonez/simulador-auditoria-pims`.
2. Dirígete a la pestaña **Settings** (Configuración) $\rightarrow$ sección **Pages** (en el menú lateral izquierdo).
3. En **Build and deployment** $\rightarrow$ **Source**, selecciona:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` / Folder: `/ (root)`
4. Haz clic en **Save** (Guardar).
5. En aproximadamente 1 minuto, la plataforma estará disponible públicamente en:
   👉 **`https://aaronquinonez.github.io/simulador-auditoria-pims/`**

---

## 🎓 Autoría y Créditos
- **Curso:** Auditoría de Sistemas
- **Semestre:** 8vo Ciclo
- **Institución:** Universidad Nacional de San Agustín de Arequipa (UNSA)
- **Facultad:** Facultad de Ingeniería de Producción y Servicios (FIIS)
- **Licencia:** MIT (Open Source con fines educativos y de acreditación académica)
