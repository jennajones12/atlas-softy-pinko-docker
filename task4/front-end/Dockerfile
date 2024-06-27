# Use latest version of Nginx
FROM nginx

# Cp front-end files to appropriate dir in Docker image
COPY ./softy-pinko-front-end /usr/www/html/softy-pinko-front-end

# Remove .git folder from the copied directory
RUN rm -rf /usr/www/html/softy-pinko-front-end/.git

# Cp Nginx config file to appropriate dir
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose port
EXPOSE 9000
