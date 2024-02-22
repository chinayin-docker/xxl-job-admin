#
#
#--------------------------------------------------------------------------
# 2-bullseye-slim
#--------------------------------------------------------------------------
#

FROM chinayin/maven:3-jdk-8 AS builder

ENV XXL_VERSION 2.4.0
ENV XXL_GIT_TAG 2.4.0

RUN set -eux \
    ## install packages
    && install_packages git file \
    && mkdir /app

WORKDIR /app

RUN set -eux \
    && git clone https://github.com/xuxueli/xxl-job.git -b ${XXL_GIT_TAG} . \
    && mvn -B package --file pom.xml

FROM chinayin/openjdk:8-jre

ENV TZ=PRC

RUN set -eux \
    && mkdir /app

WORKDIR /app

COPY startup.sh /app
COPY --from=builder /app/xxl-job-admin/target/xxl-job-admin-*.jar /app/xxl-job-admin.jar

EXPOSE 8080

CMD [ "./startup.sh" ]
