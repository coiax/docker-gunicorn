FROM python:2.7-stretch

RUN pip install gunicorn

WORKDIR /app

EXPOSE 8000

COPY gunicorn.conf /app
COPY hello_world.py /app

ENV PYTHONUNBUFFERED 1

ENTRYPOINT ["gunicorn", "--config", "./gunicorn.conf", "-b", ":8000"]
CMD ["hello_world:app"]
