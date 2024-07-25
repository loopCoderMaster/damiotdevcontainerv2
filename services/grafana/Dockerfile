ARG GRAFANA_VERSION="latest"
FROM grafana/grafana:${GRAFANA_VERSION}

# Set Grafana options
ENV GF_ENABLE_GZIP=true
ENV GF_USERS_DEFAULT_THEME=light
ENV GF_FEATURE_TOGGLES_ENABLE=topnav

# Updates Check (Optional)
# Disabilitati di default, decommentate se necessario
#ENV GF_ANALYTICS_CHECK_FOR_UPDATES=false
#ENV GF_ANALYTICS_CHECK_FOR_PLUGIN_UPDATES=false

# Copia il file grafana.ini
COPY grafana.ini /etc/grafana/grafana.ini

# Non modificare l'utente Grafana
USER grafana

# Entrypoint (lasciato inalterato)
ENTRYPOINT ["/run.sh"]