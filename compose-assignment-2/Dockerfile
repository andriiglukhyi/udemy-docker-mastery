# create yo;ur custom drupal image here, based of official drupal
FROM drupal:8.2
# update and install git
RUN  apt-get update && apt-get install -y git \ 
     && rm -rf /var/lib/apt/lists/*
# change workdir
WORKDIR /var/www/html/themes
# clone repo
RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \ 
    && chown -R www-data:www-data bootstrap
# change direcrory back 
WORKDIR /var/www/html