# Base Image 
FROM ubuntu:16.04 

# Owner of the Image 
MAINTAINER Amit Vashist <amitvashist7@outlook.com>

# Update the APT Repo 
RUN apt-get update 

# Install Apache Packages 
RUN apt-get install apache2 -y 

# Deploy Custom Apache Ports 
COPY ports.conf /etc/apache2/

# Deploy Custom Apache Web Page 
COPY index.html /var/www/html/

# My App Expose on Custom Port
EXPOSE 8080 

# Bring the Service 
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
