# Drupal Listado Usuarios (DDEV Project)

[`Lea la versión en español aquí`](https://github.com/astralmemories/drupal-listado-usuarios/blob/main/README_ES.md)

This repository contains a fully configured **Drupal 10/11 project using DDEV**.

This project was built to support the development and testing of my custom Drupal module, [`listado_usuarios`](https://github.com/astralmemories/listado_usuarios). The module displays a paginated, AJAX-powered list of users with filtering capabilities—all built using only custom code and Drupal best practices.

👉 You can learn more about the module in the [main repository](https://github.com/astralmemories/listado_usuarios)  
🌐 [Leer la versión en español](https://github.com/astralmemories/listado_usuarios/blob/main/README_ES.md)

---

## Getting Started with DDEV

Follow these steps to get the project up and running:

### 1. Prerequisites

Make sure you have the following tools installed:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [DDEV](https://ddev.readthedocs.io/en/stable/)

### 2. Clone this repository

```sh
git clone https://github.com/astralmemories/drupal-listado-usuarios.git
```

### 3. Start the DDEV environment

```sh
cd drupal-listado-usuarios
ddev start
```

### 4. Install Drupal dependencies via Composer

```sh
ddev composer install
```

### 5. Add the \`listado_usuarios\` custom module

Clone the custom module into the correct path:

```sh
git clone https://github.com/astralmemories/listado_usuarios.git web/modules/custom/listado_usuarios
```

### 6. Import the prebuilt database

The repository includes a preconfigured Drupal database for testing:

```sh
ddev drush sql-cli < ./BBDD/database.sql
```

### 7. Clear the cache and Launch the site

```sh
ddev drush cr
ddev launch
```

> The site will open at: [https://drupal-listado-usuarios.ddev.site](https://drupal-listado-usuarios.ddev.site)

### 8. View the Listado Usuarios page

Visit the user list page (/listado-usuarios):

[https://drupal-listado-usuarios.ddev.site/listado-usuarios](https://drupal-listado-usuarios.ddev.site/listado-usuarios)

### 9. Access the module configuration page

Use the following credentials to access the admin interface:

- **Username**: `admin`
- **Password**: `pass`

You can log in at:  
[https://drupal-listado-usuarios.ddev.site/user](https://drupal-listado-usuarios.ddev.site/user)

Access the module configuration page:

[https://drupal-listado-usuarios.ddev.site/admin/config/system/listado_usuarios](https://drupal-listado-usuarios.ddev.site/admin/config/system/listado_usuarios)

Or navigate manually:

\`Configuration → System → Configuración Listado de Usuarios\`

**Configurable Settings**
   - API URL
   - Users per page
   - Enable/disable JavaScript console logs for debugging