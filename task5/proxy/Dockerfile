# Use the latest version of Nginx
FROM nginx:latest

# Remove default configuration file
RUN rm /etc/nginx/conf.d/default.conf

# Copy proxy configuration file
COPY proxy.conf /etc/nginx/conf.d/

EXPOSE 80
