apiVersion: apps/v1
kind: Deployment
metadata:
  name: php-app-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: php-app
  template:
    metadata:
      labels:
        app: php-app
    spec:
      containers:
      - name: php-container
        image: yourdockerhubusername/basic-php-website:latest
        ports:
        - containerPort: 80
