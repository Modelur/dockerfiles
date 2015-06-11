FROM ubuntu

MAINTAINER Ziga Stopinsek <ziga.stopinsek@modelur.com>

RUN apt-get update \
      && DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-client php5-gd php5-mysql php5-curl nano emacs23-nox curl php5 php5-mcrypt php5-mysql rsync\
	  && cd /tmp\
	  && curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar\
	  && chmod +x wp-cli.phar\
	  && sudo mv wp-cli.phar /usr/local/bin/wp;

CMD ["/bin/bash"]
