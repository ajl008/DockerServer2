#base image
FROM maven:3.8.1-openjdk-11
#set working directory
WORKDIR /usr/app
#copy files needed for app to run or jar file
# could also copy files folder: COPY files/* files/
# or mount volume so if you make new files, container sees live
COPY ./target/server-1.0-SNAPSHOT.jar /usr/app
#run the application
ENTRYPOINT java -cp server-1.0-SNAPSHOT.jar lvc.cds.App
# ENTRYPOINT ["/bin/sh", "run.sh"]
# CMD ["java", "App"]

# to debug: ENTRYPOINT /bin/bash


#docker build -t [tag name] .
#docker run -t -i -p 3333:8080 [tag name]
#ctrl C to stop, rm to remove
#test on localhost:3333/?file=foo.txt