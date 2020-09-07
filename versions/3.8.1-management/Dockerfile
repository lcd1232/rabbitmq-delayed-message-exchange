FROM rabbitmq:3.8.1-management

RUN apt-get update && \
  apt-get install -y curl && \
  curl -L https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/v3.8.0/rabbitmq_delayed_message_exchange-3.8.0.ez > $RABBITMQ_HOME/plugins/rabbitmq_delayed_message_exchange-3.8.0.ez && \
  chown rabbitmq:rabbitmq $RABBITMQ_HOME/plugins/rabbitmq_delayed_message_exchange-3.8.0.ez &&  \
  rabbitmq-plugins enable --offline rabbitmq_delayed_message_exchange && \
  rabbitmq-plugins enable --offline rabbitmq_consistent_hash_exchange
