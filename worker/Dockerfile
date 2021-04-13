FROM python:3-alpine AS multilayer
RUN pip install redis && pip install requests
COPY . .
CMD ["python", "worker.py"]

FROM scratch
COPY --from=multilayer / /
