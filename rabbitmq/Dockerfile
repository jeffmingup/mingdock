FROM rabbitmq:alpine


RUN rabbitmq-plugins enable --offline rabbitmq_management

COPY management_agent.disable_metrics_collector.conf  /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf 

EXPOSE 4369 5671 5672 15671 15672 25672