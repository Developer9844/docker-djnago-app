FROM python:3

WORKDIR /app

ENV PYTHONUNBUFFERED=1

RUN pip install --upgrade pip

COPY ./requirements.txt .

RUN pip install -r requirements.txt

COPY . .


EXPOSE 8001

CMD ["gunicorn", "project1.wsgi", "--bind", "0.0.0.0:8001"]
