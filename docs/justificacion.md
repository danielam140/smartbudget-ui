# SmartBudget — Justificación metodológica (Módulo 3)

## 1) Metodología CSS elegida: BEM
Se utiliza **BEM (Block, Element, Modifier)** para organizar estilos propios del proyecto de forma escalable.
- **Bloques**: `hero`, `features`, `pricing`, `faq`, `section-heading`
- **Elementos**: `hero__title`, `hero__subtitle`, `section-heading__title`
- **Modificadores**: `pricing-card--highlight`

Bootstrap se usa como framework para estructura y componentes, y BEM se aplica principalmente a secciones y componentes propios.

## 2) SASS con estructura 7-1
La carpeta `/sass` sigue el patrón **7-1**:
- `abstracts/`: variables y mixins
- `base/`: reset y tipografía global
- `layout/`: header/footer/helpers
- `components/`: botones/cards/forms
- `pages/`: estilos específicos por página
- `themes/`: espacio para temas
- `vendors/`: overrides (solo si fuera necesario)

El punto de entrada es `sass/main.scss`, y se entrega el CSS compilado en `css/main.css`.

## 3) Layout, modelo de cajas y responsividad
- Se aplica `box-sizing: border-box` para un control consistente del modelo de cajas.
- Se utiliza el **grid de Bootstrap** (`container`, `row`, `col-*`) para distribución principal.
- Se refuerzan alineaciones con Flexbox (por ejemplo, acciones del hero).
- Enfoque **mobile-first** con breakpoints:
  - Tablet: `min-width: 768px`
  - Desktop: `min-width: 992px`

## 4) Bootstrap 4 (integración)
Se integra Bootstrap 4 vía CDN para:
- **Navbar** (menú responsive)
- **Cards** (features, pricing, pasos)
- **Modal** (crear cuenta)
- **Collapse** (FAQ)
- Utilidades de espaciado y alineación

Se evita sobreescribir Bootstrap de forma innecesaria: los estilos propios se limitan a mejorar identidad y consistencia visual.

## 5) Navegabilidad y escalabilidad
- `index.html` incluye navegación por secciones (anchors).
- `pages/dashboard.html` es una página interior mínima para evidenciar escalabilidad del sitio.
