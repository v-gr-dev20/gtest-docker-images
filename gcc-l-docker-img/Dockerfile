FROM gcc:latest

RUN apt-get update -y \
 && apt-get upgrade -y \
 && apt-get install -y gdb \
 && apt-get install -y locales \
 && sed -i -e 's/^# *\(en_US.UTF-8\)/\1/' /etc/locale.gen \
 && sed -i -e 's/^# *\(ru_RU.UTF-8\)/\1/' /etc/locale.gen \
 && locale-gen
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8  
