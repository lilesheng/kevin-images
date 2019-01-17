# Version 0.0.1
FROM java:8

MAINTAINER kevin "451676182@qq.com"

# 环境变量
ENV COMMON_INIT /commonPrj/init
ENV COMMON_DATA /commonPrj/data
ENV FONT_PATH /usr/lib/jvm/java-8-openjdk-amd64/jre/lib/fonts/fallback

#RUN
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone
RUN mkdir -p $COMMON_INIT
RUN mkdir -p $COMMON_DATA
RUN mkdir -p $FONT_PATH

#VOLUME
VOLUME ["/commonPrj/init", "/commonPrj/data"]

#COPY
COPY simsun.ttf $FONT_PATH/

# CMD
CMD ["sh", "/commonPrj/init/setup.sh"]