FROM python:3-alpine
RUN pip install redis && pip install requests
COPY . .
CMD ["python", "worker.py"]
