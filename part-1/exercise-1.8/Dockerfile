FROM ubuntu:16.04

RUN apt-get update && apt-get install -y bc git
RUN git clone https://github.com/helineva/bc-average.git && chmod a+x /bc-average/average.sh

ENTRYPOINT ["/bc-average/average.sh"]
