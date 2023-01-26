configuration terminal

event manager applet port-tracker
 event syslog pattern "%ETHPORT-5-IF_DOWN_LINK_FAILURE: Interface.*failure)$"
  action 1.0 regexp "Ethernet[0-9]\/[0-9]" $_syslog_msg port
  action 2.0 cli command "enable"
  action 3.0 cli command "config t"
  action 4.0 cli command "interface $port"
  action 5.0 cli command "shutdown"
