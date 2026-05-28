# Vixon Web — Proceso de diseño
### Documento interno · Mayo 2026

---

## Introducción

Este documento registra el proceso de diseño y desarrollo de la web de Vixon, desde las decisiones tipográficas hasta la arquitectura de la experiencia de usuario. Incluye los fundamentos de cada decisión y los criterios que guiaron la evolución del proyecto.

El objetivo central fue construir una web que no se parezca a nada del ecosistema de wearables deportivos convencional — que comunique tecnología de alto nivel con un tono cercano, que mezcle ciencia con emoción, y que convierta visitas en solicitudes de demo.

---

## 1. Posicionamiento y tono de marca

### 1.1 El problema de comunicación

Vixon opera en una categoría sin nombre propio. No es un smartwatch, no es una app de entrenamiento, no es equipamiento deportivo tradicional. Es un sistema de entrenamiento cognitivo — una categoría que el mercado no tiene del todo clara.

Esa ambigüedad es un riesgo de comunicación pero también una oportunidad: si Vixon define bien qué es, puede ser la referencia de esa categoría.

**Decisión:** El copy de la web evita descripciones técnicas en primer plano. En cambio, parte del problema del atleta (la velocidad de decisión, la reacción bajo presión) y llega a la solución de forma gradual. El producto se explica al verlo, no al leerlo.

### 1.2 Tono

La web trabaja con dos registros en tensión deliberada:

- **Ciencia aplicada:** referencias a journals, datos medibles (+23% velocidad de reacción, +31% precisión de decisión), nomenclatura técnica (NeuroEngine™, cognitive training protocol)
- **Cercanía deportiva:** voseo rioplatense en la versión española, frases cortas, verbos directos ("Entrená el cerebro", "Ganale al segundo")

Esa tensión es intencional. Un entrenador de fútbol argentino necesita sentir que esto es para él, no para un laboratorio de biomecánica. Y al mismo tiempo necesita respaldar la compra frente a una comisión directiva — para eso necesita datos.

### 1.3 NeuroEngine™ como elemento de marca

A mitad del proceso se introdujo NeuroEngine™ como nombre propio del motor de IA de Vixon. La decisión responde a tres necesidades:

1. **Diferenciación:** nombrar la tecnología la hace tangible y propietaria
2. **Credibilidad:** un sistema con nombre propio genera más confianza que "análisis con IA"
3. **Narrativa:** permite construir una historia progresiva — el chaleco recopila, la app controla, NeuroEngine™ aprende

NeuroEngine™ aparece en la sección del producto (The App), en la sección "Por qué funciona" (Neuro) y en el paso 4 del método. Se menciona siempre en contexto de datos y aprendizaje, nunca como característica técnica aislada.

---

## 2. Arquitectura de la experiencia

### 2.1 Flujo de la página

La web sigue una lógica narrativa lineal:

```
Intro (LEDs) → Hero → Ticker → Producto → Neuro → CTA intermedio → Experiencia → Testimonios → Demo
```

Cada sección cumple una función en el funnel de convicción:

| Sección | Función |
|---|---|
| Intro animada | Captar atención, generar curiosidad sin explicar |
| Hero | Declarar la propuesta de valor en una frase |
| Ticker | Reforzar el vocabulario de marca con términos clave |
| Producto | Mostrar el sistema (qué es, cómo funciona) |
| Neuro | Dar el argumento científico (por qué funciona) |
| CTA intermedio | Empujar a la acción en el punto de máxima convicción |
| Experiencia | Ampliar el mercado potencial (no solo fútbol) |
| Testimonios | Validación social, reducir fricción |
| Demo | Conversión |

### 2.2 El orden importa

La sección Neuro se ubica *antes* del CTA intermedio deliberadamente. Es el punto donde el visitante pasa de "me parece interesante" a "entiendo por qué esto funciona". El CTA llega cuando la convicción está en su punto más alto.

La sección de Experiencia se ubicó después del CTA porque amplía el mercado (futsal, academias juveniles, alto rendimiento) sin diluir el mensaje principal. Es validación adicional para quien ya está convencido, no parte del argumento central.

---

## 3. Diseño visual

### 3.1 Paleta

La paleta se construyó sobre un contraste máximo y un acento único:

- **Negro profundo (#060606)** como base — no negro puro para evitar el efecto "pantalla apagada"
- **Blanco cálido (#F2F2EE)** como texto — ligeramente amarillento, más legible y menos frío
- **Lima (#D2FF00)** como único acento — funciona como señal de alerta y de energía; remite a LEDs industriales, a señalética de emergencia, a lo tecnológico-orgánico

Las secciones alternan entre fondos oscuros (hero, neuro, testimonios) y fondos claros (#EDEDEA, #F2F2EE) para dar ritmo visual y evitar la fatiga de una web completamente dark.

### 3.2 Tipografía

**Inter** como fuente principal por tres razones:

1. **Legibilidad extrema en pantalla:** fue diseñada específicamente para interfaces digitales
2. **Peso 800/900 en uppercase:** da la contundencia de una fuente display sin perder neutralidad en cuerpo de texto
3. **Italic 800 con coherencia:** el uso de Inter italic 800 en los fragmentos en cursiva mantiene la misma familia pero genera variación rítmica

**DM Mono** para etiquetas, labels y datos técnicos. La tipografía monoespaciada refuerza el carácter técnico/científico sin recurrir a fuentes display especiales.

**Letter-spacing unificado:** todos los títulos en mayúscula usan `letter-spacing: -0.035em`, el mismo valor que el headline del hero. El tracking apretado en uppercase funciona contra la expansión natural de las letras capitales y da una sensación de densidad y confianza.

### 3.3 Interletrado: la decisión

Las tipografías en uppercase tienden a verse espaciadas por defecto porque las mayúsculas son más anchas que las minúsculas. El tracking positivo (.05em que había antes) amplificaba eso y daba una lectura más "display estético" pero menos contundente.

Con tracking negativo (-.035em), las letras se comprimen, el peso visual aumenta y los títulos ganan autoridad — especialmente en tamaños grandes. Es el mismo principio que usan titulares de medios como The Atlantic o marcas como Nike en sus campañas gráficas.

---

## 4. Hero

### 4.1 Video de fondo

El hero usa un video de jugadores entrenando con el chaleco (opacity 0.22) como fondo, con un sistema de capas encima:

1. **Video (z-index 0):** atmósfera y contexto real
2. **Scrim de gradiente (z-index 1):** asegura legibilidad del texto en cualquier frame del video
3. **Niebla fractal SVG (z-index 2):** capa de misterio generada con `feTurbulence` — da profundidad sin ser figurativa
4. **Chaleco con LEDs animados (z-index 10):** el producto como protagonista

La elección del video sobre una imagen estática responde a que el movimiento comunica algo que una foto no puede: el producto existe en movimiento real, no en un estudio.

### 4.2 Animación del chaleco

El chaleco empieza apagado (off.png) y a los 700ms hace transición a verde (green.png) con dos capas de blur adicionales para el glow. El timing de 700ms coincide con el momento en que el usuario ya leyó el primer título y está empezando a mirar hacia la derecha.

La animación de flotación (±8px, 6s, ease-in-out) evita que el chaleco se vea como un recorte estático pegado.

### 4.3 Headline

La headline del hero en español "ENTRENÁ / EL CEREBRO / GANALE / AL SEGUNDO" trabaja en cuatro líneas cortas con una cadencia rítmica deliberada:

- Las dos primeras líneas (lima) son el entrenamiento — el proceso
- Las dos siguientes (blanco) son el resultado — la ventaja competitiva

En inglés se tradujo como "TRAIN / THE BRAIN / OWN / THE SECOND" manteniendo la misma estructura de cuatro palabras/grupos cortos con la misma distribución de colores.

---

## 5. Sistema de producto — Las cards

### 5.1 Diseño de las cards

Las dos cards del producto (The Vest y The App) usan un sistema de visual area + body:

- **Visual area (520px de alto):** donde vive el producto. En The Vest, una foto full-bleed. En The App, una foto de sesión con fragments de UI flotantes superpuestos.
- **Body:** título, descripción, lista de features con hover reveal

La decisión de mostrar la UI de la app como "fragments" (no como screenshot completo) responde a que un screenshot completo se vería pequeño y confuso. Los fragments aislan los datos más importantes (reaction time, accuracy, session summary) y los muestran en contexto sin necesidad de leer la interfaz completa.

### 5.2 Feature list con hover

Las features de cada card usan un sistema de `grid-template-rows: 0fr → 1fr` para revelar la descripción en hover. Esta técnica CSS — sin JavaScript — permite una transición suave de altura-0 a altura-automática, algo que `max-height` no logra hacer de forma convincente (genera easing irregular en el extremo).

---

## 6. Sección Neuro — El argumento científico

### 6.1 Estructura de 4 pasos

El método Vixon se presenta en 4 pasos en una grilla 2×2, donde cada paso está respaldado por una publicación científica real:

1. **Percepción visual** — Journal of Sports Sciences, 2019
2. **Cognición bajo presión** — Frontiers in Psychology, 2022
3. **Ejecución en movimiento** — Int. Journal of Sports Physiology, 2020
4. **NeuroEngine™** — Journal of Sports Science & Medicine, 2021

El paso 4 integra NeuroEngine™ como el elemento que cierra el loop: los tres primeros pasos son el "por qué" científico, el cuarto es el "cómo lo hace Vixon".

### 6.2 Animación de activación

Cada card se activa (borde lima, texto brightens) cuando entra al viewport con IntersectionObserver (threshold 0.65). El efecto crea una lectura secuencial natural sin necesidad de interacción explícita.

---

## 7. Sección Experiencia — Los deportes

### 7.1 Sport hover

Las cards de deporte tienen un sistema de hover que mantiene el nombre del deporte en la posición original (bottom-left) mientras la descripción sube suavemente desde abajo. Se implementó con la misma técnica `grid-template-rows` para evitar el problema del `max-height`.

### 7.2 Selección de deportes

La selección de 5 deportes (Fútbol, Futsal, Academia juvenil, Deportes de equipo, Alto rendimiento) sigue una lógica de embudo:

- Los dos primeros son el mercado más obvio y cercano
- "Academia juvenil" apunta a un segmento de alta recurrencia (formativas compran año a año)
- "Deportes de equipo" abre sin especificar — basketball, handball, rugby
- "Alto rendimiento" valida la escala profesional del producto

---

## 8. Formulario y conversión

### 8.1 Campos del formulario

El formulario pide intencionalmente más datos que lo mínimo necesario (nombre + email). Los campos de club, rol y teléfono cumplen una función de calificación: un visitante que completa todos los campos tiene un nivel de intención mucho más alto que uno que solo pone su email.

El copy del CTA del formulario en español ("Quiero una demo") usa primera persona — no "Solicitar demo" — para reducir la fricción psicológica del clic.

### 8.2 Lo que pasa después

La sección "Qué pasa después" debajo del formulario anticipa el proceso post-envío. Está comprobado que mostrar el siguiente paso reduce la ansiedad de conversión: el visitante sabe exactamente qué esperar, lo que elimina la incertidumbre de "¿me van a llamar mil veces?".

---

## 9. Switch de idioma ES / EN

### 9.1 Decisión técnica

El switch de idioma se implementó como un sistema de JavaScript puro con un diccionario de traducciones integrado en el HTML. Se eligió este approach por sobre otras alternativas (páginas separadas, subdirectorios /en/, i18n frameworks) por tres razones:

1. **Un solo archivo:** la web es un HTML estático. Mantener dos versiones sincronizadas duplicaría el esfuerzo de mantenimiento.
2. **Sin dependencias externas:** no requiere build process, bundler ni servidor con routing
3. **Persistencia en localStorage:** la preferencia del usuario se recuerda entre sesiones

### 9.2 Criterios de traducción

Las traducciones al inglés siguieron tres criterios:

- **Mantener el tono:** el inglés es más directo que el español formal. "Request a demo" en lugar de "Request your demo session".
- **No traducir términos de marca:** NeuroEngine™, The Vest, The App, Match mode permanecen en inglés en ambas versiones.
- **Adaptar expresiones idiomáticas:** "Ganale al segundo" (culturalmente rioplatense) se convierte en "Own the second" — misma intensidad, diferente idioma.

---

## 10. Detalles y microinteracciones

### 10.1 Anillos decorativos

Las secciones Producto y Experiencia tienen anillos concéntricos decorativos implementados como `box-shadow` spread sobre un elemento de 2×2px. Seis capas de sombra a intervalos de 52px, con opacidad decreciente desde 0.038 hasta 0.005. El efecto es sutil — apenas visible en pantalla — y cumple la función de ocupar el espacio blanco sin competir con el contenido.

### 10.2 Ticker

El ticker entre el hero y el producto refuerza el vocabulario de marca (Cognitive Training, Reaction Speed, Decision Making, AI Lab, Wearable Tech) con una lógica de repetición publicitaria. Se pausa en hover para que el usuario pueda leer si quiere.

### 10.3 Nav activa

Los links de navegación se marcan como activos según la sección visible en el viewport (usando IntersectionObserver con un trigger al 40% del scroll). Esto orienta al usuario dentro de una página larga sin forzar un scroll-spy invasivo.

---

## 11. Decisiones que no se tomaron

Algunas ideas que se evaluaron y se descartaron:

- **Panel de tweaks:** se implementó durante el desarrollo para probar variantes de fuente y layout, y se eliminó en producción. Se bakearon los defaults directamente en el CSS para evitar deuda técnica.
- **Sección "Quiénes somos" desarrollada:** existe el CSS para una sección `#who` pero se decidió no incluirla en la primera versión para mantener el foco en el producto y la conversión.
- **Múltiples variantes de la app visual:** se construyeron tres variantes (live, match, session) con CSS show/hide. En producción se fijó "session" como default.

---

## Conclusión

La web de Vixon está construida para un visitante que llega con una pregunta específica: *¿esto sirve para lo que yo hago?* Cada decisión de diseño apunta a responder esa pregunta antes de pedirle que actúe.

El sistema funciona cuando el visitante llega al formulario habiendo pasado por la demo del producto, el argumento científico y la validación de otros entrenadores. En ese punto, la decisión de pedir una demo es casi obvia.

---

*Documento generado en Mayo 2026 · Vixon Cognitive Training System*
