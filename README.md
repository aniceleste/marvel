# marvel
web
cambiar marvel por index

docker build -t marvel-site .

docker run -d -p 8081:80 marvel-site 

# Utilizar la imagen base de Nginx
FROM nginx:alpine

# Copiar los archivos de tu sitio web al directorio predeterminado de Nginx
COPY ./ /usr/share/nginx/html

# Exponer el puerto 80 para que puedas acceder al sitio
EXPOSE 80

# Comando para iniciar Nginx
CMD ["nginx", "-g", "daemon off;"]
