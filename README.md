// Docker HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Static Website</title>
</head>
<body>
    <h1>Welcome to My Static Website</h1>
    <p>This is a simple website served using Docker and Nginx.</p>
</body>
</html>

//Docker File
# Use the official Nginx image from Docker Hub
FROM nginx:alpine

# Copy the index.html file into the Nginx default public directory
COPY index.html /usr/share/nginx/html/

# Expose port 80 to allow external access to the website
EXPOSE 80

# Run Nginx in the foreground (default command for the Nginx container)
CMD ["nginx", "-g", "daemon off;"]
