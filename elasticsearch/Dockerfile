ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

ENV TZ=Asia/Karachi
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
