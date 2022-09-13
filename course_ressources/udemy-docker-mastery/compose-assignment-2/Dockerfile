FROM drupal:8.2

#RUN apt package manager command to install git
RUN apt-get update \
    && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*



WORKDIR /var/www/html/themes

#use git to clone the theme
RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    #we need to change permissions on files
    && chown -R www-data:www-data bootstrap 

WORKDIR /var/www/html
