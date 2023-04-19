# Event Driven Microservices using Spring Boot 

# order-service

````
2023-04-19 22:05:48.016  INFO 44589 --- [nio-8070-exec-2] c.e.orderservice.kafka.OrderProducer     : Order event => OrderEvent(message=order status is in pending state, status=PENDING, order=Order(orderId=5f5e0d27-ddd4-479e-9b0b-2de6aa38578f, name=LG TV, qty=1, price=1000.0, customerName=John Doe, status=COMPLETED, orderDate=2023-05-05))
2023-04-19 22:05:48.042  INFO 44589 --- [nio-8070-exec-2] o.a.k.clients.producer.ProducerConfig    : ProducerConfig values: 
````

# stock-service

````
2023-04-19 22:05:48.668  INFO 43747 --- [ntainer#0-0-C-1] c.e.stockservice.kafka.OrderConsumer     : Order event received in stock service => OrderEvent(message=order status is in pending state, status=PENDING, order=Order(orderId=5f5e0d27-ddd4-479e-9b0b-2de6aa38578f, name=LG TV, qty=1, price=1000.0, customerName=John Doe, status=COMPLETED, orderDate=2023-05-05))
````

# email-service

````
2023-04-19 22:05:48.665  INFO 43798 --- [ntainer#0-0-C-1] c.e.emailservice.kafka.OrderConsumer     : Order event received in email service => OrderEvent(message=order status is in pending state, status=PENDING, order=Order(orderId=5f5e0d27-ddd4-479e-9b0b-2de6aa38578f, name=LG TV, qty=1, price=1000.0, customerName=John Doe, status=COMPLETED, orderDate=2023-05-05))
````

# CURL:

```
curl --location 'localhost:8070/api/v1/orders' \
--header 'Content-Type: application/json' \
--data '{
    "name": "LG TV",
    "qty": 1,
    "price": 1000,
    "customerName": "John Doe",
    "status": "COMPLETED",
    "orderDate": "2023-05-05"
}'
```
<img width="546" alt="Screenshot 2023-04-19 at 10 20 48 PM" src="https://user-images.githubusercontent.com/54174687/233145496-85bad5e2-7bdd-421d-9ba5-4882b2272729.png">

<img width="725" alt="Screenshot 2023-04-19 at 10 21 04 PM" src="https://user-images.githubusercontent.com/54174687/233145475-42dd7ceb-5808-401c-a27c-5f3f539c4128.png">

<img width="1341" alt="Screenshot 2023-04-19 at 10 22 24 PM" src="https://user-images.githubusercontent.com/54174687/233145778-09b97679-61ef-4f4c-96e2-fec5d0470a66.png">




