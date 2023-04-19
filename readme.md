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