# Java Producer and Consumer with Avro

## Producer preparation steps

1. Create a new topic called '\<my-initials\>-transactions' in ccloud 
2. Substitute your cluster API KEY and API KEY in file 'training.config'
3. Substitute your '\<my-initials\>' in file 'ProducerExample.java'

    private static final String TOPIC = "\<my-initials\>-transactions";

3. Build the producer

```bash
cd Module4/client/avro
mvn clean compile package
```

4. Execute the producer

```bash
mvn exec:java -Dexec.mainClass=io.confluent.examples.clients.basicavro.ProducerExample -Dexec.args="training.config"
```

## Consumer preparation steps

1. Substitute your cluster API KEY and API KEY in file 'training.config'
2. Substitute your '\<my-intials\>' in file 'ConsumerExample.java'

    private static final String TOPIC = "\<my-initials\>-transactions";

3. Build the consumer

```bash
mvn clean compile package
```

4. Execute the consumer

```bash
cd Module4/client/avro
mvn exec:java -Dexec.mainClass=io.confluent.examples.clients.basicavro.ConsumerExample -Dexec.args="training.config"
```

## This lab exercise is derived from the folowing confluent example...

This directory includes projects demonstrating how to use the Java producer and consumer with Avro and Confluent Schema Registry

How to use these examples:

* [ProducerExample.java](src/main/java/io/confluent/examples/clients/basicavro/ProducerExample.java): see [Confluent Schema Registry tutorial](https://docs.confluent.io/platform/current/schema-registry/schema_registry_tutorial.html?utm_source=github&utm_medium=demo&utm_campaign=ch.examples_type.community_content.clients-avro)
* [ConsumerExample.java](src/main/java/io/confluent/examples/clients/basicavro/ConsumerExample.java): see [Confluent Schema Registry tutorial](https://docs.confluent.io/platform/current/schema-registry/schema_registry_tutorial.html?utm_source=github&utm_medium=demo&utm_campaign=ch.examples_type.community_content.clients-avro)


