## a. What is amqp?
- amqp memiliki kepanjangan "Advanced Message Queuing Protocol". AMQP merupakan protokol message broker yang dipakai untuk komunikasi antar aplikasi. Dalam aplikasi ini, amqp digunakan untuk membantu  membantu publisher mengirim message ke queue, lalu subscriber akan mengambil message tersebut dari queue dan memprosesnya.


## b. What does it mean? guest:guest@localhost:5672 , what is the first guest, and what is the second guest, and what is localhost:5672 is for?  
- guest yang pertama adalah user untuk rabbitMQ
- gues yang kedua adalah password untuk rabbitMQ
- @localhost dipakai ketika rabbitMQ dijalankan secara local
- 5672 adalah port default amqp untuk rabbitMQ