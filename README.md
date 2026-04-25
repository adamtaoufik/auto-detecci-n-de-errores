# 🚀 Detector de Errores del Sistema (Linux)

> Monitorización + autocorrección básica de servicios y sistema en tiempo real.

---

## 🧠 ¿Qué hace?

Este script en Python actúa como un **watchdog del sistema**, cubriendo 3 áreas clave:

- ⚙️ **Servicios críticos**
  - Verifica estado (`cron`, `NetworkManager`, `ssh`, `cups`)
  - Reinicia automáticamente si fallan
  - Notifica errores si no se recuperan

- 💻 **Estado del sistema**
  - Uso de CPU, RAM y disco
  - Temperatura de la CPU
  - Detección de picos peligrosos

- 📁 **Archivos de configuración**
  - Comprueba rutas clave (`/etc/...`)
  - Restaura desde plantillas si faltan

---

## 🏗️ Arquitectura

main()
 ├── dect_arch()
 ├── dect_servicios()
 └── dect_sys()

Loop continuo con control de errores.

---

## ⚙️ Requisitos

- Python 3.x  
- psutil → `pip install psutil`  
- Linux con `systemctl` y `notify-send`

---

## 📂 Configuración

```python
CONFIG_FILE = "/home/plantilla.json"
PLANTILLAS = "/ruta/a/plantillas"
```

---

## ▶️ Ejecución

```bash
python3 script.py
```

---

## 🚨 Casos de uso

- Servidores domésticos  
- Sistemas Linux críticos  
- Automatización básica

---

## ⚠️ Notas

- Requiere permisos sobre `/etc` y servicios
- Base para escalar a daemon / systemd

---

## 👨‍💻 Autor

Adam Taoufik Ezouhari
