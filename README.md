# streams

Stream is a continuous flow of data through a pipeline. These data could be originated from various data sources and moving towards other data sinks. There are rich set of APIs available to process this data and to generate meaningful insights from this data. Unlike the traditional ETL where insights were generated once the data is at rest. Streams API allows to analyze the data while in transit - there by making it more real-time.

## Bounded streams

Bounded data stream have a defined start and end. Typically, all the data is ingested before performing any computations. Similar to traditional ETL.

## Unbounded streams

Unbounded streams have a start but no defined end. They do not terminate and provide data as it is generated. There’s no waiting for all the data to arrive because the data stream never stops coming, and events in the data stream can arrive out of order.



