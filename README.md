# BuildLine — Landing Page
Landing page oficial de BuildLine, una plataforma inteligente de gestión y control logístico para el sector construcción.

## Sobre el producto
BuildLine centraliza en un solo dashboard todo lo que hoy se gestiona de forma dispersa con chats de WhatsApp, correos y planillas de Excel. Está diseñada para gerentes de proyectos, equipos de logística e ingenieros residentes que buscan optimizar la procura y el control de materiales en obra.

La plataforma permite:
- **Requerimientos digitales**: Monitoreo en tiempo real del estado de cada pedido desde que se genera la solicitud.
- **Alertas multicanal**: Notificaciones instantáneas vía WhatsApp y correo cuando ocurre un exceso de presupuesto o quiebre de stock.
- **Trazabilidad completa**: Historial de cada orden, cotización y factura por proyecto, exportable para auditoría.
- **Control de presupuestos**: Visualización del gasto real vs. proyectado para preservar el margen de utilidad del proyecto.

## Sobre este repositorio
Contiene el código fuente de la landing page pública del producto: una web construida con **Vue 3 + Vite**, liviana y responsiva, con soporte bilingüe (Inglés y Español) gestionado a través de `vue-i18n`.

## Estructura
- `public/assets/`
    - `icons/`: SVGs optimizados para cada sección.
    - `images/`: Fotografía, avatares de testimonios y arte de marca.
- `src/`
    - `assets/styles/`: Sistema de diseño basado en CSS Vanilla con variables y componentes modulares.
    - `shared/`: Componentes comunes como Header y Footer.
    - `value-proposition/`: Secciones principales de la landing (Hero, Features, Showcase, Testimonials).
    - `locales/`: Archivos JSON de traducción para soporte multi-idioma.
