# 🏋️ TimerGym

**Timer de descanso simple y rápido para entrenamiento de gimnasio.**

TimerGym nace con una idea central: durante el entrenamiento, iniciar, pausar y ajustar un descanso debería requerir la menor cantidad posible de atención.

## 🎯 Objetivo

Crear un timer de descanso **rápido, visual y fácil de usar desde el celular**, pensado específicamente para utilizar durante una sesión de gimnasio.

La primera versión prioriza:

* Simplicidad
* Lectura rápida
* Botones grandes
* Uso con una sola mano
* Feedback visual inmediato
* Cero configuraciones innecesarias

---

## 🚀 MVP — v1.0

La versión inicial incluye:

* ⏱️ Timer de descanso de 90 segundos
* 🟢 Botón único para **Iniciar / Pausar / Continuar**
* ➕ Botón **+30 segundos**
* ➖ Botón **−30 segundos**
* 🔄 Botón **Reiniciar**
* ⚡ Barra visual de progreso
* 🚨 Alerta visual tipo flash al llegar a `00:00`
* 📱 Diseño responsive para celulares
* 🌐 Publicación mediante GitHub Pages

---

## 🧠 Lógica de funcionamiento

### Estados del timer

```text
DETENIDO
   │
   ▼
INICIAR
   │
   ▼
CORRIENDO
   │
   ├── PAUSAR
   │      │
   │      ▼
   │   PAUSADO
   │      │
   │      ├── CONTINUAR
   │      │
   │      └── REINICIAR
   │
   ▼
00:00
   │
   ▼
ALERTA
```

### Ajuste de tiempo

`+30` agrega 30 segundos al tiempo actual.

`−30` resta 30 segundos, sin permitir valores inferiores a `00:00`.

---

## 🛠️ Tecnologías

Actualmente TimerGym está construido utilizando:

* HTML5
* CSS3
* JavaScript
* Git
* GitHub
* GitHub Pages

No utiliza frameworks ni dependencias externas.

La intención en esta etapa es mantener el proyecto **simple y fácil de modificar**.

---

# 🚀 Versión 2 — Roadmap

La versión 2 buscará mejorar la experiencia de uso sin perder la simplicidad del MVP.

### Funciones previstas

* 🔒 **Screen Wake Lock**

  * Mantener la pantalla encendida mientras el timer está activo.

* ⏱️ **Timer basado en tiempo real**

  * Utilizar timestamps para mejorar la precisión.
  * Evitar depender exclusivamente de `setInterval()`.

* 🔊 **Alerta sonora**

  * Sonido al finalizar el descanso.

* 📳 **Vibración**

  * Feedback háptico en dispositivos compatibles.

* ⚙️ **Duración configurable**

  * Permitir seleccionar diferentes tiempos de descanso.

* 💾 **Persistencia de configuración**

  * Recordar la duración preferida.

* 📲 **PWA**

  * Instalar TimerGym en la pantalla de inicio.
  * Icono propio.
  * Experiencia similar a una aplicación nativa.

---

# 🔮 Visión futura

TimerGym puede evolucionar desde un simple cronómetro hacia un **asistente de entrenamiento minimalista**.

Concepto:

```text
EJERCICIO
    ↓
SERIE
    ↓
DESCANSO
    ↓
PRÓXIMA ACCIÓN
    ↓
SERIE
    ↓
DESCANSO
```

La idea es que la aplicación no solamente mida el descanso, sino que eventualmente pueda indicar **cuál es el próximo paso del entrenamiento**.

---

## 📁 Estructura actual

Actualmente el proyecto es deliberadamente simple:

```text
TimerGym/
│
├── index.html
└── README.md
```

En futuras versiones podría evolucionar hacia:

```text
TimerGym/
│
├── index.html
├── style.css
├── app.js
├── manifest.json
├── service-worker.js
│
├── assets/
│   ├── icons/
│   └── sounds/
│
└── README.md
```

---

## 📌 Versionado

El proyecto utiliza versiones para registrar su evolución:

```text
v1.0.0 — MVP inicial
v1.1.0 — Ajustes y mejoras menores
v2.0.0 — Nuevas funcionalidades
v3.0.0 — Evolución del concepto
```

Git se utiliza para mantener el historial de cambios y permitir volver a versiones anteriores cuando sea necesario.

---

## 📄 Estado del proyecto

**Estado:** 🚧 En desarrollo

**Versión actual:** `v1.0 — MVP`

**Próximo objetivo:** `v2.0`

---

## 💡 Principio del proyecto

> **Menos interacción. Más entrenamiento.**

TimerGym debe desaparecer durante el entrenamiento y aparecer únicamente cuando hace falta.

---

## 📜 Licencia

Proyecto en desarrollo.

La licencia definitiva será definida en una versión posterior.
