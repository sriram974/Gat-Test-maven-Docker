# Gat-Test-maven-Docker

Running Test Using Docker Container
Create a Docker container:

mvn clean package 
docker build -t gatling-test-example .
You alternatively run make dist image.

Run the Docker container:

docker run -e "JAVA_OPTS=-DbaseUrl=http://localhost:8080" \
     -e SIMULATION_NAME=gatling.test.example.simulation.ExampleGetSimulation gatling-test-example:latest
