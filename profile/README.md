# ✈️ Vektor AI

<div align="center">
  
<img width="300" height="300" alt="Vektor AI - Logo" src="https://github.com/user-attachments/assets/ab1b9eb5-94c1-4b2b-9ea5-6a6a97e00a11" />

# FlightOnTime - Sistema de Predicción de Puntualidad de Vuelos

![FlightOnTime](https://img.shields.io/badge/FlightOnTime-v1.0.0-blue)
![Java](https://img.shields.io/badge/Java-17-orange)
![Python](https://img.shields.io/badge/Python-3.11-green)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.1-brightgreen)
![FastAPI](https://img.shields.io/badge/FastAPI-0.109-teal)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue)
![Docker](https://img.shields.io/badge/Docker-Compose-blue)

Proyecto desarrollado para el Hackathon Oracle ONE + Alura LATAM - NoCountry

[![GitHub](https://img.shields.io/badge/GitHub-Vektor--AI-blue?style=flat&logo=github)](https://github.com/VektorAI-Equipo71)
[![Hackathon](https://img.shields.io/badge/Hackathon-Oracle%20ONE-orange?style=flat)](https://www.oracle.com/latam/education/oracle-next-education/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

[App en linea](http://159.54.159.244/) · [Video de YouTube](https://www.youtube.com/watch?v=Vxq--ZCVTao) · [Documentación](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/docs) · [Landing page - VerktorAI](https://josebenin82.github.io/landing-vektor-ai/)

</div>

---

## 🎯 Sobre el Proyecto

**Vektor AI** es una solución integral para predecir retrasos de vuelos utilizando Machine Learning. El sistema analiza datos históricos de vuelos, información meteorológica en tiempo real y características temporales para proporcionar predicciones precisas y confiables.

### 💡 ¿Por qué importa?

- 🛫 **20%** de los vuelos en USA sufren retrasos
- 💰 **$33 mil millones** en costos anuales por retrasos
- ⏱️ **145 millones** de horas perdidas por pasajeros
- 🎯 **79% accuracy** de nuestro modelo ayuda a mitigar esto

### 🌟 Características Principales

- 🤖 **Machine Learning** con modelo Random Forest entrenado
- 🌤️ **Datos meteorológicos en tiempo real** vía OpenWeatherMap API
- 📏 **Cálculo automático de distancias** usando fórmula de Haversine
- 🏢 **Arquitectura de microservicios** con Java Spring Boot y Python FastAPI
- 🎨 **Frontend moderno** estilo Oracle Redwood
- 💾 **Persistencia PostgreSQL** para historial y estadísticas
- 📊 **Dashboard de estadísticas** con gráficas interactivas
- 📦 **Procesamiento por lotes** mediante archivos CSV

---

## 🌐 Acceso al Sistema

### 🚀 Entorno de Producción

El sistema está desplegado y disponible en:

**🔗 URL de Producción**: [http://159.54.159.244/index.html](http://159.54.159.244/index.html)

> 🌟 Accede directamente a la aplicación en producción para probar todas las funcionalidades del sistema.

---

## 🎥 Demo

### Vista Previa de la Aplicación

<div align="center">

<img width="300" height="300" alt="Dashboard-1" src=https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/images/dashboard-preview1.png/>   <img width="300" height="300" alt="Dashboard-1" src=https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/images/dashboard-preview3.png/>

*Dashboard principal con gestion completa y predicción en tiempo real*

<img width="300" height="300" alt="Dashboard-1" src=https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/images/stats.png/>    <img width="300" height="300" alt="Dashboard-1" src=https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/images/batch-preview.png/>

*(1) Dashboard de estadísticas y analytics e (2) Interfaz de predicción por lotes (CSV)*

</div>

### 🎬 Video Demo

> ▶️ Click en la imagen para ver el demo completo
<p align="center">
  <a href="https://www.youtube.com/watch?v=Vxq--ZCVTao">
    <img src="https://img.youtube.com/vi/Vxq--ZCVTao/maxresdefault.jpg" width="600">
  </a>
</p>

**Duración:** 07:44 | **Idioma:** Español

---

## ⚡ Quick Start (5 minutos)

### Opción 1: Docker Compose (Recomendado)
```bash
# 1. Clonar repositorio
git clone https://github.com/VektorAI-Equipo71/vektor-ai.git
cd vektor-ai

# 2. Descargar modelo ML (obligatorio)
# Descargar desde: https://drive.google.com/file/d/1queVcz3SF7OzxB6B92lmlzKv9X4tbJnH/view
# Mover a: ml-service/random_forest_clima_v1.joblib

# 3. Crear .env
echo 'OPENWEATHER_API_KEY=tu_api_key' > .env

# 4. Iniciar
docker compose up -d

# 5. Abrir navegador
open http://localhost:8081
```

### Opción 2: Deploy en OCI

Ver guía completa en [docs/MANUAL-DESPLIEGUE-OCI.pdf](https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/MANUAL-DESPLIEGUE-OCI.pdf)

---

## 👥 Equipo

### 🎯 Product Owner
- **[Kevin Joel Lemos](https://www.linkedin.com/in/kevin-joel-lemos-583845219/)** - [@niveKJ](https://github.com/niveKJ)

### 📊 Scrum Master
- **[Gloria Carolina Guerrero Velandia](https://www.linkedin.com/in/gloria-carolina-guerrero-velandia)** - [@CarolinaG2024](https://github.com/CarolinaG2024)

### 🤖 Data Science Team
- **Líder Técnico DS:** [Sofía Martínez Véjar](https://www.linkedin.com/in/spmv1980) - [@smv1980](https://github.com/smv1980)
- **Data Scientists:**
  - [Karen Brenes](https://www.linkedin.com/in/karen-brenes-c/),- [@Karen-13C](https://github.com/Karen-13C)
  - [Miguel Baillon](https://www.linkedin.com/in/miguel-baillon-opazo-738b5487) - [@MPBOga](https://github.com/MPBOga)
  - [Ronald Varela](https://www.linkedin.com/in/ronaldvarelam) - [@Ronaldvarela852](https://github.com/Ronaldvarela852)
  - [Gloria Carolina Guerrero Velandia](https://www.linkedin.com/in/gloria-carolina-guerrero-velandia) - [@CarolinaG2024](https://github.com/CarolinaG2024)
  - [Cristian Camilo Maje](https://www.linkedin.com/in/camilo-montenegro-) - [@CamiloTrr](https://github.com/CamiloTrr)
  - [Kevin Lemos](https://www.linkedin.com/in/kevin-joel-lemos-583845219/) - [@niveKJ](https://github.com/niveKJ)
 
### ⚙️ FullStack Team
- **Líder Técnico Backend & Fontend:** [Edgar Alejandro Nestor Castillo](https://www.linkedin.com/in/edgar-nestor-75090b272/) - [@EdgarNestorC](https://github.com/EdgarNestorC)
- **Desarrollador FullStack:** [Jose Julio Rodriguez Benito](https://www.linkedin.com/in/julius-benito/) - [@JoseBenin82](https://github.com/JoseBenin82)

---

## 🏗️ Arquitectura del Sistema

```
┌─────────────────┐      ┌──────────────────┐      ┌─────────────────┐
│                 │      │                  │      │                 │
│   Frontend      │─────▶│   Backend API   │─────▶│   ML Service    │
│  (HTML+CSS+JS)  │      │   (Spring Boot)  │      │   (FastAPI)     │
│   Nginx 80      │      │   Port 8080      │      │   Port 8001     │
│                 │      │                  │      │                 │
└─────────────────┘      └────────┬─────────┘      └────────┬────────┘
                                  │                          │
                                  │                          │
                                  ▼                          ▼
                          ┌──────────────┐         ┌─────────────────┐
                          │              │         │                 │
                          │  PostgreSQL  │         │ OpenWeatherMap  │
                          │   Database   │         │      API        │
                          │              │         │                 │
                          └──────────────┘         └─────────────────┘
```

## 🚀 Stack Tecnológico

### Machine Learning
- **Lenguaje:** Python 3.11
- **Framework:** FastAPI
- **ML Library:** scikit-learn
- **Procesamiento:** pandas, numpy
- **Modelo:** RandomForestClassifier (98 árboles)

### Backend
- **Lenguaje:** Java 17
- **Framework:** Spring Boot 3.2.1
- **Build Tool:** Maven
- **Base de Datos:** PostgreSQL
- **API Externa:** OpenWeatherMap

### Frontend
- HTML5 + CSS3 + Vanilla JavaScript ES6+
- Nginx para servir estáticos
- Chart.js (gráficas), SheetJS (Excel)
- i18n manual (ES/EN), conversión unidades
- HTML puro con Fetch API

### Infraestructura
- **Cloud:** Oracle Cloud Infrastructure (OCI)
- **Containerización:** Docker
- **Orquestación:** Docker Compose
- **CI/CD:** GitHub Actions
- **Monitoreo:** Prometheus + Grafana (opcional)

---

## 🎓 Modelo de Machine Learning

### Especificaciones Técnicas

| Característica | Valor |
|---------------|-------|
| **Tipo de Modelo** | RandomForestClassifier |
| **Número de Árboles** | 98 |
| **Profundidad Máxima** | 22 |
| **Features** | 20 características |
| **Cantidad mínima de muestras que debe tener una hoja** | 16 |
| **Mínimo de muestras necesarias para dividir un nodo** | 10 |
| **Clases** | Balanceadas|
| **Máxima cantidad de variables que se consideran en cada división del árbol** | Raíz Cuadrada|

### Features del Modelo (20 en total)

1. **Temporales Cíclicas:** es_fin_de_semana, mes_sin, mes_cos, dia_semana_sin, dia_semana_cos
2. **Temporales Directas:** MONTH, QUARTER, DAY_OF_MONTH.
3. **Categóricas:** OP_UNIQUE_CARRIER, ORIGIN_AIRPORT_ID, DEST_AIRPORT_ID, TAIL_NUM
4. **Horarios:** CRS_DEP_TIME, CRS_ARR_TIME
5. **Climáticas:** temperatura, humedad, presion, visibilidad, viento_velocidad, condicion

Las cinco variables más importantes: CRS_DEP_TIME, CRS_ARR_TIME, humedad, temperatura, presión

### Aerolíneas Soportadas

🛫 **15 Aerolíneas de Estados Unidos:**

| Código | Nombre |
|--------|--------|
| 9E | Endeavor Air |
| AA | American Airlines |
| AS | Alaska Airlines |
| B6 | JetBlue Airways |
| DL | Delta Air Lines |
| F9 | Frontier Airlines |
| G4 | Allegiant Air |
| HA | Hawaiian Airlines |
| MQ | Envoy Air |
| NK | Spirit Airlines |
| OH | PSA Airlines |
| OO | SkyWest Airlines |
| UA | United Airlines |
| WN | Southwest Airlines |
| YX | Republic Airways |

### Cobertura de Aeropuertos

🌐 **397 Aeropuertos** de Estados Unidos

---
## 📊 Resultados y Métricas

### Rendimiento del Modelo

| Métrica | Valor | Target | Status |
|:--------|------:|:------:|:------:|
| **Accuracy** | 79% | >75% | ✅ |
| **Precision (A tiempo)** | 91% | >80% | ✅ |
| **Precision (Retraso)** | 49% | <80% |❌ |
| **Recall (A tiempo)** | 82% | >80% | ✅ |
| **Recall (Retraso)** | 68% | <80% |❌ |
| **F1-Score (A tiempo)** | 86% | >80% | ✅ |
| **F1-Score( Retraso)** | 57% | <80% | ❌ |
| **ROC-AUC** | 84% | >80% | ✅ |

### Rendimiento del Sistema

| Componente | Métrica | Valor |
|:-----------|:--------|------:|
| **API Backend** | Response Time (P95) | <2s |
| **ML Service** | Inferencia | 32ms |
| **Throughput** | Predicciones/seg | 20K |
| **Tests** | Coverage | 75%+ |
| **Cobertura** | Aeropuertos | 397 |
| **Cobertura** | Aerolíneas | 15 |

### Comparación de Modelos

Durante el desarrollo se evaluaron 4 modelos:

| Modelo | Accuracy | Tiempo Entrenamiento | Selección |
|:-------|:--------:|:--------------------:|:---------:|
| Logistic Regression | 60% | ⚡ 5min | ❌ |
| **Random Forest** | **79%** | ⏱️ 45min | ✅ **GANADOR** |
| XGBoost | 76% | 🐌 60min | ❌ |
| LightGBM | Falto RAM| 🐌🐌 90min | ❌ |

**Criterio de selección:** Mejor balance entre rendimiento, precisión y robustez frente a la variabilidad de los datos, manteniendo además una integración sencilla con la arquitectura del sistema.

---

## 📦 Contenido del Proyecto

| Repositorio | Descripción | Stack | Estado |
|------------|-------------|-------|--------|
| [**ML Service**](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/ml-service) | Servicio de Machine Learning | Python, FastAPI, scikit-learn | ✅ Activo |
| [**Backend**](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/backend) | API REST Backend | Java 17, Spring Boot 3.x | ✅ Activo |
| [**Frontend**](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/frontend) | Interfaz de usuario | HTML, CSS, JavaScript, Nginx | ✅ Activo |
| [**Docs**](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/docs) | Documentación técnica | Markdown | ✅ Activo |
| [**Notebooks**](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/notebooks) | Jupyter Notebook, Google Colab | Markdown | ✅ Activo |

---

## 📁 Estructura del Proyecto

```
vektor-ai-backend/
├── backend/                          # Backend Java Spring Boot (Puerto 8080)
│   ├── src/main/java/...             # Código fuente Java
│   ├── src/main/resources/           # Configuración y schema SQL
│   ├── pom.xml                       # Dependencias Maven
│   └── Dockerfile
│
├── ml-service/                       # Servicio ML Python FastAPI (Puerto 8001)
│   ├── main.py                       # Aplicación FastAPI
│   ├── airport_coords.py             # Coordenadas de aeropuertos
│   ├── random_forest_clima_v1.joblib # Modelo ML entrenado
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/                         # Frontend HTML/CSS/JS (Puerto 8081)
│   ├── index.html                    # Dashboard principal
│   ├── batch.html                    # Predicción por lotes
│   ├── history.html                  # Historial
│   ├── stats.html                    # Estadísticas
│   ├── styles.css                    # Estilos
│   ├── app.js                        # Lógica JavaScript
│   └── Dockerfile
│
├── docs/                             # Documentación
│   ├── ARCHITECTURE.md               # Arquitectura del sistema
│   ├── CONTRATO_INTEGRACION.md       # Contrato de integración API
│   ├── MANUAL-DESPLIEGUE-OCI.pdf     # Manual de despliegue en Oracle Cloud
│   └── testing/                      # Guías de pruebas
│
├── postman/                          # Colección Postman
│   ├── FlightOnTime_Postman_Collection.json
│   └── FlightOnTime_Environment.json
│
├── docker-compose.yml                # Orquestación de servicios
├── .env                              # Variables de entorno (crear)
└── README.md                         # Este archivo
```


## 🚀 Cómo Levantar el Sistema en Local (Docker)

### Prerrequisitos

| Herramienta | Versión Mínima | Instalación |
|-------------|----------------|-------------|
| **Docker** | 20.10+ | [docker.com/get-docker](https://www.docker.com/get-docker) |
| **Docker Compose** | 2.0+ | Incluido con Docker Desktop |

> 💡 **Verificar instalación**: Ejecutar `docker --version` y `docker compose version` en terminal

---

### Paso 1: Clonar el Repositorio

```bash
git clone <url-del-repositorio>
cd vektor-ai-backend
```

---

### Paso 2: Configurar Variable de Entorno

Crear un archivo `.env` en la raíz del proyecto con la API Key de OpenWeatherMap:

```env
OPENWEATHER_API_KEY=tu_api_key_aqui
```

> 📝 **Obtener API Key gratuita**: [openweathermap.org/api](https://openweathermap.org/api)

---

### Paso 3: Descargar Modelo ML (⚠️ Importante)

Debido a restricciones de tamaño de GitHub (>100MB), el modelo entrenado no se incluye en el repositorio.

1. **Descargar el archivo** `random_forest_clima_v1.joblib` desde el siguiente enlace:
   
   👉 [**Descargar Modelo ML (Google Drive)**](https://drive.google.com/file/d/1queVcz3SF7OzxB6B92lmlzKv9X4tbJnH/view?usp=drive_link)

2. **Mover el archivo descargado** a la carpeta `ml-service/` dentro del proyecto.

> ❌ **Si omites este paso**, el servicio de Machine Learning fallará al iniciar.

---

### Paso 4: Construir y Levantar los Servicios

```bash
docker compose up --build
```

> ⚠️ **Importante**: Este es el comando principal para levantar el proyecto por primera vez en local.

Este comando:
1. Construye las imágenes de Docker para cada servicio
2. Levanta todos los contenedores
3. Configura la red interna entre servicios
4. Inicializa la base de datos PostgreSQL

---

### Paso 5: Verificar que los Servicios estén Corriendo

Esperar aproximadamente **90 segundos** para que todos los servicios inicien completamente.

#### Tiempos de inicio aproximados:

| Servicio | Tiempo |
|----------|--------|
| PostgreSQL | ~10 segundos |
| ML Service | ~40 segundos (carga del modelo) |
| Backend | ~60 segundos (compilación Maven) |
| Frontend | ~10 segundos |

#### Verificar estado de contenedores:

```bash
docker compose ps
```

**Salida esperada:**
```
NAME                    STATUS
flightontime-postgres   Up (healthy)
flightontime-ml         Up (healthy)
flightontime-backend    Up (healthy)
flightontime-frontend   Up (healthy)
```

---

### Paso 6: Acceder a la Aplicación

Una vez que todos los servicios estén corriendo, acceder a:

| Servicio | URL |
|----------|-----|
| **🌐 Frontend (Aplicación Web)** | http://localhost:8081 |
| **📡 Backend API** | http://localhost:8080/api |
| **🤖 ML Service** | http://localhost:8001 |
| **📊 Métricas Prometheus** | http://localhost:8080/actuator/prometheus |

#### Health Checks:

| Servicio | URL de Health Check |
|----------|---------------------|
| Backend | http://localhost:8080/api/health |
| ML Service | http://localhost:8001/health |

---

## 🐳 Comandos Docker Útiles

### Ver logs de todos los servicios

```bash
docker compose logs -f
```

### Ver logs de un servicio específico

```bash
docker compose logs -f backend
docker compose logs -f ml-service
docker compose logs -f frontend
docker compose logs -f postgres
```

### Detener todos los servicios

```bash
docker compose down
```

### Detener y eliminar volúmenes (reset completo)

```bash
docker compose down -v
```

### Reconstruir un servicio específico

```bash
docker compose up --build backend
```

### Ejecutar en modo detached (segundo plano)

```bash
docker compose up -d --build
```

---

## 🚨 Solución de Problemas

### Error: "Port already in use"

Algún puerto ya está siendo usado por otra aplicación.

**Solución**: Detener el proceso que usa el puerto o modificar los puertos en `docker-compose.yml`

### Error: ML Service no carga el modelo

El archivo del modelo ML es muy grande (~500MB) y puede tardar en cargar. También puede fallar si no descargaste el archivo manualmente.

**Solución**: 
1. Asegúrate de haber completado el **Paso 3** (Descargar Modelo ML).
2. Verifica que el archivo `random_forest_clima_v1.joblib` esté en la carpeta `ml-service/`.
3. Si ya está, espera 40-60 segundos adicionales.

Verificar logs:
```bash
docker compose logs ml-service
```

### Error: Backend no conecta a PostgreSQL

El backend intenta conectarse antes de que PostgreSQL esté listo.

**Solución**: Docker Compose usa health checks para garantizar el orden. Si persiste, reiniciar:
```bash
docker compose down
docker compose up --build
```

### Error: API Key de OpenWeatherMap inválida

Los datos meteorológicos no se obtienen correctamente.

**Solución**: Verificar que el archivo `.env` contenga una API Key válida:
```env
OPENWEATHER_API_KEY=tu_api_key_valida
```

---

## ❓ FAQ (Preguntas Frecuentes)

<details>
<summary><strong>¿Por qué el modelo solo soporta aeropuertos de USA?</strong></summary>

El dataset utilizado proviene del Bureau of Transportation Statistics (BTS) de Estados Unidos, que es la fuente más completa y actualizada de datos de vuelos. Para expandir a otros países, se necesitarían datasets equivalentes con calidad similar.
</details>

<details>
<summary><strong>¿Qué tan preciso es el modelo?</strong></summary>

El modelo tiene un **79% de accuracy** en el conjunto de prueba. Para la clase "retraso" (1.0) el despeño es **49% de precision** y **68% de recall**. Esto significa que:
- 79 de cada 100 predicciones son correctas
- Cuando el modelo predice “retraso”, acierta en el 49% de los casos (precision), es decir, aproximadamente la mitad de las alertas de retraso son verdaderas.
- El modelo detecta el 68% de los retrasos reales (recall), lo que indica una buena capacidad para anticipar retrasos, aunque con presencia de falsos positivos.
Este comportamiento es consistente con un enfoque orientado a no perder retrasos reales, algo deseable en contextos operativos, especialmente considerando que el dataset está desbalanceado y se utilizó class_weight='balanced'.
</details>

<details>
<summary><strong>¿Puedo usar la API en producción?</strong></summary>

El sistema fue desarrollado como MVP para un hackathon. Para uso en producción recomendamos:
- ✅ Implementar autenticación (JWT)
- ✅ Agregar rate limiting
- ✅ Configurar HTTPS
- ✅ Usar caché (Redis)
- ✅ Monitoreo avanzado (Grafana)
</details>

<details>
<summary><strong>¿El modelo se actualiza automáticamente?</strong></summary>

No. El modelo actual está entrenado con datos históricos (Oct 2024 - Sep 2025). Para producción, se recomienda:
- Reentrenamiento mensual con datos frescos
- Pipeline automático de ML (MLOps)
- Validación A/B testing
</details>

<details>
<summary><strong>¿Cuánto cuesta correr esto en la nube?</strong></summary>

**Oracle Cloud Free Tier (usado en el hackathon):**
- VM: 2 OCPU, 12GB RAM → **Gratis** (Always Free)
- Storage: 100GB → **Gratis**
- Network: 10TB/mes → **Gratis**

**Costo estimado fuera del Free Tier:**
- OCI: ~$30-50/mes
- AWS: ~$50-80/mes
- GCP: ~$40-70/mes
</details>

---

## 📊 Flujo de Predicción

```
1. Usuario ingresa datos del vuelo
   ├─ Aerolínea (ej: "DL" - Delta)
   ├─ Origen (ej: "ATL" - Atlanta)
   ├─ Destino (ej: "JFK" - New York)
   └─ Fecha/hora de partida
   
2. Frontend envía request al Backend
   
3. Backend valida y normaliza datos
   ├─ Validación de campos requeridos
   ├─ Verificación de aerolínea válida
   └─ Normalización a mayúsculas
   
4. Backend llama al ML Service
   
5. ML Service procesa la predicción
   ├─ Calcula distancia (Haversine)
   ├─ Consulta clima en tiempo real
   ├─ Prepara 15 features
   ├─ Aplica encoders
   └─ Ejecuta modelo RandomForest
   
6. Resultado retorna al usuario
   ├─ Predicción: Puntual / Retrasado
   ├─ Probabilidad de retraso (0-1)
   ├─ Confianza del modelo (0-1)
   ├─ Distancia del vuelo
   └─ Información meteorológica
```

---

## 🧪 Probar la API

### Predicción Individual

```bash
curl -X POST http://localhost:8080/api/predict \
  -H "Content-Type: application/json" \
  -d '{
    "aerolinea": "DL",
    "origen": "ATL",
    "destino": "JFK",
    "fecha_partida": "2026-01-15T14:30:00"
  }'
```

### Health Check

```bash
curl http://localhost:8080/api/health
```

---

## 📡 Endpoints Principales

### Backend API (http://localhost:8080)

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| POST | `/api/predict` | Predicción individual de vuelo |
| POST | `/api/batch-predict` | Predicción por lotes (CSV) |
| GET | `/api/predictions` | Consultar historial con paginación |
| GET | `/api/stats` | Estadísticas agregadas |
| GET | `/api/health` | Health check |
| GET | `/api/docs` | Documentación de API |

### ML Service (http://localhost:8001)

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| POST | `/predict_internal` | Predicción ML interna |
| GET | `/airports` | Lista de aeropuertos |
| GET | `/health` | Health check |

---

## 📚 Documentación

- **[ARCHITECTURE.md](https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/ARCHITECTURE.md)** - Arquitectura del sistema
- **[CONTRATO_INTEGRACION.md](https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/CONTRATO_INTEGRACION.md)** - Contrato de integración API
- **[GUIA_PRUEBAS.md](https://github.com/VektorAI-Equipo71/vektor-ai/blob/main/docs/testing/GUIA_PRUEBAS.md)** - Guía de pruebas
- **[Colección Postman](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/postman)** - Colección para probar la API

---

## 📈 Roadmap

### ✅ Fase 1 - MVP (Completado)
- [x] Modelo RandomForest entrenado
- [x] API REST funcional
- [x] Interfaz web básica
- [x] Integración meteorológica
- [x] Documentación técnica
- [x] Tests automatizados completos
- [x] Deploy en OCI
- [x] CI/CD con GitHub Actions
- [x] Monitoring y alertas
- [x] Performance optimization
- [x] Historial de predicciones
- [x] Dashboard de analytics

### 🚀 Fase 2 - Evolución (Planeado)
- [ ] App móvil (React Native)
- [ ] Notificaciones push
- [ ] API pública con rate limiting
- [ ] Modelo mejorado con más features

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Este proyecto fue desarrollado durante un hackathon, pero está abierto a mejoras.

### Cómo Contribuir

1. **Fork** el repositorio
2. **Crea** una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** tus cambios (`git commit -m 'Add: Amazing Feature'`)
4. **Push** a la rama (`git push origin feature/AmazingFeature`)
5. **Abre** un Pull Request

### Guías de Estilo

- **Commits:** Usar [Conventional Commits](https://www.conventionalcommits.org/)
  - `feat:` nuevas características
  - `fix:` correcciones de bugs
  - `docs:` cambios en documentación
  - `test:` agregar/modificar tests
  
- **Código:**
  - Java: Google Java Style Guide
  - Python: PEP 8
  - JavaScript: StandardJS

### Reportar Bugs

Abre un [issue](https://github.com/VektorAI-Equipo71/vektor-ai/issues) con:
- **Descripción** del problema
- **Pasos** para reproducir
- **Comportamiento esperado** vs **actual**
- **Screenshots** si aplica
- **Entorno:** OS, versiones de Docker, etc.

---
## 🏆 Hackathon ONE 2025 - Oracle + Alura Latam

<div align="center">

<img width="200" height="120" alt="ONE - Logo" src="https://github.com/user-attachments/assets/7f90bb38-b457-41af-814e-482c650f6003" />     <img width="180" height="100" alt="Alura - Logo" src="https://github.com/user-attachments/assets/7de0014e-1272-4dd2-8a7a-7d834f090a46" />


Este proyecto fue desarrollado como parte del **hackathon final** del Programa **Oracle Next Education (ONE)**, una iniciativa de Oracle en colaboración con Alura LATAM para formar desarrolladores y data scientist en Latinoamérica.

**Equipo:** Grupo 71  
**Duración:** 6 semanas    
**Plataforma:** NoCountry

[Más sobre el Programa ONE](https://www.oracle.com/latam/education/oracle-next-education/)

</div>

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo [LICENSE](LICENSE) para más detalles.

```
MIT License

Copyright (c) 2025 Vektor AI - Equipo 71

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 📞 Contacto y Soporte

### 💬 Canales de Comunicación
- **Email del Equipo:** vektor.ia.equipo71@gmail.com

---

## 🙏 Agradecimientos

Agradecemos especialmente a:

- **Oracle** y **Alura LATAM** por el Programa ONE
- **NoCountry** por la plataforma de colaboración
- Todos los **mentores** y **facilitadores** del programa
- La **comunidad open source** por las herramientas utilizadas
- Nuestras **familias** por el apoyo durante el hackathon

---

## 🌟 Star History

Si este proyecto te resultó útil, ¡considera darle una estrella! ⭐

---

<div align="center">

### 💙 Desarrollado con pasión por el Equipo 71

**Vektor AI** - *Predicción Inteligente de Retrasos de Vuelos*

---

[![GitHub](https://img.shields.io/badge/GitHub-Vektor--AI-blue?style=for-the-badge&logo=github)](https://github.com/VektorAI-Equipo71)
[![Oracle ONE](https://img.shields.io/badge/Oracle-ONE-orange?style=for-the-badge&logo=oracle)](https://www.oracle.com/latam/education/oracle-next-education/)
[![Made with ❤️](https://img.shields.io/badge/Made%20with-❤️-red?style=for-the-badge)](https://github.com/Vektor-AI)

</div>
