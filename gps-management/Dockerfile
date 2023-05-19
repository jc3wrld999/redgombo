FROM python:3.7-alpine
WORKDIR /app
COPY requirements.txt .
RUN python3 -m pip install -U pip
RUN python3 -m pip install -r requirements.txt
RUN python3 -m pip install gunicorn
COPY . .
EXPOSE 5001
# CMD ["python", "app.py"]
CMD ["gunicorn", "-w", "4", "--bind", "0.0.0.0:5001", "wsgi"]