FROM python:3-alpine AS multilayer
COPY . .
RUN pip install redis && pip install requests

FROM scratch
COPY --from=multilayer / /

CMD ["worker.py"]
ENTRYPOINT ["python"]
