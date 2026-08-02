# 🩺 Clínicas 6to Ciclo — Plataforma de Estudio (UPAO)

App web para gestionar tus cursos clínicos: sube el sílabo en PDF, la app arma automáticamente el plan de estudio por semana, y agregas resúmenes y banco de preguntas para cada una.

## 📲 Cómo publicarla en GitHub Pages

1. Crea un repositorio nuevo en GitHub (ej: `clinicas-6to-ciclo`).
2. Sube el archivo **`index.html`**.
3. Ve a **Settings → Pages** → rama `main`, carpeta `/ (root)`.
4. En 1-2 minutos: `https://TU-USUARIO.github.io/clinicas-6to-ciclo/`

## ✨ Cómo funciona

**1. Sube el sílabo de cada curso**
- Entra al curso → "Subir sílabo" → selecciona el PDF.
- La app lee el texto del PDF **directamente en tu navegador** (no se sube a ningún servidor).
- Detecta automáticamente semanas, temas y exámenes buscando patrones como "SEMANA 5", "Tema 1:", "Examen Parcial".

**2. Revisa y ajusta**
- La detección automática no es perfecta — cada sílabo se redacta distinto.
- Te muestra una pantalla para **corregir/completar** antes de guardar: agregar, quitar o editar semanas, temas y marcar exámenes.

**3. Por cada semana:**
- 📝 **Resumen** — escribe o pega tus apuntes.
- 📚 **Banco de preguntas** — agrega preguntas de opción múltiple (con explicación) y practica en modo quiz.

## ⚠️ Importante: dónde se guardan tus datos

Todo se guarda en el **almacenamiento local de tu navegador** (localStorage). Esto significa:

- ✅ Funciona **sin internet** una vez cargada la página.
- ✅ Tus datos **no se envían a ningún servidor** — privacidad total.
- ⚠️ **No se sincroniza entre dispositivos.** Si usas el celular y la compu, son datos separados.
- ⚠️ Si **borras el caché del navegador**, pierdes los datos.

**Por eso: usa el botón "⬇ Exportar" seguido para respaldar tus datos** (descarga un `.json`), y "⬆ Importar" para restaurarlos o pasarlos a otro dispositivo/navegador.

## 🚀 Próximos pasos (cuando quieras escalar)

Esta es la versión 1 (sin backend, sin login, de uso personal). Si más adelante quieres:
- Sincronizar entre dispositivos
- Múltiples usuarios (compañeros de clase)
- Vender o licenciar la plataforma
- Publicidad / monetización

...eso requiere una segunda fase con **backend real** (base de datos, autenticación, servidor). Avísame cuando quieras dar ese salto y lo planeamos.

---
*Hecho para José · Facultad de Medicina Humana, UPAO*
