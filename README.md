# Request Hub

Este repositorio contiene la configuración principal del proyecto **Request Hub**, integrando los siguientes submódulos:

* [request-hub-web](https://github.com/WongLeyF/request-hub-web) → Interfaz web.
* [request-hub-api](https://github.com/WongLeyF/request-hub-api) → Backend y API.

## 🚀 Configuración del Proyecto

### Clonación del repositorio con submódulos
Para clonar este proyecto junto con los submódulos, usa:

```bash
git clone --recurse-submodules git@github.com:WongLeyF/request-hub.git
```

Si ya has clonado el repositorio sin submódulos, inicialízalos manualmente con:

```bash
git submodule init
git submodule update --recursive
```

### Actualizar los submódulos
Para traer los últimos cambios de los repositorios de los submódulos:

```bash
git submodule update --remote --merge
```

### Eliminar un submódulo
Si necesitas eliminar un submódulo, usa:

```bash
git submodule deinit -f [nombre_submodulo]
rm -rf .git/modules/[nombre_submodulo]
git rm -f [nombre_submodulo]
```

## 📂 Estructura del Repositorio

```plaintext
request-hub/
├── web/  # Submódulo de la interfaz web
├── api/  # Submódulo de la API
├── assets/ # Recursos multimedia
│   └── images/ # Capturas de pantalla
├── README.md
├── .gitmodules
└── .gitignore
```

## 🐳 Iniciar el proyecto dockerizado
Para iniciar el proyecto con Docker, asegúrate de tener Docker y Docker Compose instalados. Luego, ejecuta:

### Iniciar el frontend
```bash
docker-compose -f web/docker-compose.yml up -d
```

### Iniciar el backend
```bash
docker-compose -f api/docker-compose.yml up -d
```

## 🖼️ Capturas de pantalla

### Dashboard
![Dashboard](assets/images/dashboard.png)

### Administración de Solicitudes
![Solicitudes](assets/images/requests.png)
![Nueva Solicitud](assets/images/new-request.png)
![Ver Solicitud](assets/images/view-request.png)

### Aprobaciones
![Aprobaciones](assets/images/approvals.png)

### Administración de Tipos de Solicitud
![Administración de Tipos de Solicitud](assets/images/request-type-admin.png)

### Administración de Usuarios
![Administración de Usuarios](assets/images/user-admin.png)

### Reportes
![Reportes](assets/images/reports.png)
![Reportes Generados](assets/images/reports-generated.png)