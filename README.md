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

### Important Stream APIs

- map
- flatmap
- filter
- reduce
- collect
- join

### Windowing Concept

The windowing concept brings the notion of micro-batching within an unbounded data stream.

- Tumbling Window
A tumbling windows assigner assigns each element to a window of a specified window size. Tumbling windows have a fixed size and do not overlap. For example, if you specify a tumbling window with a size of 5 minutes, the current window will be evaluated and a new window will be started every five minute

- Sliding Window
The sliding windows assigner assigns elements to windows of fixed length. Similar to a tumbling windows assigner, the size of the windows is configured by the window size parameter. An additional window slide parameter controls how frequently a sliding window is started. Hence, sliding windows can be overlapping if the slide is smaller than the window size. In this case elements are assigned to multiple windows.
For example, you could have windows of size 10 minutes that slides by 5 minutes. With this you get every 5 minutes a window that contains the events that arrived during the last 10 minutes

- Session Window
The session windows assigner groups elements by sessions of activity. Session windows do not overlap and do not have a fixed start and end time, in contrast to tumbling windows and sliding windows. Instead a session window closes when it does not receive elements for a certain period of time, i.e., when a gap of inactivity occurred

- Global Window
A global windows assigner assigns all elements with the same key to the same single global window.

### Notion Of Time
For micro-batching or windowing the streams based on time - the notion of time plays a key role. The windows can be created by "processing time" (the time the event is received at the pipeline) or the "event time" (the time is part of the event payload and is the time when event got generated). Windowing based on the processing time is straight forward, where as based on event time is tricky as events can arrive pretty late.

As events can come unordered or late the windowing uses heuristics to identify when to close a window or process the events in window. Broader concepts of "watermark" and "triggers" are used to identify all events belongng to the window and processing/garbage collection of windows respectively.



