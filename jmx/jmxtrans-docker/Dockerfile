FROM java:8-jre
MAINTAINER Adam Kunicki <kunickiaj@gmail.com>

RUN set -x \
  && apt-get update -qq \
  && mkdir /opt/jmxtrans /opt/jmxtrans/conf /opt/jmxtrans/log \
  && apt-get clean -qq \
  && rm -rf /var/lib/apt/lists/*

COPY jmxtrans-254-local-all.jar /opt/jmxtrans/jmxtrans-all.jar

VOLUME /opt/jmxtrans/conf
COPY docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["jmxtrans"]
