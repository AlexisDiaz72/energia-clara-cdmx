# Energía Clara CDMX

Aplicación web que ayuda a los hogares de la Ciudad de México a entender su recibo de luz, saber en qué se va su gasto y encontrar apoyos para ahorrar y dar el paso a energías limpias.

**2º lugar** en el hackatón *Juventudes por la transición energética justa de la Ciudad de México*, organizado por el PNUD México y la Secretaría de Desarrollo Económico de la CDMX (octubre de 2026). Proyecto en equipo; desarrollo principal de la aplicación: **Alexis Flores Díaz**.

### [Ver demo en vivo](https://alexisdiaz72.github.io/energia-clara-cdmx/)

## El problema

Muchas familias pagan la luz sin saber cuánto consumen, qué aparatos les cuestan más ni qué apoyos existen. Pagar de más reduce el dinero disponible para otros gastos básicos, y en algunas alcaldías una parte importante de los hogares ni siquiera tiene contrato formal de luz.

## Qué hace

1. **Mapa de acceso a la luz.** Las 16 alcaldías con sus límites oficiales del INEGI y el porcentaje de hogares con contrato de CFE (por ejemplo, Milpa Alta: 43%).
2. **Recibo en pesos.** Calcula el recibo con la tarifa doméstica 1 de CFE por bloques de consumo (básico, intermedio y excedente) con IVA, y avisa cuando el hogar se acerca a la tarifa de alto consumo (DAC).
3. **¿Qué gasta más en tu casa?** Ordena los aparatos por consumo en kWh y en pesos, y muestra qué parte del recibo representan.
4. **Índice de Bienestar Energético (0 a 100).** Evalúa cuatro dimensiones ponderadas (asequibilidad, acceso, equipamiento y seguridad), incluida la parte del ingreso que se va en luz y si pagarla obliga a recortar otros gastos.
5. **Resultados y apoyos.** Estima el ahorro posible en pesos, kWh y CO₂, y recomienda programas según las respuestas (FIDE, SEDECO Ciudad Solar, SEDEMA, SENER, PROFECO y Locatel), con la lista de documentos que hay que llevar.

## Decisiones de diseño

- **Privacidad:** las respuestas se guardan solo en el navegador (`localStorage`); no hay servidor, registro ni envío de datos personales.
- **Sin instalación ni compilación:** React y htm vienen incluidos en `vendor.js`, así que la app funciona con cualquier servidor estático.
- **Accesibilidad:** tipografía Atkinson Hyperlegible, mapa navegable con teclado y respeto a la preferencia de "reducir movimiento".
- **Compartir:** el resumen de resultados se puede enviar por WhatsApp o copiar.

## Tecnologías

HTML · CSS · JavaScript · React (con htm, sin compilación) · SVG · localStorage · GitHub Pages

## Ejecutarlo localmente

```bash
git clone https://github.com/AlexisDiaz72/energia-clara-cdmx.git
cd energia-clara-cdmx
python3 -m http.server 8080
```

Abre `http://localhost:8080` en tu navegador. También funciona con la extensión Live Server de VS Code.

## Estructura del código

| Archivo | Contenido |
|---|---|
| `index.html` | Estructura de la página y carga de recursos |
| `styles.css` | Colores, tipografías y diseño |
| `app.js` | Datos (tarifas, alcaldías, aparatos, programas), cálculos y pantallas |
| `vendor.js` | Librerías React, ReactDOM y htm |

## Datos y fuentes

Cobertura de contratos residenciales de CFE 2025 por alcaldía, límites del Marco Geoestadístico del INEGI y potencial solar del Atlas AZEL. Las tarifas de CFE y los requisitos de los programas son aproximados y están marcados como `APROXIMADO` en `app.js`.

## Autor

**Alexis Flores Díaz** · [GitHub](https://github.com/AlexisDiaz72)
