FROM gitlab/gitlab-runner:ubuntu-v17.8.4
#FROM gitlab/gitlab-runner:ubuntu-v13.10.0

#RUN sed -i s@/deb.debian.org/@/mirrors.aliyun.com/@g /etc/apt/sources.list
RUN apt-get clean && \
    apt-get update -y && \
    apt-get install -y sudo vim zlib1g-dev ruby-dev gcc libffi-dev make g++ ruby ruby-dev nodejs

# 替换gem国内源
#RUN gem sources --add http://gems.ruby-china.com/ --remove https://rubygems.org/ && \
#    gem install bundler
RUN gem install bundler -v 2.4.22

RUN usermod -a -G sudo gitlab-runner
