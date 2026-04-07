# Insular S.p.A. — Dashboard de Cuentas

Dashboard de seguimiento de pagos y aportes de los 10 socios de Insular S.p.A.

## Estructura

Single-file HTML dashboard (`index.html`) con CSS + JS + Chart.js embebidos. No requiere build ni dependencias.

## Datos

- **Fuente exclusiva:** Cartolas Scotiabank verificadas (206 depósitos)
- **Clasificación automática:** Cada depósito se asigna cronológicamente a: GGCC → Cuota Mob → Capital → Construcción → Mobiliario → Otros

## Secciones

- **Resumen** — KPIs de aportes comprometidos ($331M), GGCC acumulado, estado general por socio
- **Aportes de Capital** — Desglose por año y categoría, sección construcción Club House Chaicura
- **GGCC (Cartolas)** — Grilla mensual de gastos comunes por socio/año
- **Sociedad** — Información legal, casa (mobiliario), historia, documentos

## Deploy en Vercel

1. Crear repo en GitHub:
   ```bash
   gh repo create insular-cuentas --public --source=. --push
   ```
2. Ir a [vercel.com](https://vercel.com), importar el repo `insular-cuentas`
3. Framework: **Other**, Output: raíz del proyecto
4. Deploy automático en cada push

## Actualización de datos

1. Agregar depósitos nuevos al array `ALL_DEPOSITS` en `index.html`
2. Actualizar `MESES_CON_DATOS_2026` con el último mes de cartola disponible
3. Commit + push → Vercel redeploya automáticamente
