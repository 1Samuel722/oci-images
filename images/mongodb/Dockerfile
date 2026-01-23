# Bitnami-compatible MongoDB image
# Built on official MongoDB image with Bitnami directory structure and environment variables

ARG MONGODB_VERSION=8

FROM mongo:${MONGODB_VERSION}

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

# Create bitnami-compatible directory structure
RUN mkdir -p /bitnami/mongodb/data /bitnami/mongodb/conf /bitnami/mongodb/logs \
    && chown -R mongodb:mongodb /bitnami

VOLUME ["/bitnami/mongodb"]

EXPOSE 27017

ENTRYPOINT ["/entrypoint.sh"]
