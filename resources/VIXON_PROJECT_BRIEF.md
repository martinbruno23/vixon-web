# Vixon — Project Brief for Claude Code
> Leer este archivo al inicio de cada sesión antes de tocar cualquier código.

---

## El proyecto

Rediseño completo del sitio web de **Vixon** (vixon.pro), una empresa de tecnología deportiva que fabrica chalecos con LEDs programables para entrenamiento cognitivo. El sitio es desarrollado por **Yacaré** (yacare.io).

El sitio reemplaza el Framer actual. Se construye con **HTML/CSS/JS estático**, sin CMS, sin frameworks pesados. Deploy en **Vercel o Netlify**.

---

## El producto

Vixon son chalecos con LEDs programables que se controlan desde una app. Los jugadores reciben estímulos visuales durante el entrenamiento y deben reaccionar/decidir en tiempo real. El sistema tiene tres componentes:

- **The Top** — el chaleco físico con LEDs RGB
- **The App** — app del entrenador para configurar modos y leer datos
- **AI Lab** — reportes de rendimiento cognitivo post-sesión

**Propuesta de valor núcleo:** no entrena el cuerpo, entrena la velocidad de decisión y reacción cognitiva. "Faster Brain. Faster Body."

---

## Audiencia y decisores

- **Decisor principal:** entrenador semiprofesional/amateur que busca innovar
- **Decisor secundario:** dirigente o director técnico de club (maneja presupuesto)
- **Validador:** el jugador — entiende el producto rápido y genera demanda interna
- **Acción principal del sitio:** completar formulario de contacto para demo → lead para Meta Ads

---

## Identidad visual

- **Paleta:** negro profundo (#060606), lima (#C8F400), blanco roto (#F2F2EE), rojo LED (#FF3B3B)
- **Tipografías:** Bebas Neue (títulos/display), Inter 300/400/500 (cuerpo), DM Mono (labels, etiquetas, UI)
- **Estética:** editorial oscura, tecnológica, deportiva. Referencias: Apple, Nike, Whoop, Playermaker
- **NO usar:** fondos blancos, layouts genéricos, gradientes púrpura, tipografías sans-serif neutras tipo Inter como display

---

## Estructura del sitio (One Page con anchors)

| Sección | Anchor | Descripción |
|---|---|---|
| Intro video | — | Pantalla full con LEDs animados, logo centrado. Desaparece al scroll. |
| Hero | #hero | Imagen full-bleed del chaleco en acción. Headline + CTA + stats. |
| Product | #product | The Top + The App. Grid 2x2 alternando texto e imagen. |
| Experience | #experience | Grid de 6 deportes/contextos de uso con fotos reales. |
| Neuro | #neuro | 4 pasos del sistema cognitivo: Estímulo → Decisión → Ejecución → Data. |
| Who We Are | #who | Sorín (quote + imagen) + clubes + testimonial de entrenador. |
| Demo | #demo | Formulario de contacto (6 campos). CTA final. |
| Footer | — | Logo, links, copyright. |

---

## Credibilidad y contenido real disponible

- **Juan Pablo Sorín** — socio estratégico, advisor y embajador global. Se sumó por convicción en el producto.
- **Clubes:** Barracas Central Futsal (Buenos Aires), Port St. Lucie (Florida, USA)
- **Imágenes disponibles:** 15 fotos reales de sesiones de entrenamiento (jugadores con chalecos LED en campo). Verde y rojo. Formato portrait y landscape.
- **Video:** en producción. Cuando esté listo va en la intro en reemplazo del placeholder CSS.
- **KPIs:** a definir en conjunto con el cliente antes del lanzamiento.

---

## Archivos del proyecto

```
vixon_home_v1.html     — home completa (HTML/CSS/JS en un solo archivo)
images/                — carpeta con las 15 fotos del cliente (ver lista abajo)
```

### Imágenes disponibles (nombrar así en el proyecto)
| Archivo | Descripción | Uso sugerido |
|---|---|---|
| 1.jpg | Jugador de espaldas con chaleco verde (campo, pelota) | Hero o product |
| 2.jpg | Jugador corriendo con chaleco verde (motion blur) | Hero |
| 3.jpg | Jugador de frente, chaleco rojo encendido, señalando | Product / neuro |
| 4.jpg | Grupo corriendo en pista, chalecos rojos | Experience |
| 5.jpg | Dos jugadores en cancha profesional (LEDs rojo/verde) | Hero principal |
| 6.jpg | Grupo numeroso corriendo, primer plano | Experience |
| 7.jpg | Editorial oscuro "Faster Brain Faster Body", chalecos rojos | Social / background |
| 8.jpg | Jugador de espaldas, chaleco rojo, árboles | Product |
| 9.jpg | Grupo corriendo en pista, cielo nublado, motion blur | Experience |
| 10.jpg | Primer plano jugador corriendo, escalera de coordinación | Experience |
| 2.png | Grupo corriendo (versión editada) | Experience |
| 3.png | Grupo en pista, cielo dramático | Experience |
| 1.png | Jugador, chaleco verde fluorescente | Hero alternativo |
| 4__1_.jpg | Jugador corriendo, chaleco rojo, escalera | Experience |
| 5.jpeg | Horizontal, dos jugadores en cancha profesional | Hero landscape |

---

## Copy confirmado (en inglés)

- **Tagline:** Faster Brain. Faster Body.
- **Headline hero:** Faster Brain. Faster Body.
- **Eyebrow:** Cognitive Training System
- **CTA principal:** Get a Demo / Request a Demo
- **CTA secundario:** See how it works
- **Trust copy:** Response within 24 hours · No cost for first session · Works for clubs of any level
- **Sorín quote (tentativa):** "I joined Vixon because I see something real here. The way they're training decision-making inside movement — that's the future."

---

## Decisiones de diseño tomadas

- One page con scroll, no multipage — el visitante completa el journey sin salir
- Intro fullscreen que desaparece al hacer scroll (estilo Apple), placeholder CSS hasta tener video real
- Nav fija transparente que se oscurece con blur al scrollear
- Imágenes oscurecidas con overlay, nunca blancas ni de estudio
- Formulario de 6 campos: nombre, apellido, club, rol, email, teléfono
- Sin métricas numéricas en el hero hasta que el cliente tenga datos propios validados
- Idioma: inglés (versión en español pendiente como segunda fase)

---

## Gantt de trabajo (resumen)

| Semana | Fase |
|---|---|
| S1 (12–16 May) | Estrategia, contenido estructurado, KPIs — **en curso** |
| S2 (19–23 May) | Diseño home → **Reunión 1: Entrega home v1** |
| S3–S4 (26 May–6 Jun) | Subpáginas → **Reunión 2: Entrega subpáginas** |
| S5 (9–13 Jun) | Contenido real, QA, deploy → **Reunión 3: Entrega final** |
| Post-launch | Ciclo de mejora continua (servicio separado) |

---

## Cómo usar este brief en Claude Code

Al iniciar una sesión de trabajo en Claude Code, pegá este texto o referenciá el archivo:

```
Lee VIXON_PROJECT_BRIEF.md y usalo como contexto completo del proyecto 
antes de hacer cualquier cambio al código.
```

Luego describí el cambio específico que necesitás. Ejemplo:
```
Ajuste: en la sección Hero, el headline debe ir centrado en mobile.
Ajuste: agregar sección de precios placeholder entre Experience y Neuro.
Ajuste: el formulario debe tener validación básica antes del submit.
```

---

## Contactos del proyecto

- **Cliente:** Vixon — Lucas y Nayla
- **Agencia:** Yacaré (yacare.io)
- **Sitio actual:** vixon.pro (en Framer)
- **Sitio nuevo:** deploy en Vercel, dominio a confirmar

---
*Última actualización: Mayo 2026 · Yacaré*
