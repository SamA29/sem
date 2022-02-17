#Use the latest mySQL image
FROM mysql
#Set the woprking directory
WORKDIR /tmp
#Copy all the files to the working directory of the container
COPY test_db/*.sql /tmp/
COPY test_db/*.dump /tmp/
# Copy main sql file to docker-entrypoint-initdb.d.
# Scripts and SQL files in this folder are executed on a container startup
# This is specific to MySQL
COPY test_db/employees.sql /docker-entrypoint-initdb.d
ENV MYSQL_ROOT_PASSWORD example