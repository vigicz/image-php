FROM ghcr.io/vigicz/php:8.1-fpm

# Install SUPERVISOR
RUN apt-get update && apt-get install -y supervisor logrotate gettext \
    && apt-get clean -y  \
    && apt-get autoclean -y  \
    && apt-get autoremove -y  \
    && rm -rf /var/lib/apt/lists/* /var/lib/log/* /tmp/* /var/tmp/* \
    && touch /var/run/supervisor.sock \
    && chmod 777 /var/run/supervisor.sock

ADD ./supervisord.conf /etc/supervisor/supervisord.conf