FROM nginx:latest

RUN useradd -r -u 1001 appuser \
    && mkdir /app && chown appuser /app \
    && chown appuser /var/log/nginx/error.log
    # && chown appuser /var/run/nginx.pid

COPY nginx.conf etc/nginx/nginx.conf

# USER appuser

EXPOSE 8000

# RUN useradd -r -u 1001 webuser && \
#     mkdir /app && \
#     chown webuser /app

# COPY hw.html /app

# RUN sed -i -r 's/listen.+;/listen 8000;/g' /etc/nginx/conf.d/default.conf && \
#     sed -i -r 's/root.+;/root \/app;/g' /etc/nginx/conf.d/default.conf && \
#     sed -i -r 's/user\s.+;/user webuser;/g' /etc/nginx/nginx.conf
# EXPOSE 8000/tcp
