# Bitácora diaria

Rastreador de hábitos y desintoxicación en una sola página HTML autocontenida — sin build, sin dependencias externas de pago, sin backend.

## Qué incluye

- Cuadrícula mensual de hábitos con categorías por color y emoji identificador
- Modo "Desintoxicación" (dark mode) para hábitos que quieres dejar, con racha de días limpios
- Gráficos de horas de sueño y de entrenamiento físico por día
- Registro diario con notas tipo diario personal
- Rachas (🔥) por hábito y por sección
- Perfil con nombre, fecha de inicio y rango que sube con el progreso
- Frase motivacional diaria
- Todo se guarda en `localStorage` del navegador; exporta/importa un respaldo en JSON desde el botón "Copia de seguridad"

## Cómo publicarlo con GitHub Pages

1. Crea un repositorio nuevo en GitHub (puede ser público o privado).
2. Sube `index.html` a la raíz del repositorio (y este `README.md` si quieres).
3. Ve a **Settings → Pages**.
4. En "Build and deployment", elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
5. Guarda. GitHub te dará una URL como `https://tu-usuario.github.io/tu-repo/` en uno o dos minutos.

## Notas

- Los datos viven solo en el navegador donde abras la página. Si la abres desde otro dispositivo, empezarás con la lista por defecto — usa el respaldo JSON para trasladar tu progreso.
- No requiere ningún paso de build: es un único archivo HTML.
