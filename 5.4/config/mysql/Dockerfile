FROM mysql:5.5

COPY ./my.cnf /etc/mysql/conf.d

RUN apt-get update && apt-get install -y locales \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN sed -i -E 's/# (jp_JP.UTF8)/\1/' /etc/locale.gen \
    && locale-gen

ENV LANG jp_JP.UTF-8

CMD ["mysqld", "--character-set-server=utf8", "--collation-server=utf8_unicode_ci"]
