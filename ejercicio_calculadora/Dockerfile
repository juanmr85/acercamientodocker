#Utiliza una imagen Alpine
FROM alpine:latest

#Actualiza repositorios locales e instala el paquete python3
RUN apk update && apk add python3

#Añade el repositorio de la calculadora
COPY calculadora.py /app/calculadora.py

#Pasa variables de entorno a la calculadora
ENV IDIOMA=es \
    MODO=estandar \
    HISTORIAL=/app/historial.txt \
    DEBUG=false \
    MEMORIA=0

#Directorio de trabajo donde estamos trabajando actualmente
WORKDIR /app

#Comando para ejecutar la calculadora
CMD ["python3", "calculadora.py"]