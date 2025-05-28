# Practica Git - Despregue con Docker

## Descrición do proxecto
Este proxecto consta dun frontend servido con Nginx, un backend en Flask e unha base de datos PostgreSQL. Todo está orquestrado mediante Docker Compose para facilitar o despregue e o desenvolvemento.

## Composición dos servizos
- **frontend**: Servido con Nginx usando a imaxe `nginx:alpine`. Serve a páxina `index.html` dende o directorio local `./frontend`.
- **backend**: Aplicación Flask que se executa nun contedor baseado nun Dockerfile personalizado. Código Python montado dinámicamente dende o host para facilitar a edición.
- **db**: Servizo PostgreSQL usando a imaxe oficial `postgres:15`. Usa un volume para persistencia de datos e executa un script SQL de inicialización.

## Comandos principais

- Levantar todos os servizos en segundo plano:

  ```bash
  docker-compose up --build -d

- Verificar logs do backend:
  
  ```bash
  docker-compose logs -f backend

- Deter os servizos:
  
  ```bash
  docker-compose down
