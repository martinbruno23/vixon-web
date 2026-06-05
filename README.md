# Vixon Web

Sitio web estático de Vixon Cognitive Training System. Un solo archivo HTML con CSS y JS embebidos — sin frameworks, sin build process.

## Estructura del proyecto

```
vixon-web/
├── index.html              # Toda la web (HTML + CSS + JS)
├── hero-v2-bg.mp4          # Video de fondo del hero
├── images/                 # Fotos generales (testimonios, etc.)
├── vixon_destacadas/       # Fotos destacadas del producto y deportes
├── logo/                   # Logo SVG en variantes
├── lights/                 # Assets de LEDs animados del hero
├── KV/                     # Assets varios
├── resources/              # Recursos adicionales
└── docs/
    ├── vixon-web-proceso-diseno.md    # Proceso de diseño (Markdown)
    └── vixon-web-proceso-diseno.docx  # Proceso de diseño (Word)
```

## Cómo trabajar

No requiere instalación ni dependencias. Abrir `index.html` directamente en el browser, o servir con cualquier servidor estático:

```bash
# Opción 1 — Python (viene con macOS/Linux)
python3 -m http.server 3000

# Opción 2 — Node
npx serve .

# Opción 3 — VS Code
# Instalar extensión "Live Server" y hacer clic en "Go Live"
```

## Deploy

El sitio se despliega automáticamente en **Vercel** con cada push a `main`.

URL de producción: `https://vixon-web.vercel.app`

Configuración en Vercel:
- **Framework:** Other (HTML estático)
- **Build command:** vacío
- **Output directory:** `.` (raíz)

## Funcionalidades implementadas

- **Switch ES / EN** — i18n completo con diccionario JS + persistencia en `localStorage`
- **Loader animado** — 4 tiras LED verticales con animación de color (lima / rojo)
- **Hero** — Video de fondo + variante niebla con ghost text (switch Video/Niebla)
- **Sección Producto** — Cards con acordeones tap/click (chevron indicator)
- **Sección Experiencia** — Flip cards (scaleX fold) con tap en mobile, hover en desktop
- **CTA secundario** — "Pedí más información" en hero y en sección experiencia
- **Responsive mobile** — Breakpoint en 900px, ajustes específicos para cada sección

## Paleta

| Token | Valor | Uso |
|---|---|---|
| `--black` | `#060606` | Fondo principal |
| `--white` | `#F2F2EE` | Texto principal |
| `--lime` | `#D2FF00` | Acento único |
| `--red` | `#FF3B3B` | Acento secundario (LEDs) |

## Tipografía

- **Inter** (800/900) — Títulos y UI principal
- **DM Mono** — Labels, datos técnicos, monoespaciado

---

*Vixon Cognitive Training System · Mayo 2026*
