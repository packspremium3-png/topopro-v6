# TopoPro Elite V6.0 🇨🇴

> Aplicación web progresiva (PWA) de alta precisión para topografía, geodesia y navegación GNSS en Colombia. Soporta el sistema oficial **CTM12 (Origen Nacional Único)** y los 5 orígenes históricos **MAGNA-SIRGAS**.

---

## 🚀 Novedades y Mejoras Implementadas

1. **⏱️ Promediador GNSS de 60 Segundos:**
   - Adquisición de épocas durante 60 segundos con cronómetro interactivo y barra de progreso.
   - Cálculo de la media aritmética de coordenadas geodésicas y filtrado de precisión.
   - Alarma acústica y háptica (vibración) al finalizar los 60 segundos.
   - **Botón Destacado "Copiar Toda la Información del Punto":** Genera un reporte técnico completo listo para WhatsApp, cuaderno de campo o reporte de obra con ID, fecha, coordenadas proyectadas, Lat/Lon en sexagesimal, precisión y épocas.

2. **📐 Modo Replanteo (Stakeout) Opcional:**
   - Solo se muestra si el usuario lo activa desde la barra de herramientas.
   - Permite seleccionar un punto guardado o ingresar coordenadas objetivo (Norte / Este).
   - Calcula en tiempo real:
     - Distancia euclidiana al objetivo ($m$).
     - Azimut geodésico ($0^\circ$ a $360^\circ$ en GG° MM' SS").
     - Deltas de desplazamiento ($\Delta \text{Norte}$ y $\Delta \text{Este}$).
     - Brújula visual orientada hacia el punto objetivo.

3. **💾 Centro de Exportación Opcional:**
   - Solo se muestra cuando el usuario lo activa.
   - **CSV para AutoCAD Civil 3D:** Formato oficial `PUNTO,NORTE,ESTE,ELEVACION,DESCRIPCION`.
   - **TXT Topográfico:** Formato tabular para software de topografía.
   - **KML para Google Earth:** Visualización espacial de los puntos.
   - Copiado rápido de la tabla completa de puntos.

4. **🇨🇴 Geodesia Oficial de Colombia:**
   - **CTM12 (EPSG:9377):** Origen Nacional Único (IGAC Resoluciones 471 y 529 de 2020).
   - **MAGNA-SIRGAS:** Orígenes Bogotá (EPSG:3116), Este Central (3117), Este Este (3118), Oeste (3115) y Oeste Oeste (3114).
   - Doble motor geodésico: `Proj4js` + algoritmo riguroso de Gauss-Krüger offline con elipsoide GRS80.
   - Diferenciación clara entre cota elipsoidal WGS84 ($h$) y ortométrica.

5. **📶 Soporte Offline (PWA):**
   - Incluye `manifest.json` y `sw.js` (Service Worker).
   - Funciona sin internet ni señal celular en áreas rurales de campo.
   - Instalable en Android e iOS como aplicación nativa en la pantalla de inicio.

6. **🗺️ Capas de Mapa Dinámicas:**
   - Esri Satelital de alta resolución.
   - OpenStreetMap (Calles).
   - CartoDB Dark (Ahorro de batería en pantallas OLED).

7. **🧮 Conversor de Coordenadas Manual:**
   - Permite proyectar coordenadas en oficina sin encender el GPS.

---

## 📂 Estructura de Archivos

```
topopro-elite/
├── index.html       # Aplicación web completa y estilizada
├── manifest.json    # Configuración PWA e iconos
├── sw.js            # Service Worker para funcionamiento sin conexión
└── README.md        # Documentación y guía de uso
```
