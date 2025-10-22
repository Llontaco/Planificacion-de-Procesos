# 🧠 Planificación de Procesos en Sistemas Operativos

## 📚 Descripción General

Este proyecto implementa y analiza distintos **algoritmos de planificación de procesos** en sistemas operativos, incluyendo:

- **FCFS (First Come, First Served)**
- **SJF (Shortest Job First)**
- **Round Robin (RR)**
- **Prioridad (estática y dinámica con envejecimiento)**

El objetivo es **comparar su desempeño** en diversos escenarios simulados mediante métricas clásicas de rendimiento:  
tiempo de retorno, tiempo de espera, tiempo de respuesta, throughput y equidad.

---

## 👥 Autores

- **Andrey Hegel Zafra Venegas**  
- **Estefano Alexis Ramírez García**  
- **Henry Alessandro Llontop Falcón**  
- **Maleck Ramírez Álvarez**  
- **Luis Quispe Alvarado**

---

## 🧩 Objetivos del Proyecto

- Implementar los principales algoritmos de planificación de CPU.  
- Simular diferentes escenarios de carga y tipos de procesos.  
- Evaluar métricas de rendimiento bajo condiciones controladas.  
- Visualizar los resultados mediante **tablas comparativas y diagramas de Gantt**.  
- Analizar la eficiencia y equidad de cada política de planificación.

---

## ⚙️ Tecnologías Utilizadas

- **Lenguaje:** Python 🐍  
- **Bibliotecas principales:**
  - `pandas` → manejo de datos y tablas
  - `matplotlib` → gráficos y diagramas de Gantt
  - `copy` → duplicación segura de estructuras de datos
  - `random` → generación de procesos sintéticos

---

## 🧠 Algoritmos Implementados

| Algoritmo | Descripción | Tipo de Política |
|------------|-------------|------------------|
| **FCFS** | Atiende los procesos en el orden de llegada. | No expropiativo |
| **SJF** | Selecciona el proceso con menor duración. | No expropiativo |
| **Round Robin** | Distribuye equitativamente el CPU mediante un *quantum*. | Expropiativo |
| **Prioridad (Estática/Dinámica)** | Asigna prioridades a procesos; la versión dinámica incluye *envejecimiento* para evitar inanición. | Mixto |

---

## 🧪 Escenarios de Prueba

### 🔹 Escenario A – Mezcla de procesos cortos y largos
Evalúa cómo los algoritmos manejan cargas heterogéneas.  
- 5–10 procesos  
- 50% cortos (1–4 unidades), 50% largos (8–20 unidades)

### 🔹 Escenario B – Procesos CPU-bound vs I/O-bound
Analiza equidad y eficiencia con diferentes tipos de procesos.  
- 5 CPU-bound y 5 I/O-bound  
- Llegadas distribuidas en [0,10]

### 🔹 Escenario C – Alta vs baja concurrencia
Evalúa escalabilidad bajo diferentes niveles de carga.  
- Baja concurrencia: 4–6 procesos  
- Alta concurrencia: 20–30 procesos

---

## 📊 Métricas de Evaluación

| Métrica | Descripción |
|----------|-------------|
| **Tiempo de retorno (Turnaround Time)** | Tiempo total desde llegada hasta finalización. |
| **Tiempo de espera (Waiting Time)** | Tiempo en cola antes de ejecución. |
| **Tiempo de respuesta (Response Time)** | Tiempo hasta la primera asignación de CPU. |
| **Throughput** | Número de procesos completados por unidad de tiempo. |
| **Equidad (Fairness)** | Medida de distribución justa de CPU entre procesos. |

---

## 📈 Resultados Destacados

- **SJF** obtuvo los menores tiempos de espera promedio.  
- **Round Robin** logró buena equidad y respuesta consistente.  
- **FCFS** mostró mayor variabilidad y riesgo de inanición.  
- **Prioridad dinámica** equilibró eficiencia y justicia al aplicar envejecimiento.  

---

## 💬 Conclusiones

La comparación de algoritmos mostró que **no existe un único planificador óptimo**, sino que su desempeño depende del tipo de carga y de los objetivos del sistema:

- **SJF** es ideal para cargas predecibles.  
- **Round Robin** es más justo para sistemas interactivos.  
- **Prioridad dinámica** ofrece balance entre rendimiento y equidad.

Como trabajo futuro, se propone **evaluar condiciones totalmente aleatorias** y **diseñar variantes híbridas** que combinen lo mejor de cada enfoque.

---
