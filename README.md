# SALECAR-Proyecto-Final-Redes-2025

**Análisis y visualización de datos del mercado automotor de Emiratos Árabes mediante microservicios y procesamiento distribuido.**

---

## 🚗 Descripción del Proyecto

Sale Cars es una plataforma web que permite explorar, analizar y visualizar información sobre vehículos usados en Emiratos Árabes Unidos. El sistema combina una arquitectura de microservicios en Node.js con un clúster de Apache Spark para análisis de datos a gran escala, integrando visualizaciones dinámicas mediante Metabase.

---

## 🧩 Arquitectura del Sistema

### 🔹 Microservicios Web
- **Usuarios:** Registro, login, gestión de perfiles (Node.js + Express + JWT).
- **Vehículos:** CRUD de anuncios de autos.
- **Compras:** Agendamiento y simulación de compra.
- **Frontend:** React.js + Tailwind CSS + React Router.

### 🔹 Sistema de Análisis Distribuido
- **Apache Spark Cluster (Dockerized):** Procesamiento en paralelo.
- **PySpark Runner:** Pipeline ETL y consultas SQL.
- **Base de Datos:** MySQL 8.0 (contenedorizada).
- **Metabase:** Dashboards incrustados en el frontend vía iframes.

---

## 📊 Dataset Utilizado

**Fuente:** [UAE Used Car Prices - Kaggle](https://www.kaggle.com/datasets/alikalwar/uae-used-car-prices-and-features-10k-listings)

**Tamaño:** 10,000+ registros

**Variables principales:** `make`, `model`, `year`, `mileage`, `price`, `fuel_type`, `transmission`, `color`, `engine_size`, `cylinders`.

---

## ⚙️ Tecnologías

- **Backend:** Node.js, Express, bcrypt, JWT, mysql2
- **Frontend:** React.js, Tailwind CSS
- **Base de datos:** MySQL
- **Procesamiento:** Apache Spark + PySpark
- **Visualización:** Metabase
- **Orquestación:** Docker Swarm
- **Pruebas de carga:** Apache JMeter

---

## 🚀 Despliegue

1. Clonar el repositorio.
2. Construir imágenes:
   ```bash
   docker build -t mariavalencia30/salescarsv2-usuarios backend/usuarios_src
   docker push mariavalencia30/salescarsv2-usuarios
   # Repetir para cada microservicio y componente

3.Iniciar Docker Swarm:
docker swarm init --advertise-addr <IP_manager>

4.Desplegar stack:
docker stack deploy -c docker-compose.yml salescarsv2


---

## 🔐 Credenciales de Acceso al Panel de Administrador

- **Email:** admisalecars@car.com  
- **Nombre:** Maria V  
- **Teléfono:** 123456789  
- **Contraseña:** thebestcars  

---

## 📊 Acceso a Métricas y Paneles de Administración

- **Estadísticas de HAProxy:**  
  [http://192.168.119.138:8404/haproxy_stats](http://192.168.119.138:8404/haproxy_stats) *(ajustar según IP utilizada)*

- **Interfaz de Apache Spark (Web UI):**  
  [http://192.168.119.138:8081/](http://192.168.119.138:8081/) *(ajustar según IP utilizada)*

---

## 📁 Ruta de Trabajo del Proyecto en Servidor

El proyecto debe estar ubicado en:  
`/var/www/html/SalesCarsV2`
