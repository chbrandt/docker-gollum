FROM ruby
RUN apt-get -y update && \
    apt-get -y install libicu-dev cmake python-pip && \
    apt-get clean
RUN pip install docutils
RUN gem install gollum \
#                redcarpet \
                org-ruby
WORKDIR /wiki
CMD ["gollum", "--port", "80", "--mathjax", "--show-all"]
EXPOSE 80
