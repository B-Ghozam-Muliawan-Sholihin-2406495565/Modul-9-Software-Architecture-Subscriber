## a. What is amqp?
- amqp memiliki kepanjangan "Advanced Message Queuing Protocol". AMQP merupakan protokol message broker yang dipakai untuk komunikasi antar aplikasi. Dalam aplikasi ini, amqp digunakan untuk membantu  membantu publisher mengirim message ke queue, lalu subscriber akan mengambil message tersebut dari queue dan memprosesnya.


## b. What does it mean? guest:guest@localhost:5672 , what is the first guest, and what is the second guest, and what is localhost:5672 is for?  
- guest yang pertama adalah user untuk rabbitMQ
- gues yang kedua adalah password untuk rabbitMQ
- @localhost dipakai ketika rabbitMQ dijalankan secara local
- 5672 adalah port default amqp untuk rabbitMQ

## Simulation slow subscriber
![rabbitmq](assets/image.png)

## why the total number of queue is as such
- Pada komputer saya menunjukkan queue adalah 6 yang berarti pada saat itu ada 6 queued messages yang masih menunggu diproses oleh subscriber. Ini terjadi karena pada source code sengaja waktu proses message sengaja dilambatkan, sehingga subscriber membutuhkan waktu lebih lama untuk menangani setiap message. Sementara itu, publisher dapat mengirim message lebih cepat daripada kemampuan subscriber untuk memprosesnya. jadinya, beberapa message akan ngantri di queue RabbitMQ sebelum akhirnya dikonsumsi oleh subscriber. Jumlah queue saya berbeda karena queue ini dapat berbeda di setiap komputer tergantung kecepatan eksekusi program, waktu menjalankan publisher dan subscriber, serta environment sistem.