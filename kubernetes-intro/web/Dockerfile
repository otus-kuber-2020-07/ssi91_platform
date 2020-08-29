FROM nginx:latest

RUN useradd -r -u 1001 appuser \
    && mkdir /app && chown appuser /app \
    && chown appuser /var/log/nginx/error.log

COPY nginx.conf etc/nginx/nginx.conf

EXPOSE 8000
