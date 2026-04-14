FROM eclipse-temurin:21-jdk-jammy
WORKDIR /app
COPY . .

RUN chmod +x mvnw
RUN ./mvnw clean package -DskipTests
RUN ls -la && pwd

EXPOSE 8086
# CMD ["java", "-jar", "target/*.jar"]
ENTRYPOINT ["sh", "-c", "java -jar target/*.jar"]
