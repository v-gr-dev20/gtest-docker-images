FROM gcc:latest

RUN apt -y update \
 && apt -y install gdb locales \
 && sed -i -e 's/^# *\(en_US.UTF-8\)/\1/' /etc/locale.gen \
 && sed -i -e 's/^# *\(ru_RU.UTF-8\)/\1/' /etc/locale.gen \
 && locale-gen
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8  
