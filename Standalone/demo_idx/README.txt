Here is the minimal configuration set up required at Splunk standalone indexer to accept data from UF.
1. Enable the receiving port to accept data on port#9997 --> <<SPLUNK_HOME>>/etc/system/local/inputs.conf
2. Disable the web port#8000 by using any one of the following way,
   -> By configuring <<SPLUNK_HOME>>/etc/system/local/web.conf
   -> Using command ./splunk disable webserver
3. Create an index  --> <<SPLUNK_HOME>>/etc/apps/demo_idx1/local/indexes.conf
   * $SPLUNK_DB -> /opt/splunk/var/lib/splunk