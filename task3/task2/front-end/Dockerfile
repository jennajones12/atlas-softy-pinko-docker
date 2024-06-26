# Use latest version of Nginx
FROM nginx:latest

# Cp front-end files to appropriate dir in Docker image
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Remove .git folder from the copied directory
RUN rm -rf /var/www/html/softy-pinko-front-end/.git

# Cp Nginx config file to appropriate dir
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose port
EXPOSE 9000
