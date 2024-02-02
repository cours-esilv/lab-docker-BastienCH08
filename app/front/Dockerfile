# Use a lightweight base image for serving static content
FROM nginx:latest

# Set the working directory inside the container
WORKDIR /usr/share/nginx/html

# Copy the contents of the local 'app/front' directory to the container
COPY . .

RUN chmod -x /usr/share/nginx/html/entrypoint.sh

ENTRYPOINT ["/usr/share/nginx/html/entrypoint.sh"]

# Expose port 80 for serving the frontend
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]