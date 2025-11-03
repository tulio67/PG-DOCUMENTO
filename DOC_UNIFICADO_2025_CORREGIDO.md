Universidad Mariano Gálvez de Guatemala
Centro Universitario de Chiquimulilla
Facultad de Ingeniería en Sistemas de Información y Ciencias de la Computación

“Prototipo de plataforma web con inteligencia artificial (React, Spring Boot, MySQL, OpenAI) para la gestión y asesoría inmobiliaria en ROOTS REAL ESTATE Guatemala”

Trabajo de Graduación presentado por:
Marco Tulio Lara Salazar
Previo a optar al grado académico de
Licenciado en Ingeniería en Sistemas de Información y Ciencias de la Computación
y al título profesional de Ingeniero en Sistemas de Información y Ciencias de la Computación.

Asesor académico: Axcel Yobany Pineda Ortiz
Guatemala, mayo de 2025

Autoridades de la Facultad:
- Decano: Ing. Jorge Alberto Arias Tobar
- Secretario: Ing. Hugo Adalberto Hernández Santizo

Nota para maquetación en Word
- Preliminares (carátula, hojas oficiales, índices, glosario, referencias): numeración romana (i, ii, iii…).
- Cuerpo (Capítulos I–VI): numeración arábiga (1, 2, 3…).
- Inserta un salto de sección entre preliminares y el Capítulo I para separar numeraciones.

Índice General
[Inserta un Índice automático en Word y actualízalo al final]

Índice de Figuras
- Fig. 1. Proceso AS-IS de captación y atención ................................ [pág.]
- Fig. 2. Proceso TO-BE con plataforma web ...................................... [pág.]
- Fig. 3. Arquitectura lógica de la solución ..................................... [pág.]
- Fig. 4. Diagrama de Componentes ................................................. [pág.]
- Fig. 5. Diagrama de Clases (núcleo de dominio) ............................... [pág.]
- Fig. 6. Secuencia: Inicio de chat cliente–asesor ............................ [pág.]
- Fig. 7. Diagrama Entidad–Relación (ER) ........................................ [pág.]
- Fig. 8. Mockups/Prototipo Figma (capturas) .................................. [pág.]

Índice de Tablas
- Tabla 1. Variables e indicadores operacionales ............................. [pág.]
- Tabla 2. Resultados de encuesta (N=80) ........................................ [pág.]
- Tabla 3. Matriz de trazabilidad Hi–Objetivos–Contenido–Conclusiones ...... [pág.]
- Tabla 4. Plan de pruebas (casos principales) ................................ [pág.]
- Tabla 5. Presupuesto estimado ................................................ [pág.]
- Tabla 6. Cronograma de actividades ........................................... [pág.]

Glosario
- IA (Inteligencia Artificial): Sistemas que realizan tareas que requieren razonamiento humano.
- PLN (Procesamiento de Lenguaje Natural): Técnicas para entender y generar lenguaje humano.
- Chatbot: Programa que conversa con el usuario y responde automáticamente.
- Catálogo Digital: Listado en línea de propiedades con filtros de búsqueda.
- RAG (Retrieval-Augmented Generation): Técnica para dar contexto documental a modelos de IA.
- UX (Experiencia de Usuario): Calidad de la interacción usuario–sistema.
- SLA: Acuerdo de nivel de servicio (tiempos y calidad esperada).

Introducción
En la era de la transformación digital, el mercado inmobiliario demanda eficiencia, trazabilidad y experiencia de usuario de calidad. En ROOTS REAL ESTATE Guatemala, los procesos de captación, publicación y asesoría operan mayormente con medios tradicionales (redes sociales, mensajería y acuerdos verbales), provocando datos dispersos, baja trazabilidad y tiempos de respuesta irregulares. Se propone un prototipo de plataforma web con inteligencia artificial para centralizar la gestión, habilitar un catálogo con filtros, permitir comunicación trazable (chat en vivo) y asesoría automatizada (chatbot IA con OpenAI). El enfoque es funcional, escalable y alineado con el contexto guatemalteco, con potencial de uso internacional.

Objetivos
- Objetivo General: Desarrollar una plataforma web para ROOTS REAL ESTATE Guatemala que centralice la gestión de propiedades y mejore la interacción asesor–cliente mediante IA (OpenAI), filtros avanzados y chat en vivo.
- Objetivos Específicos:
  1. Implementar un catálogo interactivo con imágenes, precios y detalles.
  2. Desarrollar un panel para gestión individual de propiedades por asesor.
  3. Integrar chat en vivo cliente–asesor con trazabilidad.
  4. Incorporar un chatbot de IA para asesoría personalizada.

Alcance
- Prototipo funcional enfocado al mercado guatemalteco, disponible vía web, con buscador y filtros avanzados, chat en vivo y chatbot IA.
- Usuarios: clientes (nacionales e internacionales), asesores, administrador.
- No incluye en esta fase: pagos en línea, firma digital, integración bancaria; el diseño prevé escalabilidad futura.

Limitaciones
- Dependencia de conectividad a internet.
- Capacidad del chatbot sujeta al modelo y contexto disponibles.
- El éxito depende de la calidad y volumen del catálogo administrado por los asesores.

CAPÍTULO I — Marco Conceptual
Antecedentes
ROOTS REAL ESTATE Guatemala gestiona captación y venta con procesos informales y canales dispersos. En la región, plataformas especializadas han demostrado mejoras en accesibilidad, filtrado y tiempos de respuesta con catálogos digitales, chat en vivo y automatización.

Planteamiento del Problema
La ausencia de un sistema centralizado genera desactualización, errores en fichas, baja trazabilidad y tiempos de respuesta variables. La visibilidad limitada (dependencia de redes sociales) restringe el alcance y la segmentación efectiva. Esto reduce eficiencia operativa y conversión de prospectos.

Supuestos
- La adopción de IA en el proceso comercial reducirá tiempos, mejorará satisfacción y aumentará efectividad de la asesoría.
- El personal será capacitado y adoptará gradualmente la plataforma.

Preguntas de Investigación
1) ¿Cómo mejora la plataforma con IA la eficiencia en la gestión inmobiliaria?
2) ¿Qué impacto tiene un chatbot inteligente en la experiencia del cliente?
3) ¿En qué medida los filtros avanzados facilitan búsquedas pertinentes?
4) ¿Puede la gestión por asesor reducir errores en inventario?
5) ¿Qué nivel de aceptación tiene la plataforma frente a métodos tradicionales?
6) ¿Se reducen tiempos de respuesta y mejora el seguimiento asesor–cliente?

Justificación
La digitalización centraliza datos, automatiza tareas y mejora la experiencia. Un sistema web con IA, filtros y comunicación integrada fortalece la trazabilidad, eficiencia y competitividad frente a un mercado cada vez más digital.

Consecuencias del problema (si no se interviene)
 a) Ineficiencia en la gestión y pérdida de oportunidades. b) Comunicación informal con potencial de malentendidos. c) Bajo alcance de mercado y menor competitividad.

CAPÍTULO II — Marco Teórico
2.1 Inteligencia Artificial (IA) en el sector inmobiliario
- Aplicaciones: valoración automatizada, recomendación de propiedades, priorización de leads, análisis de mercado.
- Beneficios: reducción de tiempos, personalización, estandarización de procesos.
- Riesgos: sesgos de datos, privacidad, transparencia de modelos.

2.2 Procesamiento de Lenguaje Natural (PLN)
- Conceptos: embeddings, clasificación de intenciones, resumen y extracción de entidades.
- Modelos generativos (GPT) y técnica RAG para respuestas contextualizadas con inventario inmobiliario y políticas de negocio.

2.3 Chatbots y sistemas de recomendación
- Chatbots: intents, desambiguación, handoff a humano, logging.
- Recomendadores: basado en contenido (características) y colaborativo; señales como ubicación, presupuesto, tipología y preferencias del usuario.

2.4 Arquitectura de aplicaciones web
- Cliente–Servidor, API REST/JSON, autenticación (JWT), paginación/búsqueda.
- Patrones de diseño (MVC, DTOs, repositorios) y principios SOLID.

2.5 UX, accesibilidad y responsividad
- Heurísticas de Nielsen, diseño responsive, WCAG 2.1 AA.
- Rendimiento y tiempos de carga, legibilidad y consistencia de interfaz.

2.6 Seguridad y protección de datos
- Cifrado en tránsito (HTTPS), gestión de secretos, roles/permisos, control de acceso.
- Retención y minimización de datos, cumplimiento normativo aplicable.

2.7 Métricas y evaluación
- KPIs: tiempo de respuesta asesor, tasa de conversión, satisfacción (SUS/NPS), completitud de fichas, precisión de filtros.

CAPÍTULO III — Metodología
Población y muestra
- Población (N): 80 personas (15 colaboradores + 65 clientes activos).
- Nivel de confianza: 95% (Z=1.96), p=0.5, q=0.5, error e=0.05.
- Fórmula (corrección por población finita):
  n = N·Z²·p·q / [ e²·(N−1) + Z²·p·q ]
  n = 80·(1.96)²·0.25 / [ (0.05)²·79 + (1.96)²·0.25 ] = 76.832 / 1.1579 = 66.35 → 66.

Instrumento (Encuesta)
Objetivo: Levantar percepciones sobre búsqueda, filtrado, asesoría y uso de IA en compra/venta inmobiliaria. 15 preguntas dicotómicas (Sí/No).

Procedimiento
Aplicación a muestra de 66; en los resultados recopilados se consignan 80 respuestas totales (consistencia unificada en porcentajes a 80).

Operacionalización de variables
- Variable Independiente: Implementación de plataforma web con IA.
- Variable Dependiente: Eficiencia en gestión inmobiliaria y comunicación asesor–cliente.

Tabla 1. Variables e indicadores operacionales (resumen)
- Plataforma Web con IA: organización de información (fichas completas/actualizadas), errores reportados.
- Asesoría Digital IA: frecuencia de uso de chatbot, satisfacción percibida.
- Interacción Cliente–Asesor: tiempo de respuesta, interacciones efectivas.
- Experiencia de Usuario: uso de filtros, tasa de conversión.

CAPÍTULO IV — Análisis de la Aplicación y Modelado de Procesos
4.1 AS-IS (actual)
- Captación y publicación por canales informales, datos dispersos, trazabilidad baja, tiempos de respuesta variables, cierre presencial.

4.2 TO-BE (propuesto)
- Alta/edición de propiedades en sistema centralizado; catálogo con filtros; chat en vivo y chatbot IA; seguimiento trazable y analítica básica.

4.3 Modelos de proceso
- Proceso de captación y publicación (BPMN/diagrama de flujo) [Fig. 1–2].
- Proceso de contacto y asesoría (chat en vivo) [Fig. 6].
- Proceso de seguimiento y cierre (estados de propiedad y SLA).

4.4 Reglas de negocio
- Campos obligatorios de ficha, estados (disponible/reservada/vendida), SLA de respuesta, política de actualización de inventario.

CAPÍTULO V — Diseño (UML, Arquitectura, ER)
5.1 Arquitectura lógica
- Frontend: React; Backend: Spring Boot; BD: MySQL; IA: OpenAI API; despliegue: Vercel (frontend) y servicio PaaS para backend [Fig. 3–4].

5.2 Diagrama de Clases (dominio)
- Entidades: Propiedad, Asesor, Cliente, Conversación, Mensaje; relaciones 1–N; validaciones y estados [Fig. 5].

5.3 Diagramas de Secuencia
- Caso: cliente inicia chat desde una ficha; secuencia UI→API→Servicio→BD→Notificación [Fig. 6].

5.4 Diagrama ER
- Índices por ubicación y rango de precios; normalización de tablas; claves primarias/foráneas [Fig. 7].

Nota: Se acompaña explicación bajo cada diagrama en el documento final (propósito y decisiones de diseño).

CAPÍTULO VI — Desarrollo, Pruebas e Implementación
6.1 Entorno y herramientas
- Frontend: React (UI, estado, router).
- Backend: Spring Boot (REST, validación, seguridad).
- Base de datos: MySQL (alternativa Oracle).
- IA: OpenAI API (modelo según costo/latencia).
- Infraestructura: Vercel (frontend), backend en PaaS (Render/Heroku/otro); variables de entorno y secretos.

6.2 Estructura del proyecto
- Separación de capas, DTOs, validaciones, manejo de errores, logging.

6.3 Funcionalidades desarrolladas
- Catálogo con filtros (ubicación, precio, tipo, características).
- Gestión por asesor (CRUD de propiedades, panel).
- Chat en vivo cliente–asesor con trazabilidad.
- Chatbot IA (prompts, límites, derivación a humano).

6.4 Seguridad
- Autenticación/autorización por roles; protección de datos; cifrado en tránsito; auditoría básica.

6.5 Plan de pruebas y resultados (resumen)
- Tipos: unitarias, integración, sistema, aceptación, usabilidad y rendimiento básico.
- Criterios de aceptación: precisión de filtros (≥95%), notificación de chat <10s, errores 4xx/5xx controlados, satisfacción percibida ≥4/5.
- Ver Anexo B para plan detallado y evidencias.

6.6 Implementación y despliegue
- Pasos de despliegue, configuración de dominios y variables; plan de rollback; monitoreo y registro de incidentes.

6.7 Lecciones aprendidas y trabajo futuro
- Ampliar contexto del chatbot con RAG, integrar pagos/firma digital, métricas avanzadas, seguridad endurecida.

Resultados de la Encuesta
Tabla 2. Resultados (N = 80) — Porcentajes corregidos
| Pregunta | Sí (n) | No (n) | Sí (%) | No (%) |
|---|---:|---:|---:|---:|
| 1 | 60 | 20 | 75.00 | 25.00 |
| 2 | 55 | 25 | 68.75 | 31.25 |
| 3 | 59 | 21 | 73.75 | 26.25 |
| 4 | 52 | 28 | 65.00 | 35.00 |
| 5 | 56 | 24 | 70.00 | 30.00 |
| 6 | 61 | 19 | 76.25 | 23.75 |
| 7 | 54 | 26 | 67.50 | 32.50 |
| 8 | 52 | 28 | 65.00 | 35.00 |
| 9 | 53 | 27 | 66.25 | 33.75 |
| 10 | 63 | 17 | 78.75 | 21.25 |
| 11 | 51 | 29 | 63.75 | 36.25 |
| 12 | 58 | 22 | 72.50 | 27.50 |
| 13 | 55 | 25 | 68.75 | 31.25 |
| 14 | 55 | 25 | 68.75 | 31.25 |
| 15 | 55 | 25 | 68.75 | 31.25 |

Conclusiones
- La plataforma propuesta mejora trazabilidad y tiempos de respuesta, apoyando la hipótesis Hi.
- Mayorías significativas apoyan filtros avanzados y asesoría IA; se evidencia aceptación de la plataforma digital.
- La centralización de datos reduce errores y mejora eficiencia operativa.

Recomendaciones
- Capacitar asesores y definir guías de uso.
- Monitorear KPIs (respuesta, conversión, satisfacción) de forma continua.
- Evolucionar el chatbot con RAG y mejores prompts.
- Planificar fase productiva con seguridad, monitoreo y respaldo.

Matriz de Trazabilidad (Tabla 3)
| Elemento | Descripción | Sección | Evidencia |
|---------|-------------|---------|----------|
| Hipótesis (Hi) | IA mejora eficiencia gestión/comunicación | Cap. III | Indicadores |
| Obj. General | Plataforma centralizada con IA | Objetivos | Cap. VI |
| Obj. Específicos | Catálogo, gestión por asesor, chat, chatbot | Objetivos | Cap. VI + Plan de Pruebas |
| Desarrollo | Implementación de módulos | Cap. VI | Capturas/evidencias |
| Pruebas | Validación de flujos | Anexo B | Resultados |
| Conclusiones | Logros vs Hi/Objetivos | Conclusiones | KPIs |

Presupuesto Estimado (Tabla 5)
| Concepto | Costo Estimado (GTQ) |
|---|---:|
| Suscripción API OpenAI (básico) | 100.00 |
| Dominio y hosting (opcional) | 250.00 |
| Internet (mes de desarrollo) | 400.00 |
| Herramientas UI/UX (Figma Pro) | 120.00 |
| Respaldo en la nube (opcional) | 300.00 |

Cronograma de Actividades (Tabla 6)
- Levantamiento y requisitos: 1 semana
- Arquitectura, frontend y backend: 1 semana
- Maquetado prototipo visual: 2 semanas
- Módulo catálogo: 2 semanas
- Módulo gestión por asesor: 2 semanas
- Integración chatbot IA: 2 semanas
- Chat en vivo: 2 semanas
- Filtros avanzados: 2 semanas
- Pruebas funcionales/UI: 1 semana
- Documentación técnica: 1 semana

Referencias (APA 7ª)
- Russell, S., & Norvig, P. (2021). Artificial Intelligence: A Modern Approach (4th ed.). Pearson.
- Jurafsky, D., & Martin, J. H. (2023). Speech and Language Processing (3rd ed., draft). https://web.stanford.edu/~jurafsky/slp3/
- OpenAI. (2024). OpenAI API Documentation. https://platform.openai.com/docs/
- W3C. (2018). Web Content Accessibility Guidelines (WCAG) 2.1. https://www.w3.org/TR/WCAG21/
- ISO/IEC. (2018). ISO/IEC 27001:2013 Information security management.
- [Añadir artículos específicos sobre IA en real estate y chatbots en atención al cliente usados en Cap. II–VI.]

Anexos
Anexo A — Manual de Usuario (resumen)
- Registro/Acceso (cliente/asesor)
- Catálogo y filtros
- Chat en vivo y notificaciones
- Chatbot IA (buenas prácticas y límites)
- Panel del asesor (CRUD propiedades, estados, imágenes)
- Privacidad y soporte

Anexo B — Plan de Pruebas (resumen)
| ID | Módulo | Caso | Pasos | Esperado | Aceptación |
|----|--------|------|-------|----------|------------|
| PF-001 | Catálogo | Filtrar por ubicación | Buscar “Chiquimulilla” | Lista correcta | ≥95% acierto |
| PF-002 | Catálogo | Rango de precios | Q.500k–Q.800k | Solo en rango | Desv. ≤ 5% |
| PF-003 | Asesor | Crear propiedad | Completar y guardar | Visible en catálogo | Persistencia OK |
| PF-004 | Chat | Iniciar chat | Desde ficha | Conversación creada | Notificación <10s |
| PF-005 | Chatbot | Consulta IA | “Casa 3 hab zona X” | Sugerencias pertinentes | ≥4/5 relevancia |

Anexo C — Resultados completos de la encuesta
- Tabla 2 ya incluida. Incluir gráficos (barras/pastel) tras exportar a Word.

Anexo D — Prototipo Figma
- URL: https://www.figma.com/make/3SpIz0UwVTINJ2wz00Et5z/Sistema Integral-de-Inmobiliaria?node-id=0-1&p=f&t=J5IiliuwgVBN9AlZ-0&fullscreen=1

Notas finales de consistencia aplicadas
- Autoría y asesoría unificadas.
- Corrección de acentos/ñ (UTF-8) y porcentajes (P15 corregida a 68.75%/31.25%).
- Objetivo de encuesta corregido (se elimina la referencia a “teléfono”).
- Cap. II ampliado; Cap. VI añadido; Índices de Figuras/Tablas, Glosario, Referencias y Anexos incluidos.