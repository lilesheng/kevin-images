# Version 0.0.1
FROM nginx:1.12.0

#创建文件所在目录
RUN mkdir -p /nginx/data
RUN mkdir -p /nginx/init

#VOLUME
VOLUME ["/nginx/data", "/nginx/init"]

#RUN
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

#设置容器启动时执行的命令
CMD ["sh", "/nginx/init/setup.sh"]