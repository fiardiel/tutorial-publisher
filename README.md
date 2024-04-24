# ADVPROG Module 8 - Publisher

## How many data your publisher program will send to the message broker in one run? 
The publisher program will send 5 data to the message broker in one run, since in the main function, there are 
5 publish events and each publish events there are 1 `UserCreatedEventMessage` to the broker

## Same url `amqp://guest:guest@localhost:5672` as the subcriber program
The publisher program uses the same url `amqp://guest:guest@localhost:5672` as the subscriber program. This is because the publisher program will send the data to the message broker and the subscriber program will receive the data from the message broker.

## Running RabbitMQ as message broker
![RabbitMQImage](image/rabbitmq.png)

## Sending and processing event
![SendingMessage](image/consolesubscriber.png)

The publisher program will send the data to the message broker and the subscriber program will receive the data from the message broker. The subscriber program will process the data and print the data to the console.