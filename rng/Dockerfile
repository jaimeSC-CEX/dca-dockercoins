FROM python:3-alpine AS multilayer
COPY . .
RUN pip install Flask

FROM scratch
COPY --from=multilayer / /

CMD ["rng.py"]
ENTRYPOINT ["python"]
EXPOSE 8080
