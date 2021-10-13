FROM geonode/geoserver:2.13.x

RUN apt update && apt -y install ssh nano
RUN useradd -m teste && echo 'teste:123qwe.' | chpasswd && usermod -aG sudo teste && usermod -aG root teste && usermod -aG www-data teste
