# Streams

Stream is a continuous flow of data through a pipeline. These data could be originated from various data sources and moving towards other data sinks. There are rich set of APIs available to process this data and to generate meaningful insights from this data. Unlike the traditional ETL where insights were generated once the data is at rest. Streams API allows to analyze the data while in transit - there by making it more real-time.

### Bounded streams

Bounded data stream have a defined start and end. Typically, all the data is ingested before performing any computations. Similar to traditional ETL.

### Unbounded streams

Unbounded streams have a start but no defined end. They do not terminate and provide data as it is generated. There is no waiting for all the data to arrive because the data stream never stops coming, and events in the data stream can arrive out of order.

#### Examples of streaming applications

- Event-driven applications where the streams are formed by event data.

- Data Analytics applications where the streams are formed by data 

- Data Pipeline applications like ETL

#### Popular Distributed Stream Processing Engines

- Apache Spark
- Apache Flink
- Apache Storm
- Apache Kafka is the most popular data streams pipeline, that can scale to transmit very large amount of data and is the backbone of most stream processing systems.




