FROM clojure:openjdk-16-lein-slim-buster

WORKDIR /

RUN apt-get update && apt-get install -y curl zip unzip
RUN curl -s -L https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-3.3.0.1492-linux.zip -o sonarscanner.zip
RUN unzip -qq sonarscanner.zip
RUN rm -rf sonarscanner.zip
RUN mv sonar-scanner-3.3.0.1492-linux sonar-scanner
COPY sonar-scanner.properties sonar-scanner/conf/sonar-scanner.properties
ENV SONAR_RUNNER_HOME=sonar-scanner
ENV PATH $PATH:/sonar-scanner/bin

WORKDIR /app

ENTRYPOINT ["tail", "-f", "/dev/null"]