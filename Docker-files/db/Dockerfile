FROM mysql:8.0.33-debian

# Set environment variables
ENV MYSQL_ROOT_PASSWORD=admin123
ENV MYSQL_DATABASE=accounts
ENV MYSQL_USER=admin
ENV MYSQL_PASSWORD=admin123

# Copy the database backup file
COPY db_backup.sql /docker-entrypoint-initdb.d/

# Expose MySQL port
EXPOSE 3306

# Set the default command
CMD ["mysqld"]
