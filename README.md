# Kafka-1
Data pipeline installation
Create a Kafka topics called trip and enriched_trip
• Replication factor 1
• Number of partitions 3

# Extract data from STM
Download the data set of STM GTFS from http://stm.info/sites/default/files/gtfs/gtfs_stm.zip
Have trips.txt file in your local machine accessible

# Data pipeline
Produce trips.txt file to Kafka using kafka-console-producer. Each line is one message.
Consume the trip topic into your application
Parse each record polled from Kafka into a Trip object
Instantiate an object of EnrichedTrip for each message (only populate trip data and leave the rest
empty e.g., null)
Convert each EnrichedTrip to CSV format and produce it to enriched_trip topic
