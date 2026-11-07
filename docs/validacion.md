# Evidencia de validación

Fecha: **7 de noviembre de 2026**. Producto revisado: **Folio demo 0.1.1**, con los
cambios locales de manual, interfaz y respaldo de presentación.

## Verificaciones ejecutadas

| Área | Herramienta o recorrido | Resultado |
| --- | --- | --- |
| Backend | Suite pytest | 255 correctas y 122 omitidas |
| Backend | Ruff: análisis y formato | Correctos |
| Interfaz | Vitest | 2 pruebas correctas |
| Interfaz | TypeScript y compilación Vite | Correctos |
| Interfaz | Prettier | Correcto |
| Navegador | Playwright: modo demo/local y conexión fallida | 2 pruebas correctas |
| Proxy | Autenticación, configuración, descargas y escrituras | 3 pruebas correctas |
| Publicación | Revisión del historial, credenciales y archivos incluidos | Sin credenciales reales detectadas |

Los controles de secretos incluyen Gitleaks 8.30.1 y comparación local con los
valores privados actuales. Se revisaron 5 commits y 364 blobs históricos antes de
guardar esta revisión. Tres alertas iniciales correspondían a dos claves
ficticias de pruebas y un identificador ilustrativo de idempotencia; se verificaron
y se acotaron por valor exacto y ruta.

## Límites de esta evidencia

- Las 122 pruebas omitidas requieren PostgreSQL de pruebas configurado y no se
  presentan como superadas.
- Se ejecutó el archivo de pruebas de navegador del modo de despliegue; no toda
  la suite Playwright.
- Las verificaciones locales no certifican el estado actual de servicios remotos.
- La aceptación del plano por Siigo sigue pendiente.
- La detección automática de secretos reduce riesgos, pero no es una auditoría
  integral de seguridad de la aplicación.

## Revisión de la presentación pública

El repositorio público se prepara desde una carpeta independiente, sin copiar
el historial del código. Solo se incluyen documentos escritos para el portafolio
y tres capturas verificadas del escenario ficticio. No se publican resultados
brutos, registros, documentos DIAN, bases, claves ni configuraciones operativas.

El material de empleadores y clientes queda fuera del caso de estudio.
