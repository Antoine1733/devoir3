FROM python:latest
COPY . /app

RUN pip3 install psycopg2
RUN wget https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh -P /
RUN chmod +x /wait-for-it.sh
ENTRYPOINT ["/wait-for-it.sh", "db:5432", "--"]
CMD ["python", "-m","app"]

