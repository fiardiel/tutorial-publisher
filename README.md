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

## Monitoring chart based on the publisher
![MonitoringChart](image/spike.png)

From the chart, we can infer that when the publisher sends data to the broker, 
the chart will spike, if the spike is high, it means that the publisher sends a lot of data to the broker. And we can see that in the chart, the first spike is high, and then it goes lower down to 0, and then it spikes again, this is due to the fact that I ran the publisher program multiple times first, and then I delayed the next 2 program runs. 