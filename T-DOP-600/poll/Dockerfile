FROM python:3.8-alpine
WORKDIR /app
COPY . /app
EXPOSE 80
RUN  pip3 install -r requirements.txt
ENV FLASK_APP app.py
CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]