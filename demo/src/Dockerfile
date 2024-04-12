# Koristimo zvanicni Docker image za Java 11
FROM adoptopenjdk:11-jre-hotspot

# Postavljamo radni direktorijum unutar kontejnera
WORKDIR /app

# Kopiramo JAR fajl aplikacije u radni direktorijum
COPY target/demo-0.0.1-SNAPSHOT.jar application.jar

# Dodajemo environment varijable za povezivanje sa PostgreSQL bazom
# TODO: ove vrednosti ce se dobiti na kolokvijumu
ENV DB_HOST hostname
ENV DB_PORT port
ENV DB_NAME name
ENV DB_TABLE table
ENV DB_USERNAME db_username
ENV DB_PASSWORD db_password

# Pokrećemo Spring Boot aplikaciju prilikom startovanja kontejnera
CMD ["java", "-jar", "application.jar"]