
# Drupal Listado Usuarios (Proyecto DDEV)

Este repositorio contiene un proyecto completamente configurado de **Drupal 10/11 usando DDEV**.

Este proyecto fue creado para apoyar el desarrollo y las pruebas de mi módulo personalizado de Drupal, [`listado_usuarios`](https://github.com/astralmemories/listado_usuarios). El módulo muestra una lista paginada de usuarios con capacidad de filtrado, todo implementado usando solo código personalizado y las mejores prácticas de desarrollo en Drupal.

👉 Puedes conocer más sobre el módulo en el [repositorio principal](https://github.com/astralmemories/listado_usuarios/blob/main/README_ES.md)

---

## Comenzando con DDEV

Sigue estos pasos para poner en marcha el proyecto:

### 1. Requisitos Previos

Asegúrate de tener instaladas las siguientes herramientas:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [DDEV](https://ddev.readthedocs.io/en/stable/)

### 2. Clona este repositorio

```sh
git clone https://github.com/astralmemories/drupal-listado-usuarios.git
```

### 3. Inicia el entorno DDEV

```sh
cd drupal-listado-usuarios
ddev start
```

### 4. Instala las dependencias de Drupal vía Composer

```sh
ddev composer install
```

### 5. Agrega el módulo personalizado `listado_usuarios`

Clona el módulo personalizado en la ruta correcta:

```sh
git clone https://github.com/astralmemories/listado_usuarios.git web/modules/custom/listado_usuarios
```

### 6. Importa la base de datos preconfigurada

El repositorio incluye una base de datos de Drupal lista para pruebas:

```sh
ddev drush sql-cli < ./BBDD/database.sql
```

### 7. Limpia la caché y lanza el sitio

```sh
ddev drush cr
ddev launch
```

> El sitio se abrirá en: [https://drupal-listado-usuarios.ddev.site](https://drupal-listado-usuarios.ddev.site)

### 8. Ver la página de Listado de Usuarios

Visita la página de listado de usuarios (/listado-usuarios):

[https://drupal-listado-usuarios.ddev.site/listado-usuarios](https://drupal-listado-usuarios.ddev.site/listado-usuarios)

### 9. Accede a la página de configuración del módulo

Usa las siguientes credenciales para acceder a la interfaz de administración:

- **Usuario**: `admin`  
- **Contraseña**: `pass`

Puedes iniciar sesión en:  
[https://drupal-listado-usuarios.ddev.site/user](https://drupal-listado-usuarios.ddev.site/user)

Accede a la página de configuración del módulo:

[https://drupal-listado-usuarios.ddev.site/admin/config/system/listado_usuarios](https://drupal-listado-usuarios.ddev.site/admin/config/system/listado_usuarios)

O navega manualmente:

`Configuración → Sistema → Configuración Listado de Usuarios`

**Ajustes configurables**
   - URL de la API
   - Usuarios por página
   - Activar/desactivar los logs de consola JavaScript para depuración
