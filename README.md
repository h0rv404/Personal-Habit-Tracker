# Bitácora diaria · edición negro y dorado

## Abrir y conservar tus datos

Descarga `index.html` y ábrelo en tu navegador. No necesita Python, instalación, cuenta ni conexión. También puedes sustituir el HTML de tu publicación actual por este archivo.

**Antes de cambiar de archivo o ubicación, abre tu versión anterior y descarga un respaldo JSON.** Los registros están en el navegador, no dentro del HTML. Si la nueva versión aparece vacía, abre **Respaldo**, selecciona tu JSON y pulsa **Importar**. Se mantiene la clave `bitacora.v1` y se aceptan los respaldos originales. La ubicación de un archivo local puede afectar al acceso a los datos guardados.

## Uso

- **Registrar hoy:** abre hábitos, sueño, entrenamiento, cantidades y notas. También puedes abrir una fecha desde el calendario, la cuadrícula, los gráficos o las barras semanales.
- **Cuadrícula:** pulsa una celda para marcar. En hábitos a reducir, alterna cumplido → ocurrió → sin registro. Los días futuros y las casillas anteriores al inicio están bloqueados.
- **Deshacer marca:** revierte la última modificación hecha en una celda, sin sustituir las notas ni otras cantidades.
- **Buscar y filtrar:** combina el buscador con una categoría. Las estadísticas generales siguen mostrando toda la sección.
- **Ficha del hábito:** pulsa su nombre o su racha para consultar racha actual, récord histórico, semana e hitos de 3, 7, 14, 30 y 90 días.
- **Cantidades:** en la ficha, añade una etiqueta, unidad y referencia semanal opcional. Introduce las cantidades reales en el diario. Se admiten minutos, horas, gramos, mililitros, kilómetros, páginas, repeticiones, kcal y soles.
- **Horas estimadas por marca:** parámetro independiente de las cantidades reales. Cero desactiva esta estimación. Las equivalencias no representan tiempo cronometrado.
- **Editar lista:** personaliza nombres, iconos, categorías y orden; añade o elimina hábitos. Eliminar y restaurar requieren confirmación.
- **Respaldo:** descarga o copia JSON; importa pegando el contenido o eligiendo un archivo. La importación reemplaza el estado completo y pide confirmación.

## Ejemplos de métricas

| Hábito | Etiqueta | Unidad |
| --- | --- | --- |
| Practicar lectura | Páginas leídas | pág. |
| Meditar | Tiempo de meditación | min |
| Caminar | Distancia recorrida | km |
| Alimentación | Carbohidratos consumidos | g |
| Reducir compras | Ahorro registrado | S/ |

La cantidad y la casilla son independientes: registrar 20 minutos no marca automáticamente un hábito. Vacío significa sin datos; cero es un registro real. Las referencias semanales son de acumulación y no son límites de consumo ni recomendaciones de salud. El tracker no calcula carbohidratos “perdidos”, grasa perdida ni calorías quemadas a partir de casillas.

## Cómo se calculan los indicadores

- El resumen superior y las cantidades usan **la semana actual, de lunes a domingo**, hasta hoy, aunque estés consultando otro mes.
- La cuadrícula, los gráficos y el cumplimiento mensual usan **el mes visible**.
- El cumplimiento cuenta oportunidades desde la fecha de inicio del perfil; los hábitos nuevos tienen además su propia fecha de creación. Los días sin marcar no cuentan como cumplidos.
- La racha actual termina hoy si hoy está registrado; si todavía no lo está, conserva la racha que termina ayer. Un día anterior sin marca interrumpe la racha.
- Los récords e hitos se calculan sobre el historial. Borrar un hábito elimina sus marcas y afecta sus puntos. Las cantidades huérfanas pueden conservarse en respaldos, pero no se muestran sin su hábito.
- Los promedios de sueño y entrenamiento usan únicamente días con cantidades registradas. Los gráficos muestran huecos cuando faltan datos.
- Las asociaciones entre sueño y hábitos son descriptivas, no demuestran causalidad.

## Revisión del original y cambios

La estructura original era adecuada para una aplicación personal sin servidor: hábitos por categoría, registros por fecha, perfil, calendario, estadísticas, diario y exportación. Se conservaron estos componentes y el formato de datos para facilitar la transición.

Se corrigieron el registro de fechas futuras desde el diario, la eliminación sin confirmación, la validación débil de JSON, el progreso de rango artificialmente superior a cero, los rangos limitados de sueño, las líneas que unían días sin datos y las equivalencias de horas que presentaban supuestos como resultados. Se retiraron las fuentes remotas para funcionar sin conexión.

Se incorporaron diseño adaptable negro y dorado, colores por categoría, resumen semanal, filtros, búsqueda, fichas e hitos interactivos, cantidades reales configurables, deshacer casillas y carga de archivos JSON. Los rangos son elementos lúdicos de la aplicación, no evaluaciones de salud.

## Límites

- Los datos solo se guardan en ese navegador; no hay sincronización entre dispositivos, autenticación ni almacenamiento remoto. Exporta respaldos periódicos.
- El HTML no incluye los registros de tu navegador original: solo tú puedes exportarlos desde allí.
- Todos los hábitos usan frecuencia diaria. No hay todavía días programados, recordatorios ni archivo de hábitos.
- Las métricas tienen una unidad por hábito; cambiarla no convierte cantidades antiguas. Exporta un respaldo antes de cambiar una unidad usada.
- Esta versión conserva el seguimiento personal original; puedes retirar de la lista cualquier hábito que no tenga sentido para tus objetivos.

## Publicar

Sube `index.html` a la raíz de tu repositorio y usa GitHub Pages como en la versión anterior. Mantén la misma dirección para facilitar la continuidad de almacenamiento. Si cambias de dominio, navegador o dispositivo, utiliza exportar/importar.

## Validación realizada

Probado en Chromium con tamaños de escritorio y móvil (390 px), sin errores de JavaScript y sin desbordamiento horizontal de la página. Se revisaron visualmente el panel y las fichas. Se comprobaron registro diario, persistencia al recargar, métricas y sumas, búsqueda y filtros, cambio de sección, bloqueo de días futuros, importación inválida, migración del formato anterior, respaldo de ida y vuelta, rachas con días anteriores, deshacer y distinción entre cero y dato ausente. La cuadrícula y los gráficos pueden desplazarse horizontalmente dentro de sus propios paneles en móvil.
