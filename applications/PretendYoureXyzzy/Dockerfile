FROM maven
WORKDIR /opt
RUN git clone https://github.com/fknbwdwn/PretendYoureXyzzy.git
WORKDIR PretendYoureXyzzy
COPY build.properties.example build.properties
RUN mvn clean package war:exploded -Dmaven.buildNumber.doCheck=false -Dmaven.buildNumber.doUpdate=false -DcheckModificationExcludeList=WebContent/js/cah.constants.js
EXPOSE 8080
CMD mvn jetty:run
