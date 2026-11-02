# BALI · Concesión Planta Desaladora para la Región de Coquimbo

Visor web interactivo de las **Bases de Licitación** (texto refundido) de la *Concesión Planta Desaladora para la Región de Coquimbo*. Todo el sitio está en **un solo archivo (`index.html`)**, autónomo y sin proceso de compilación. Reúne dos vistas que comparten los mismos datos:

- **Visor de texto**: índice, búsqueda, filtros, notas y panel de análisis.
- **Mapa mental**: mapa jerárquico de las exigencias, con la descripción y el texto completo de cada artículo.

Para pasar de una vista a otra, usa **✦ Mapa mental** (tecla `G`) en el visor y **← Visor** (tecla `V`) en el mapa. Ambos botones llevan al mismo artículo en la otra vista.

## Funcionalidades

| Módulo | Descripción |
|---|---|
| **Índice** | Tabla de contenidos navegable de los 523 artículos (Cap. 1 Administrativas, Cap. 2 Técnicas, Cap. 3 Económicas y Anexos). |
| **Búsqueda** | Búsqueda de texto completo, sin distinguir tildes, con frases exactas entre comillas y salto entre coincidencias. |
| **Filtros** | Por capítulo, sección, etapa, categoría, criticidad, multas, plazos y notas propias. |
| **Notas** | Notas por artículo o sobre texto seleccionado, con etiquetas (Observación, Riesgo, Consulta, Cumplido) y exportación a `.md` / `.csv`. |
| **Panel · Resumen** | Indicadores clave, distribución por categoría, etapa y criticidad, y rankings de artículos más referenciados y con más multas. Cada elemento aplica su filtro con un clic. |
| **Panel · Mapa** | Mapa de todo el articulado: un cuadro por artículo, con tamaño según la extensión del texto y color por criticidad, etapa, multas, capítulo o notas. |
| **Panel · Relaciones** | Grafo de referencias cruzadas (a qué artículos remite y quién lo cita), con navegación e historial. |
| **Sonidos y animaciones** | Señales sonoras sintetizadas (silenciables) y transiciones. Se respeta la preferencia de "reducir movimiento" del sistema. |

## Mapa mental

| Función | Descripción |
|---|---|
| **Despliegue jerárquico** | Árbol ordenado de izquierda a derecha (BALI → capítulo → sección → artículo), con columnas alineadas por nivel y animaciones de entrada y salida. |
| **Una rama a la vez** | Al desplegar una rama se contraen sus hermanas, para mantener el mapa ordenado (opción desactivable). |
| **Ficha del artículo** | Descripción del artículo, exigencias clave, plazos, entregables, multas, normativa y numerales del DS 15. |
| **Texto BALI** | Texto completo del artículo, con resaltado de los términos buscados. |
| **Relaciones** | Al seleccionar un artículo se trazan con animación sus dependencias (naranjo) y las referencias entrantes (gris). |
| **Búsqueda** | Por código, título o texto completo, con extracto de cada coincidencia. |
| **Filtros** | Etapa, criticidad, categoría, multas, plazos y entregables; opción para ocultar las ramas sin coincidencias. |
| **Vista 3D y sonido** | Plano en perspectiva con paralaje, tarjetas con relieve y señales sonoras sintetizadas (silenciables). |
| **Recorrido** | Presentación automática de los 15 artículos más críticos. |
| **Exportación** | Imagen PNG o SVG vectorial de la vista desplegada. |
| **Enlaces directos** | `index.html#a-1.7.5` abre el visor en ese artículo; `index.html#mapa/1.7.5` abre el mapa con ese artículo seleccionado. |

Teclas propias del mapa: flechas para navegar la jerarquía, `Enter` para desplegar o contraer, `1`–`4` para elegir el nivel, `0` para ajustar la vista, `C` para centrar, `D` para la vista 3D, `R` para los flujos entre secciones, `P` para el panel, `T` para el tema y `?` para la ayuda.

## Atajos de teclado (visor)

| Tecla | Acción |
|---|---|
| `/` | Ir a la búsqueda |
| `Enter` / `Shift+Enter` | Coincidencia siguiente / anterior |
| `M` | Abrir o cerrar el Panel |
| `1` `2` `3` | Resumen / Mapa / Relaciones |
| `S` | Activar o silenciar sonidos |
| `Retroceso` | Volver al artículo anterior en Relaciones |
| `G` | Abrir el mapa mental en el artículo actual |
| `Esc` | Cerrar panel o paneles laterales |

## Publicación con GitHub Pages

1. Sube `index.html` a la raíz del repositorio (opcionalmente también `README.md` y `.nojekyll`).
2. En **Settings → Pages**, elige *Deploy from a branch*, rama `main`, carpeta `/ (root)`.
3. El sitio queda disponible en `https://<usuario>.github.io/<repositorio>/`.

## Almacenamiento de notas

Las notas se guardan en el `localStorage` del navegador de cada usuario. No salen del equipo ni se comparten entre dispositivos. Para respaldarlas o compartirlas, usa **Mis notas → Exportar**.

## Fuente y verificación

El texto de los 529 artículos se extrajo directamente del PDF oficial **«21.11.25 - BALI Planta Desaladora Coquimbo VF Refundida»** (459 páginas), incluidas tablas, notas al pie, subíndices y superíndices. Se verificó que el 99,9 % de las líneas del cuerpo del PDF figuran en el sitio.

Correcciones respecto de la versión anterior del sitio:

- Se recuperaron pasajes que se habían perdido en la conversión anterior; por ejemplo, las reglas vi) a xiv) de 1.2.5, las glosas de la boleta de garantía en 1.4.5 y el texto completo de 1.13.2.4.
- Se agregaron 6 artículos que estaban fusionados con otros: 1.10.2.1.4, 1.13.2.5, 2.4.5.2, 2.4.6.5, 2.7.1.10.1 y 2.7.1.12.
- Se corrigieron 16 títulos. Por ejemplo, 1.17.2 «Efectos de la extinción de la concesión» y 1.17.3 «Recepción de la obra concesionada luego de la extinción de la concesión».
- La Tabla N° 6 (multas) se releyó del PDF: 231 multas, todas con monto y criterio (antes había 17 artículos con montos «s/d»). La criticidad se recalculó con esos montos.

Observaciones del propio PDF oficial (se mantienen tal como están):

- **Numeración duplicada:** los artículos «Discrepancias entre normas y documentos», «Reglas de interpretación» y «Definiciones» aparecen numerados 1.2.1, 1.2.2 y 1.2.3, repitiendo números anteriores. El sitio los numera 1.2.4, 1.2.5 y 1.2.6, y las referencias a «artículo 1.2.3» que aluden a definiciones enlazan a 1.2.6.
- **Referencias rotas:** en 1.14.5.1.7 aparece dos veces «¡Error! No se encuentra el origen de la referencia».
- **Numeración de multas:** la Tabla N° 6 no tiene multas N° 46 ni N° 155.

## Créditos técnicos

El archivo incluye la biblioteca [D3.js](https://d3js.org) v7.8.5 (licencia ISC) integrada en el archivo, por lo que funciona sin conexión.

## Aviso

Esta herramienta sirve de apoyo para la consulta. El texto oficial y vinculante es el publicado por el mandante del proceso de licitación.
