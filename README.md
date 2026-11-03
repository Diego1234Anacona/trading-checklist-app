# Trading Checklist — Cumplimiento del plan de trading

**En línea:** [trading.check.snakegym.cloud](https://trading.check.snakegym.cloud)
**172 commits** · proyecto propio, de punta a punta

Aplicación para revisar, operación por operación, si se cumplió el plan de
trading antes de entrar al mercado. La disciplina es lo que separa a un
operador rentable de uno que no lo es, y una lista que se responde en frío
evita la decisión impulsiva.

---

## Tecnologías

| Capa | Herramientas |
|---|---|
| **Frontend** | Angular 22, TypeScript, RxJS, SCSS, PWA instalable |
| **Backend** | Python, FastAPI |
| **Base de datos** | SQLite, con respaldo diario automático |
| **Seguridad** | WebAuthn — entrada por huella o clave de acceso, sin contraseña |
| **Infraestructura** | Docker, Docker Compose, Caddy con TLS automático, VPS Linux |

---

## Lo que resuelve

### Entrar sin contraseña, con la huella
Usa **WebAuthn**, el estándar de llaves de acceso: el navegador guarda una
llave en el aparato y el servidor solo conserva su parte pública. No hay
contraseña que robar ni que recordar, y la huella nunca sale del teléfono.

### Instalable, y rápida en el celular
Es una PWA: se instala desde el navegador y abre como una app, sin pasar por
una tienda. Está pensada para responderse de pie, antes de abrir una posición.

### Capas separadas desde el principio
Las rutas no saben cómo se guardan los datos y la capa de datos no sabe nada de
HTTP. Esa separación se paga sola: cambiar el motor de base de datos queda
contenido en dos archivos en vez de repartido por todo el proyecto.

### Respaldo diario, no opcional
La base se respalda sola todos los días. Un sistema que guarda el historial de
decisiones de alguien no puede perderlo por un disco que falla.

---

## Capturas

<!-- Pendientes -->
