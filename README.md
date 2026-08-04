# 🩺 MYCI — Plataforma de Estudio (UPAO · Medicina Humana)

App web para acompañarte durante **toda** la carrera de Medicina Humana, no solo un ciclo puntual: sube el sílabo de cada curso, arma el plan de estudio por semana, lleva tus notas ponderadas y sigue tu avance por los 14 ciclos de la malla curricular. Sirve para cualquier estudiante en cualquier ciclo — cada cuenta elige el suyo al crearse.

## 📲 Cómo publicarla en GitHub Pages

1. Crea un repositorio nuevo en GitHub (o usa uno existente).
2. Sube el archivo **`index.html`**.
3. Ve a **Settings → Pages** → rama `main`, carpeta `/ (root)`.
4. En 1-2 minutos: `https://TU-USUARIO.github.io/TU-REPO/`

## ✨ Cómo funciona

**1. Inicia sesión**
- La app tiene login multiusuario: cada cuenta guarda sus propios datos, totalmente separados de las demás, y sincronizados en la nube por cuenta (ver más abajo).
- Crear una cuenta nueva requiere una clave maestra (solo la conoce el administrador de la app) y elegir **en qué ciclo vas** (I al internado) — la app arma automáticamente los cursos oficiales de ese ciclo, no siempre los mismos.

**2. Mi Camino — ubica tu ciclo en la carrera**
- Un mapa tipo videojuego con los 14 ciclos de la malla curricular oficial de Medicina Humana (362 créditos en total): completados, el actual y los que faltan, con sus cursos y créditos.
- Al cambiar de ciclo, los cursos del home se actualizan solos según la malla — puedes agregarlos o quitarlos, pero siempre eligiéndolos de la malla oficial, no con texto libre.
- Cada cuenta sigue su propio avance de forma independiente: sirve igual para alguien en Ciclo II que para alguien en Ciclo XII.

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

Todo se guarda primero en el **almacenamiento local de tu navegador** (localStorage), por cuenta — la app funciona igual con o sin internet. Además, cada cuenta sincroniza en la nube (Firebase) ligada a tu usuario/contraseña:

- ✅ Funciona **sin internet**: sigue guardando todo en local aunque no haya conexión, y sincroniza solo cuando la vuelve a haber.
- ✅ **Se sincroniza entre dispositivos y navegadores.** Entrando con el mismo usuario/contraseña desde el celular, la compu, u otro navegador, ves los mismos datos.
- ⚠️ Tus datos quedan guardados en tu cuenta de la app (Firebase), no se comparten con nadie más — solo tú puedes leer/escribir tu propia información (reglas de seguridad por usuario).
- 🔌 Puedes revisar si la nube está conectada con el botón **"Nube"** en el Home (te dice si hay sesión activa y si hubo algún error de sincronización).

**Aun así, usa el botón "⬇ Exportar" de vez en cuando para tener un respaldo local** (descarga un `.json`), por si acaso — y "⬆ Importar" para restaurarlo si lo necesitas.

## 🚀 Próximos pasos (cuando quieras escalar)

Ya tiene backend real (Firebase: Auth + Firestore) para sincronizar cuentas entre dispositivos. Si más adelante quieres:
- Múltiples usuarios reales (compañeros de clase, con sus propios accesos)
- Vender o licenciar la plataforma
- Publicidad / monetización
- Empaquetarla como app Android/iOS (Capacitor/Cordova, reusando el mismo código)

...eso son pasos adicionales sobre lo que ya existe. Avísame cuando quieras dar ese salto y lo planeamos.

---
*MYCI — Hecho para los estudiantes de Medicina Humana, UPAO*
