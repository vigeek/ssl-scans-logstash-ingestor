# ssllabs-logstash-ingestor
Runs SSL Labs or SSlyze tests against domains, outputs data into logstash with proper formatting.

# Work in progress
Initial push is just the logstash configuration.  A script is used that can be used in bulk scanning or continous integration systems.  Script will be posted soon.

# Note
The logstash configuration will parse SSL labs results and create a new record for each endpoint tested. 

To see it in action:   curl "https://api.ssllabs.com/api/v2/analyze?host=www.ssllabs.com&all=done" | curl -XPOST http://logstashhost:PORT --data-binary @-

The logstash configuration also supports parsing SSlyze scans, some light sanitation is required before posting.
