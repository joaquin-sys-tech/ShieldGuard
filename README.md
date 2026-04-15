# 🛡️ ShieldGuard


<p align="center">
  <a href="https://shieldguard.app">
    <img src="https://img.shields.io/badge/Web-ShieldGuard-blue?style=for-the-badge&logo=google-chrome&logoColor=white" />
  </a>
</p>

**ShieldGuard** es un bot de moderación avanzado para Discord enfocado en la protección contra raids, spam y acciones maliciosas dentro de servidores.

Está diseñado para ser **ligero, configurable y automático**, permitiendo a los administradores mantener el control sin intervención constante.
---
## 🌐 Página web

Visita la web oficial para más información y futuras funcionalidades:

👉 https://shieldguard.app

---

## 🚀 Características principales

### 🔒 Anti-Raid

* Detección de múltiples usuarios entrando en un corto periodo de tiempo
* Activación automática de modo protección
* Control de cuentas nuevas (edad mínima configurable)

### 🛑 Anti-Spam

* Detección de mensajes repetitivos o flooding
* Sistema basado en umbral de mensajes por tiempo
* Sanciones automáticas configurables

### 🔗 Anti-Link

* Bloqueo de enlaces no permitidos
* Sistema de whitelist por roles

### 📣 Anti-Mentions

* Prevención de abuso de menciones
* Límite configurable de menciones por mensaje

### 💥 Anti-Nuke

* Protección contra acciones masivas como:

  * Baneos
  * Kicks
  * Eliminación de canales
* Detección por actividad anormal en intervalos de tiempo

### 📜 Sistema de Logs

* Registro de eventos importantes
* Canal configurable para auditoría

---

## 🧠 Risk Engine (Motor de Evaluación de Riesgo)

ShieldGuard incorpora un sistema interno de evaluación denominado **Risk Engine**, encargado de analizar el comportamiento de los usuarios en tiempo real y determinar su nivel de riesgo dentro del servidor.

Este sistema permite una **moderación adaptativa**, reaccionando de forma proporcional según el contexto y la actividad detectada.

---

### 🔍 ¿Cómo funciona?

El Risk Engine utiliza un modelo basado en:

* **Eventos** (mensajes, joins, acciones)
* **Frecuencia** (actividad en ventanas de tiempo)
* **Contexto** (tipo de acción y entorno)
* **Historial reciente del usuario**

Cada evento relevante contribuye a una **puntuación dinámica de riesgo**, que se ajusta continuamente.

---

### ⚙️ Señales analizadas

El sistema tiene en cuenta múltiples indicadores, incluyendo:

#### 📥 Actividad de entrada

* Frecuencia de nuevos usuarios en el servidor
* Edad de las cuentas
* Patrones de entrada simultánea

#### 💬 Comportamiento en mensajes

* Velocidad de envío
* Repetición de contenido
* Uso de menciones masivas
* Presencia de enlaces

#### ⚡ Acciones sensibles

* Eliminación de canales
* Baneos/kicks en masa
* Cambios administrativos rápidos

#### 🔁 Patrones temporales

* Actividad concentrada en ventanas cortas
* Cambios bruscos en comportamiento

---

### 📊 Evaluación de riesgo

* Cada usuario tiene un **estado de riesgo temporal**
* La puntuación:

  * **Aumenta** ante comportamientos sospechosos
  * **Disminuye gradualmente** con el tiempo (decay)

> Esto evita penalizar permanentemente a usuarios legítimos.

---

### 🚨 Respuesta automática

Cuando se superan ciertos umbrales internos, ShieldGuard puede ejecutar acciones como:

* Aplicar restricciones temporales
* Silenciar (mute) automáticamente
* Expulsar (kick)
* Banear en casos extremos
* Activar modo anti-raid global

Las acciones dependen de:

* Nivel de riesgo acumulado
* Tipo de comportamiento detectado
* Configuración del servidor

---

### 🧩 Integración con sistemas existentes

El Risk Engine actúa como una capa superior que coordina:

* Anti-Spam
* Anti-Raid
* Anti-Link
* Anti-Nuke

Esto permite:

* Evitar duplicación de lógica
* Tomar decisiones más inteligentes
* Reducir falsos positivos

---

### 🔐 Seguridad del sistema

Para prevenir abusos o evasiones:

* No se exponen:

  * Pesos de evaluación
  * Umbrales exactos
  * Lógica interna detallada

* El sistema:

  * No depende de una única señal
  * Correlaciona múltiples eventos
  * Está diseñado para resistir evasión básica

---

### 🔄 Decaimiento de riesgo (Decay)

* El riesgo disminuye automáticamente con el tiempo
* Se reinicia tras periodos de inactividad
* Permite recuperación de usuarios legítimos

---

## 🧠 Arquitectura

* Basado en **discord.py**
* Sistema modular por eventos
* Configuración persistente por servidor
* Uso de estructuras eficientes para detección en tiempo real

---

## 🔐 Seguridad

* No se expone lógica crítica
* No se almacenan credenciales en el código
* Diseñado para minimizar vectores de evasión

---

## ⚠️ Notas

* Algunas funciones requieren permisos elevados
* Se recomienda:

  * Gestionar mensajes
  * Expulsar miembros
  * Banear miembros


---

## 🧾 Licencia

MIT License

---

## 🔮 Futuro

* Mejora continua del Risk Engine
* Panel web de administración
* Métricas avanzadas
* Integración con sistemas inteligentes

---

## 🛡️ ShieldGuard

> Protección automática, configurable y eficiente para comunidades de Discord.
