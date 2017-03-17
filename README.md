# insecure_content

nagios check for insecure content on a webpage

either you need python-selenium from jessie-backports and
node install -g phantomjs:

    ./insecure_content https://www.abcnyheter.no/

or we wrap it in a huge docker image:

    docker build -t insecure_content .
    docker run -e "URL=https://www.abcnyheter.no" -it insecure_content


# repo git@github.com:startsiden/insecure_content.git
# build:
#
# docker build -t eu.gcr.io/divine-arcade-95810/check-http-insecure-content:latest .
# gcloud docker push eu.gcr.io/divine-arcade-95810/check-http-insecure-content:latest

