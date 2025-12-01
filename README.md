# Portafolio de Santiago Ismael Flores-Chávez

Sitio web personal construido con Jekyll para GitHub Pages.

## Estructura

- `_config.yml` - Configuración de Jekyll
- `_layouts/` - Plantillas HTML reutilizables
- `_includes/` - Componentes reutilizables (header, footer)
- `assets/` - CSS, JavaScript e imágenes
- Páginas HTML con front matter YAML

## Desarrollo Local

1. Instalar Jekyll y dependencias:
   ```bash
   bundle install
   ```

2. Ejecutar servidor local:
   ```bash
   bundle exec jekyll serve
   ```

3. Abrir en navegador: `http://localhost:4000`

## Despliegue en GitHub Pages

1. Subir cambios a GitHub
2. GitHub Pages detectará automáticamente que es un sitio Jekyll
3. El sitio se construirá y desplegará automáticamente

## Notas

- Las rutas se manejan automáticamente con `relative_url` de Jekyll
- El sitio funciona tanto en repositorios de usuario (`username.github.io`) como en repositorios con nombre

