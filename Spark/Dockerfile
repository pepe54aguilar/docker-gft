FROM jupyter/datascience-notebook:latest

# Instalar Java
USER root
RUN apt-get update && apt-get install -y openjdk-8-jdk-headless && apt-get clean && \
    pip install pyspark && pip install findspark pandas
    
USER $NB_UID

# Configurar las variables de entorno JAVA_HOME
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
