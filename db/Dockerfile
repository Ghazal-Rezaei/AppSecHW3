FROM mysql:latest

RUN mkdir /data
COPY ./products.csv /data/products.csv
COPY ./users.csv /data/users.csv

COPY ./migrate.sql /migrate.sql
COPY ./djangoSeed.py /djangoSeed.py

ENTRYPOINT ["/entrypoint.sh"]
CMD ["mysqld", "--secure-file-priv=/data"]
#CMD ["--secure-file-priv=/"]
