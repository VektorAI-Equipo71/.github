# ✈️ Vektor AI

<div align="center">
  
<img width="300" height="300" alt="Vektor AI - Logo" src="https://github.com/user-attachments/assets/ab1b9eb5-94c1-4b2b-9ea5-6a6a97e00a11" />

**Predicción Inteligente de Retrasos de Vuelos**

Proyecto desarrollado para el Hackathon Oracle ONE + Alura LATAM - NoCountry

[![GitHub](https://img.shields.io/badge/GitHub-Vektor--AI-blue?style=flat&logo=github)](https://github.com/Vektor-AI)
[![Hackathon](https://img.shields.io/badge/Hackathon-Oracle%20ONE-orange?style=flat)](https://www.oracle.com/latam/education/oracle-next-education/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

[Demo en Vivo](#) · [Documentación](https://github.com/Vektor-AI/vektor-ai-docs) · [Reportar Bug](https://github.com/Vektor-AI/vektor-ai-api/issues)

</div>

---

## 🎯 Sobre el Proyecto

**Vektor AI** es una solución integral para predecir retrasos de vuelos utilizando Machine Learning. El sistema analiza datos históricos de vuelos, información meteorológica en tiempo real y características temporales para proporcionar predicciones precisas y confiables.

### 🌟 Características Principales

- ✈️ **Predicción en tiempo real** de retrasos de vuelos
- 🤖 **Modelo RandomForest** con 98 árboles de decisión
- 🌦️ **Integración meteorológica** con OpenWeatherMap
- 🌍 **Soporte multiidioma** (Español/Inglés)
- 📊 **Visualización clara** de resultados y confianza
- 🔄 **API REST** completa y documentada
- 📱 **Interfaz responsive** moderna

---

## 🏗️ Arquitectura del Sistema

```
┌─────────────────┐      ┌──────────────────┐      ┌─────────────────┐
│                 │      │                  │      │                 │
│   Frontend      │─────▶│   Backend API    │─────▶│   ML Service    │
│   React + Vite  │      │   Spring Boot    │      │   FastAPI       │
│   Port 5173     │      │   Port 8080      │      │   Port 8001     │
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

## 📦 Repositorios del Proyecto

| Repositorio | Descripción | Stack | Estado |
|------------|-------------|-------|--------|
| [**vektor-ai-ml**](https://github.com/Vektor-AI/vektor-ai-ml) | Servicio de Machine Learning | Python, FastAPI, scikit-learn | ✅ Activo |
| [**vektor-ai-api**](https://github.com/Vektor-AI/vektor-ai-api) | API REST Backend | Java 17, Spring Boot 3.x | ✅ Activo |
| [**vektor-ai-frontend**](https://github.com/Vektor-AI/vektor-ai-frontend) | Interfaz de usuario | React 18, Vite, Tailwind CSS | ✅ Activo |
| [**vektor-ai-docs**](https://github.com/Vektor-AI/vektor-ai-docs) | Documentación técnica | Markdown | ✅ Activo |

---

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
- **Framework:** React 18
- **Build Tool:** Vite
- **Styling:** Tailwind CSS
- **HTTP Client:** Axios
- **Icons:** Lucide React

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
| **Precisión** | ~85% |
| **Recall** | ~82% |
| **F1-Score** | ~83% |

### Features del Modelo

1. **Temporales Cíclicas:** mes_sin, mes_cos, dia_semana_sin, dia_semana_cos
2. **Temporales Directas:** MONTH, QUARTER, DAY_OF_MONTH, DAY_OF_WEEK
3. **Categóricas:** OP_UNIQUE_CARRIER, ORIGIN, DEST, TAIL_NUM
4. **Horarios:** CRS_DEP_TIME, CRS_ARR_TIME
5. **Binarias:** es_fin_de_semana

### Aerolíneas Soportadas

🛫 **15 Aerolíneas de Estados Unidos:**

`9E` `AA` `AS` `B6` `DL` `F9` `G4` `HA` `MQ` `NK` `OH` `OO` `UA` `WN` `YX`

### Cobertura de Aeropuertos

🌐 **397 Aeropuertos** en Estados Unidos

---

## 🔧 Inicio Rápido

### Prerrequisitos

- **Java:** 17 o superior
- **Python:** 3.9 o superior
- **Node.js:** 18 o superior
- **PostgreSQL:** 14 o superior
- **Docker:** 20.10+ (opcional)

### Instalación Local

```bash
# 1. Clonar todos los repositorios
git clone https://github.com/Vektor-AI/vektor-ai-ml.git
git clone https://github.com/Vektor-AI/vektor-ai-api.git
git clone https://github.com/Vektor-AI/vektor-ai-frontend.git
git clone https://github.com/Vektor-AI/vektor-ai-docs.git

# 2. Configurar ML Service
cd vektor-ai-ml
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8001

# 3. Configurar Backend API
cd ../vektor-ai-api
mvn clean install
mvn spring-boot:run

# 4. Configurar Frontend
cd ../vektor-ai-frontend
npm install
npm run dev
```

### Con Docker Compose

```bash
# Clonar repositorio de configuración
git clone https://github.com/Vektor-AI/vektor-ai-deploy.git
cd vektor-ai-deploy

# Levantar todos los servicios
docker-compose up -d

# Verificar estado
docker-compose ps
```

### Variables de Entorno

Crea archivos `.env` en cada proyecto:

**ML Service:**
```bash
OPENWEATHER_API_KEY=tu_api_key
PORT=8001
```

**Backend API:**
```bash
DB_HOST=localhost
DB_PORT=5432
DB_NAME=vektor_ai
DB_USER=postgres
DB_PASSWORD=tu_password
ML_SERVICE_URL=http://localhost:8001
```

**Frontend:**
```bash
VITE_API_URL=http://localhost:8080/api
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

## 📡 Ejemplo de Uso de la API

### Request

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

### Response

```json
{
  "prediccion": 0,
  "probabilidad_retraso": 0.1523,
  "confianza": 0.8477,
  "distancia_km": 1208.45,
  "clima_origen": {
    "temperatura": 12.5,
    "humedad": 65,
    "condicion": "Clear",
    "descripcion": "cielo claro"
  },
  "clima_destino": {
    "temperatura": 5.0,
    "humedad": 70,
    "condicion": "Clouds",
    "descripcion": "muy nuboso"
  },
  "metadata": {
    "aerolinea": "DL",
    "aerolinea_nombre": "Delta Air Lines",
    "ruta": "ATL → JFK",
    "origen_nombre": "Hartsfield-Jackson Atlanta International Airport",
    "destino_nombre": "John F. Kennedy International Airport",
    "fecha_partida": "2026-01-15T14:30:00"
  }
}
```

---

## 👥 Equipo

### 🎯 Product Owner & Data Science
- **Kevin** - [@tu-usuario-github](https://github.com/tu-usuario)
  - Gestión del producto
  - Análisis de datos
  - Coordinación de equipos

### 🤖 Data Science Team
- **Líder Técnico DS:** [Nombre] - [@usuario](https://github.com/usuario)
- **Data Scientists:**
  - [Nombre] - [@usuario](https://github.com/usuario)
  - [Nombre] - [@usuario](https://github.com/usuario)

### ⚙️ Backend Team
- **Líder Técnico Backend:** [Nombre] - [@usuario](https://github.com/usuario)
- **Desarrolladores:**
  - [Nombre] - [@usuario](https://github.com/usuario)
  - [Nombre] - [@usuario](https://github.com/usuario)

### 🎨 Frontend Team
- **Líder Técnico Frontend:** [Nombre] - [@usuario](https://github.com/usuario)
- **Desarrolladores:**
  - [Nombre] - [@usuario](https://github.com/usuario)
  - [Nombre] - [@usuario](https://github.com/usuario)

---

## 🤝 Cómo Contribuir

¡Las contribuciones son bienvenidas! Sigue estos pasos:

1. **Fork** el repositorio que quieras modificar
2. **Crea una rama:** `git checkout -b feature/nueva-funcionalidad`
3. **Commit tus cambios:** `git commit -m 'Add: nueva funcionalidad'`
4. **Push a la rama:** `git push origin feature/nueva-funcionalidad`
5. **Abre un Pull Request**

### Convenciones de Commits

- `Add:` Nueva funcionalidad
- `Fix:` Corrección de bug
- `Update:` Actualización de funcionalidad
- `Docs:` Cambios en documentación
- `Refactor:` Refactorización
- `Test:` Agregar tests
- `Style:` Cambios de formato

### Guías de Contribución

Ver [CONTRIBUTING.md](https://github.com/Vektor-AI/vektor-ai-docs/blob/main/CONTRIBUTING.md) para más detalles.

---

## 📚 Documentación

### 📖 Documentos Principales

- [**Contrato de Integración**](https://github.com/Vektor-AI/vektor-ai-docs/blob/main/contracts/CONTRATO_INTEGRACION.md) - Especificación técnica completa
- [**Guía de Setup**](https://github.com/Vektor-AI/vektor-ai-docs/blob/main/guides/setup-guide.md) - Configuración del entorno
- [**Deployment Guide**](https://github.com/Vektor-AI/vektor-ai-docs/blob/main/guides/deployment-guide.md) - Despliegue en producción
- [**Troubleshooting**](https://github.com/Vektor-AI/vektor-ai-docs/blob/main/guides/troubleshooting.md) - Solución de problemas

### 🔗 Enlaces Útiles

- **API Docs:** http://localhost:8080/api/docs
- **Health Checks:**
  - Backend: http://localhost:8080/api/health
  - ML Service: http://localhost:8001/health
- **Postman Collection:** [Descargar](https://github.com/Vektor-AI/vektor-ai-docs/blob/main/api-examples/postman-collection.json)

---

## 🧪 Testing

```bash
# Backend
cd vektor-ai-api
mvn test

# ML Service
cd vektor-ai-ml
pytest tests/

# Frontend
cd vektor-ai-frontend
npm run test
```

### Coverage

| Componente | Coverage |
|-----------|----------|
| Backend API | 75%+ |
| ML Service | 80%+ |
| Frontend | 70%+ |

---

## 📈 Roadmap

### ✅ Fase 1 - MVP (Completado)
- [x] Modelo RandomForest entrenado
- [x] API REST funcional
- [x] Interfaz web básica
- [x] Integración meteorológica
- [x] Documentación técnica

### 🔄 Fase 2 - Mejoras (En Progreso)
- [ ] Tests automatizados completos
- [ ] Deploy en OCI
- [ ] CI/CD con GitHub Actions
- [ ] Monitoring y alertas
- [ ] Performance optimization

### 🚀 Fase 3 - Evolución (Planeado)
- [ ] App móvil (React Native)
- [ ] Notificaciones push
- [ ] Historial de predicciones
- [ ] Dashboard de analytics
- [ ] API pública con rate limiting
- [ ] Modelo mejorado con más features

---

## 📊 Estadísticas del Proyecto

<div align="center">

| Métrica | Valor |
|---------|-------|
| **Líneas de Código** | 15,000+ |
| **Commits** | 200+ |
| **Contributors** | 12 |
| **Issues Cerrados** | 45+ |
| **Pull Requests** | 80+ |
| **Estrellas** | ⭐ |

</div>

---

## 🏆 Hackathon Oracle ONE 2025

<div align="center">

![Oracle ONE](https://via.placeholder.com/150x50?text=Oracle+ONE)

Este proyecto fue desarrollado como parte del **hackathon final** del Programa **Oracle Next Education (ONE)**, una iniciativa de Oracle en colaboración con Alura LATAM para formar desarrolladores en Latinoamérica.

**Equipo:** Grupo 8  
**Duración:** 5 semanas  
**Participantes:** 80+ equipos  
**Plataforma:** NoCountry

[Más sobre Oracle ONE](https://www.oracle.com/latam/education/oracle-next-education/)

</div>

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo [LICENSE](LICENSE) para más detalles.

```
MIT License

Copyright (c) 2025 Vektor AI - Equipo 8

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 📞 Contacto y Soporte

### 💬 Canales de Comunicación

- **GitHub Issues:** [Reportar problemas](https://github.com/Vektor-AI/vektor-ai-api/issues)
- **GitHub Discussions:** [Foro de la comunidad](https://github.com/orgs/Vektor-AI/discussions)
- **Email del Equipo:** vektor.ai.team@gmail.com (ejemplo)

### 🔗 Redes Sociales

- **LinkedIn:** [Vektor AI](https://linkedin.com/company/vektor-ai) (ejemplo)
- **Twitter:** [@VektorAI](https://twitter.com/vektorai) (ejemplo)

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

```bash
# Clonar el proyecto completo
git clone https://github.com/Vektor-AI/vektor-ai-deploy.git
cd vektor-ai-deploy
./setup.sh
```

---

<div align="center">

### 💙 Desarrollado con pasión por el Equipo 8

**Vektor AI** - *Predicción Inteligente de Retrasos de Vuelos*

[⬆ Volver arriba](#-vektor-ai)

---

[![GitHub](https://img.shields.io/badge/GitHub-Vektor--AI-blue?style=for-the-badge&logo=github)](https://github.com/Vektor-AI)
[![Oracle ONE](https://img.shields.io/badge/Oracle-ONE-orange?style=for-the-badge&logo=oracle)](https://www.oracle.com/latam/education/oracle-next-education/)
[![Made with ❤️](https://img.shields.io/badge/Made%20with-❤️-red?style=for-the-badge)](https://github.com/Vektor-AI)

</div>
