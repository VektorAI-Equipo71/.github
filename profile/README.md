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

[Demo en Vivo](#) · [Documentación](https://github.com/VektorAI-Equipo71/vektor-ai/tree/main/docs)

</div>

---

## 🎯 Sobre el Proyecto

**Vektor AI** es una solución integral para predecir retrasos de vuelos utilizando Machine Learning. El sistema analiza datos históricos de vuelos, información meteorológica en tiempo real y características temporales para proporcionar predicciones precisas y confiables.

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

## 👥 Equipo

### 🎯 Product Owner
- **Kevin Joel Lemos** - [@niveKJ](https://github.com/niveKJ)

### 📊 Scrum Master
- **Gloria Carolina Guerrero Velandia** - [@CarolinaG2024](https://github.com/CarolinaG2024)

### 🤖 Data Science Team
- **Líder Técnico DS:** [Sofía Martínez Véjar] - [@smv1980](https://github.com/smv1980)
- **Data Scientists:**
  - [Karen Brenes] - [@Karen-13C](https://github.com/Karen-13C)
  - [Miguel Baillon] - [@MPBOga](https://github.com/MPBOga)
  - [Ronald Varela] - [@Ronaldvarela852](https://github.com/Ronaldvarela852)
  - [Gloria Carolina Guerrero Velandia] - [@CarolinaG2024](https://github.com/CarolinaG2024)
  - [Cristian Camilo Maje] - [@CamiloTrr](https://github.com/CamiloTrr)
  - [Kevin Lemos] - [@usuario](https://github.com/usuario)
 
### ⚙️ FullStack Team
- **Líder Técnico Backend & Fontend:** [Edgar Alejandro Nestor Castillo] - [@EdgarNestorC](https://github.com/EdgarNestorC)
- **Desarrollador FullStack:** [Jose Julio Rodriguez Benito] - [@JoseBenin82](https://github.com/JoseBenin82)

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
vektor-ai/
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


## 🚀 Stack Tecnológico

### Machine Learning
- **Lenguaje:** Python 3.9+
- **Framework:** FastAPI
- **ML Library:** scikit-learn
- **Procesamiento:** pandas, numpy
- **Modelo:** RandomForestClassifier (98 árboles)

### Backend
- **Lenguaje:** Java 17
- **Framework:** Spring Boot 3.x
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
| **Features** | 15 características |
| **Precisión** | ~79% |
| **Recall** | 82% |
| **F1-Score** | 86% |
| **ROC-AUC** | 83% |

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

- **[ARCHITECTURE.md](docs/ARCHITECTURE.md)** - Arquitectura del sistema
- **[CONTRATO_INTEGRACION.md](docs/CONTRATO_INTEGRACION.md)** - Contrato de integración API
- **[GUIA_PRUEBAS.md](docs/testing/GUIA_PRUEBAS.md)** - Guía de pruebas
- **[Colección Postman](postman/)** - Colección para probar la API

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

## 🏆 Hackathon Oracle ONE 2025

<div align="center">

![Oracle ONE](https://via.placeholder.com/150x50?text=Oracle+ONE)

Este proyecto fue desarrollado como parte del **hackathon final** del Programa **Oracle Next Education (ONE)**, una iniciativa de Oracle en colaboración con Alura LATAM para formar desarrolladores en Latinoamérica.

**Equipo:** Grupo 71  
**Duración:** 5 semanas    
**Plataforma:** NoCountry

[Más sobre Oracle ONE](https://www.oracle.com/latam/education/oracle-next-education/)

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
