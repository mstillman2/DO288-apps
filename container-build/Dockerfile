# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 9090
LABEL io.k8s.description="A basic Apache HTTP Server child image uses ONBUILD" \
      io.k8s.display-name="Apache HTTP Server" \ 
      io.openshift.expose-services="9090:http" \
      io.openshift.tags="appache, httpd"
RUN sed -i "s/Listen 90/Listen 9090/g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && chmod -R g=u /var/log/httpd /var/run/httpd
USER 1001

