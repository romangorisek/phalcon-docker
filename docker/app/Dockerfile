# Pull base image
FROM phalconphp/php-apache:ubuntu-16.04

MAINTAINER Serghei Iakovlev <serghei@phalconphp.com>

ENV PROVISION_CONTEXT "development"

# Deploy scripts/configurations
COPY bin/*.sh /opt/docker/provision/entrypoint.d/

# RUN mkdir -p /vendor \
#     && composer --working-dir=/vendor require phalcon/devtools \
#     && ln -s /vendor/vendor/phalcon/devtools/phalcon.php /usr/local/bin/phalcon \
#     && chmod ugo+x /usr/local/bin/phalcon
    
RUN git clone https://vagrant:s5vagrant@gitlab.dspot.si/development/phalcon-devtools.git /phalcon-devtools \
    && cd phalcon-devtools \
    && sh phalcon.sh \
    && rm -f /usr/bin/phalcon \
    && ln -s /phalcon-devtools/phalcon.php /usr/bin/phalcon \
    && chmod ugo+x /usr/bin/phalcon