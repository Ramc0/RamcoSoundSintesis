# RamcoSoundSintesis
---

# 🎵 RamcoSoundSintesis — Motor Visual de Síntesis Sonora

## 📌 Descripción general

**RamcoSoundSintesis** es un motor interactivo de generación de sonido sintético basado en **Web Audio API** y renderizado visual en **HTML5 Canvas**.

El proyecto combina:

* Física básica (colisiones y rebotes)
* Generación procedural de notas musicales
* Escalas dinámicas
* Armonización automática
* Interacción en tiempo real

El sistema permite lanzar bolas dentro de dos círculos (registro grave y agudo).
Cada rebote genera sonido según:

* Escala seleccionada
* Tonalidad
* Tipo de onda
* Modo armónico

El resultado es un entorno audiovisual generativo donde la física produce música.

---

## 🎯 Objetivo del proyecto

Este proyecto nace como evolución de una práctica académica sobre síntesis de sonido.

El objetivo ha sido:

* Expandir funcionalidad original
* Mejorar la interfaz visual
* Añadir motor armónico dinámico
* Implementar colisiones entre objetos
* Optimizar el código eliminando redundancias
* Aplicar buenas prácticas de estructuración

Se trata de un ejercicio de segundo curso donde la modificación funcional tiene gran peso evaluativo.

---

## 🧠 Filosofía del proyecto

RamcoSoundSintesis se basa en los siguientes principios:

* 🎵 La física genera música
* 🎨 La visualización refuerza la experiencia sonora
* ⚙️ El código debe ser claro y modular
* 🔊 La síntesis debe ser completamente generada por la computadora
* 🧩 Las modificaciones deben tener impacto real en la lógica

No se utilizan samples ni archivos de audio:
todo el sonido se genera mediante osciladores del navegador.

---

## 🏗 Arquitectura técnica

El sistema se compone de cuatro bloques principales:

### 1️⃣ Motor Visual (Canvas)

* Renderizado de círculos musicales
* Renderizado de bolas dinámicas
* Efecto glow
* Motion blur
* Previsualización de trayectoria al arrastrar

---

### 2️⃣ Motor Físico

* Rebote contra circunferencia
* Cálculo de normales
* Reflexión vectorial
* Colisiones elásticas entre bolas
* Separación para evitar solapamiento

---

### 3️⃣ Motor Musical

* Escalas dinámicas (Mayor, Menor, Pentatónica)
* Tonalidad seleccionable
* Generación de notas vía MIDI
* Conversión MIDI → frecuencia
* Registro grave y agudo

---

### 4️⃣ Motor de Síntesis

Implementado mediante **Web Audio API**:

* OscillatorNode
* GainNode con envolvente exponencial
* Control dinámico de ganancia según número de osciladores activos
* Selección de forma de onda:

  * Seno
  * Cuadrada
  * Triangular
  * Sierra

---

## 🎛 Controles disponibles

La interfaz permite modificar en tiempo real:

| Control      | Función                         |
| ------------ | ------------------------------- |
| Escala       | Cambia los intervalos musicales |
| Tonalidad    | Cambia la raíz (nota base)      |
| Onda         | Tipo de oscilador               |
| Armonía      | Genera acordes automáticos      |
| Borrar bolas | Reinicia la simulación          |

---

## 🎶 Modos armónicos

El sistema soporta:

* Nota simple
* Quinta justa
* Acorde mayor
* Acorde menor

Cada rebote puede generar múltiples osciladores simultáneamente.

---

## ⚙️ Funcionamiento

1. El usuario hace clic dentro de un círculo.
2. Arrastra el ratón para definir dirección y fuerza.
3. Se genera una bola con velocidad inicial.
4. Cada colisión:

   * Calcula el arco correspondiente
   * Obtiene nota según escala actual
   * Ejecuta síntesis sonora
5. Las bolas también colisionan entre sí generando sonido adicional.

---

## 📁 Estructura del proyecto

```
RamcoSoundSintesis/
│
├── RamcoSoundSintesis.html
└── README.md
```

El proyecto no requiere backend ni dependencias externas.

---

## ▶️ Ejecución

Solo es necesario abrir el archivo:

```
RamcoSoundSintesis.html
```

O ejecutarlo con Live Server si se desea.

No requiere instalación.

---

## 💻 Tecnologías utilizadas

* HTML5
* CSS3
* JavaScript
* Canvas API
* Web Audio API

---

## 🧪 Características técnicas destacables

✔ Escalas generadas dinámicamente
✔ Separación lógica entre motor visual y motor musical
✔ Gestión de múltiples osciladores simultáneos
✔ Control dinámico de ganancia
✔ Colisiones físicas realistas simplificadas
✔ Código optimizado sin estructuras innecesarias

---

## 📈 Mejoras implementadas respecto al ejercicio base

* Sistema de escalas dinámicas
* Selector de tonalidad
* Selector de forma de onda
* Sistema de armonización
* Colisión entre bolas
* Botón de limpieza global
* Interfaz rediseñada
* Eliminación de código redundante
* Optimización de renderizado

---

## 📚 Finalidad educativa

Este proyecto demuestra:

* Comprensión de síntesis sonora digital
* Uso de Web Audio API
* Programación orientada a eventos
* Matemática aplicada (vectores y colisiones)
* Diseño interactivo

---

## 🚀 Posibles extensiones futuras

* Control de tempo global
* Modo secuenciador
* Exportación MIDI
* Control ADSR completo
* Cambio de tamaño de bolas según velocidad
* Sistema de presets
* Guardado de composiciones

---

## 👨‍💻 Autoría

Proyecto académico desarrollado como desarrollado como práctica del módulo de Programación Multimedia.

---
