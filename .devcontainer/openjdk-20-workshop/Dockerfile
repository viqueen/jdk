FROM maven:3.9-eclipse-temurin-20

RUN apt-get update \
    && apt-get install -y file autoconf make unzip zip build-essential \
    && apt-get install -y libasound2-dev libcups2-dev libfontconfig1-dev libx11-dev libxext-dev \
    && apt-get install -y libxrender-dev libxrandr-dev libxtst-dev libxt-dev


RUN apt-get install -y git ant wget \
    && echo 'export ANT_HOME=/usr/share/ant' >> ~/.bashrc \
    && git clone https://github.com/viqueen/jtreg.git --depth 1 --no-tags /workspaces/jtreg \
    && cd /workspaces/jtreg \
    && bash make/build.sh --jdk /opt/java/openjdk