# SEO Dashboard — nothingAD

Dashboard interno de auditoría SEO para el equipo de nothingAD. Lee datos directamente desde Google Sheets y los visualiza por cliente en tiempo real.

🔗 **[Ver dashboard](https://developmentnothingAD.github.io/seo-dashboard)**

---

## Qué hace

Muestra los resultados de los 5 agentes SEO construidos en n8n:

| Módulo | Fuente | Datos |
|--------|--------|-------|
| **Auditoría Técnica** | n8n + robots.txt + Sitemap | URLs en sitemap, bloqueos, alertas |
| **Cobertura de Indexación** | n8n + Search Console | URLs indexadas vs sitemap, páginas huérfanas |
| **On-Page** | Screaming Frog | Títulos, H1, meta descriptions, rendimiento, CLS, LCP |
| **Semrush** | API Semrush | Authority Score, keywords, backlinks, toxicidad |
| **Enlaces Internos** | Screaming Frog | 404, redirecciones, profundidad, páginas sin inlinks |

---

## Cómo funciona

1. Los agentes n8n ejecutan las auditorías y vuelcan los datos en Google Sheets
2. El dashboard lee el Sheets en tiempo real via la API pública de Google
3. Se filtra por cliente desde el selector superior

No requiere servidor ni base de datos. Todo es estático.

---

## Uso

1. Abre el dashboard
2. Selecciona el cliente en el desplegable superior
3. Navega por las pestañas para ver cada módulo
4. Pulsa **↻ Actualizar** para recargar los datos más recientes

---

## Stack

- HTML + CSS + JavaScript vanilla
- Google Sheets como base de datos
- n8n cloud para los agentes de automatización
- GitHub Pages para el hosting

---

## Mantenimiento

Para añadir un cliente nuevo simplemente ejecuta los agentes en n8n con el dominio del nuevo cliente. Los datos aparecerán automáticamente en el dashboard.

Para añadir nuevos módulos editar `index.html` y añadir la pestaña correspondiente.

---

*Uso interno nothingAD — no compartir externamente*
