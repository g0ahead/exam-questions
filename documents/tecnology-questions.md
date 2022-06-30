## Was ist RabbitMQ?
RabbitMQ basiert auf der Idee des Advanced Message Queuing Protocols (AMQP). Der große Vorteil von 
AMQP: Sender und Empfänger müssen nicht die gleiche Programmiersprache verstehen. Inzwischen hat 
sich der Messaging Broker etwas von AMQP gelöst und geht dank Plug-ins auch mit anderen 
Nachrichtenprotokollen wie STOMP oder MQTT um – die Idee bleibt aber die gleiche: Zwischen dem 
Produzenten und dem Konsumenten einer Nachricht liegt eine Warteschlange. 
In dieser werden die Messages zwischengelagert.

## Wie ist der Ablauf mit RabbitMQ
Bei der Nachrichtenübermittlung gibt es vier Stationen:
- Producer: erzeugt Nachrichten
- Exchange: leitet Nachrichten weiter
- Queue: lagert Nachrichten
- Consumer: verarbeitet die Nachricht