FROM python:3-alpine AS multilayer
RUN pip install Flask
COPY . .
CMD ["python", "rng.py"]
EXPOSE 8080

FROM scratch
COPY --from=multilayer / /
