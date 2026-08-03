# 🩺 Clínicas — Plataforma de Estudio (UPAO · Medicina Humana)

App web para acompañarte durante toda la carrera de Medicina Humana: sube el sílabo de cada curso, arma el plan de estudio por semana, lleva tus notas ponderadas y sigue tu avance por los 14 ciclos de la malla curricular.

## 📲 Cómo publicarla en GitHub Pages

1. Crea un repositorio nuevo en GitHub (o usa uno existente).
2. Sube el archivo **`index.html`**.
3. Ve a **Settings → Pages** → rama `main`, carpeta `/ (root)`.
4. En 1-2 minutos: `https://TU-USUARIO.github.io/TU-REPO/`

## ✨ Cómo funciona

**1. Inicia sesión**
- La app tiene login multiusuario: cada cuenta guarda sus propios datos, totalmente separados de las demás en el mismo dispositivo.
- Crear una cuenta nueva requiere una clave maestra (solo la conoce el administrador de la app).

**2. Mi Camino — ubica tu ciclo en la carrera**
- Un mapa tipo videojuego con los 14 ciclos de la malla curricular oficial de Medicina Humana (362 créditos en total): completados, el actual y los que faltan, con sus cursos y créditos.
- Al cambiar de ciclo, los cursos del home se actualizan solos según la malla — puedes agregarlos o quitarlos, pero siempre eligiéndolos de la malla oficial, no con texto libre.

**3. Sube el sílabo de cada curso**
- Entra al curso → "Subir sílabo" → PDF o Word (.docx).
- La app lee el texto **directamente en tu navegador** (no se sube a ningún servidor).
- Detecta automáticamente semanas, temas y exámenes ("SEMANA 5", "Tema 1:", "Examen Parcial"), y también los **componentes de evaluación** con sus pesos (incluye el formato con subcomponentes de UPAO, ej. "COMP1 7%" con sus "SC1/SC2/SC3").
- La detección automática no es perfecta — siempre te muestra una pantalla para **revisar y corregir** antes de guardar. Si falla, hay una opción de extraer con IA (usando tu propia API key de Anthropic).

**4. Por cada semana**
- 📝 **Resumen** — escribe o pega tus apuntes (o súbeles diapositivas y genera resumen/preguntas con IA).
- 📚 **Banco de preguntas** — preguntas de opción múltiple con explicación, para practicar en modo quiz o repaso espaciado. Se agregan a mano, en lote (pegando texto con formato), o subiendo un PDF/Word con preguntas ya hechas para que la IA las extraiga (sin inventar nada nuevo).
- 🗺️ **Guía de estudio** — con IA, a partir de tus diapositivas o resumen: qué debes saber sí o sí antes de la clase, y un repaso de refuerzo para después.

**5. Notas y evaluación**
- Los componentes de evaluación (y sus subcomponentes, si el sílabo los trae) quedan armados como un menú: solo escribes la calificación en cada casillero.
- El promedio se calcula solo, respetando los pesos de cada nivel, y se ve como nota final ponderada del curso (con aviso de qué tan aprobatoria es).

**6. Progreso y repaso**
- Repaso espaciado (estilo Anki) para el banco de preguntas de todos tus cursos.
- Simulacros de examen por curso, por examen específico (con las semanas que definas) o combinados.
- Estadísticas con racha de estudio, aciertos recientes y nota final por curso.

**7. Modo oscuro**
- Sigue automáticamente el tema de tu sistema/navegador (`prefers-color-scheme`), sin necesidad de configurarlo.

## ⚠️ Importante: dónde se guardan tus datos

Todo se guarda en el **almacenamiento local de tu navegador** (localStorage), por cuenta. Esto significa:

- ✅ Funciona **sin internet** una vez cargada la página.
- ✅ Tus datos **no se envían a ningún servidor** — privacidad total.
- ⚠️ **No se sincroniza entre dispositivos ni navegadores.** Si usas el celular y la compu (o el link normal y el ícono de "agregar a pantalla de inicio"), son almacenamientos separados.
- ⚠️ Si **borras el caché del navegador**, pierdes los datos.

**Por eso: usa el botón "⬇ Exportar" seguido para respaldar tus datos** (descarga un `.json`), y "⬆ Importar" para restaurarlos o pasarlos a otro dispositivo/navegador.

## 🚀 Próximos pasos (cuando quieras escalar)

Esta sigue siendo una app sin backend (localStorage + login local). Si más adelante quieres:
- Sincronizar entre dispositivos
- Múltiples usuarios reales (compañeros de clase, con sus propios accesos)
- Vender o licenciar la plataforma
- Publicidad / monetización

...eso requiere una segunda fase con **backend real** (base de datos, autenticación, servidor). Avísame cuando quieras dar ese salto y lo planeamos.

---
*Hecho para José · Facultad de Medicina Humana, UPAO*
