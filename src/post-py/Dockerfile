FROM python:3.6.0

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

COPY . /app

RUN pip install -r app/requirements.txt

# ADD . /app


WORKDIR /app

ENTRYPOINT ["python3", "post_app.py"]
