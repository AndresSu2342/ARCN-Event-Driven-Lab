# Event-Driven Lab: Spring Boot, RabbitMQ y Docker Compose

Este repositorio contiene la solución al laboratorio de creación de microservicios orientados a eventos.

## Arquitectura
- **Producer Service:** Expone una API REST (`/api/messages/send`) para recibir mensajes y publicarlos en RabbitMQ.
- **Consumer Service:** Escucha la cola en RabbitMQ y procesa los mensajes entrantes.
- **RabbitMQ:** Actúa como el Message Broker (intermediario) entre ambos microservicios.

## Pasos Completados
1. ✅ **Configuración del entorno** (Codespaces/Local).
2. ✅ **Creación del Producer-Service** usando Spring Boot, configurando Exchange, Queue y Routing Key.
3. ✅ **Creación del Consumer-Service** con el `RabbitListener` para procesar mensajes.
4. ✅ **Construcción y publicación de Imágenes** a Docker Hub (`andressu2342/producerservice` y `andressu2342/consumerservice`).
5. ✅ **Orquestación con Docker Compose**, creando la red y el entorno (`docker-compose.yml`).
6. ✅ **Ejecución y Pruebas** (Instrucciones abajo).

---

## 🚀 Cómo ejecutar el proyecto (Paso 6)

Dado que tienes todo configurado localmente en tu máquina con Docker Desktop, puedes ejecutarlo directamente en tu terminal.

1. Abre una terminal en la raíz del proyecto (`ARCN-Event-Driven-Lab`).
2. Levanta los contenedores:
   ```bash
   docker compose up -d
   ```
3. Espera unos 30 segundos para que RabbitMQ inicie correctamente. Verifica que los 3 contenedores estén corriendo:
   ```bash
   docker compose ps
   ```

## 📸 Evidencias del Laboratorio

A continuación se presentan las evidencias de la correcta ejecución de los microservicios y el flujo de comunicación a través de RabbitMQ:

### 1. Evidencia de Contenedores Corriendo

<img width="1092" height="456" alt="Image" src="https://github.com/user-attachments/assets/416a5b9f-56c8-461e-9a94-c593fc01b1d6" />

### 2. Evidencia del Envío del Mensaje (Producer)

<img width="1141" height="247" alt="Image" src="https://github.com/user-attachments/assets/7ac211e1-9c4b-49ee-876c-0fd10f16160a" />

### 3. Evidencia de la Recepción del Mensaje (Consumer)

<img width="1109" height="649" alt="Image" src="https://github.com/user-attachments/assets/76f7b3e5-f06d-4589-841f-96ff7da02528" />

### 4. Evidencia de la Interfaz de RabbitMQ

<img width="1545" height="749" alt="Image" src="https://github.com/user-attachments/assets/a8c88967-4e41-4439-96f7-8bcd6aec295b" />