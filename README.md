Filebeat approach(without log4j)::

Filebeat -> Logstash -> Elasticsearch -> Kibana

1) create account on elk cloud (https://www.elastic.co/)
2) select observability for logs -> scroll down, it asks to select cloud on which you want to maintain all these stuffs (aws, azure, google) 
  -> click on create deployment -> It will show you a popup window with username and password. You can simply copy and paste it somewhere 
     or you can download the file
3) close the popup
4) you will see "Open Kiban" option (sometime it asks to download kibana)
5) Scroll down -> you will have Easticsearch endpoint, Kibana endpoint and CloudId. Copy and paste these thing somewhere.
6) goto email and verify email it will redirect you to elastic cloud again(elastic cloud for adminstration use)
7) Click on Elastic logo(left upper side)
8) Open Observability and Kibana in new tab
9) first goto observability -> scroll down and click on Get Started.
10) It will redirect you to Add Data page. You will have multiple option from whre you want to fetch data.
11) In our case we will be selecting Logstash Logs option. Click on ALL tab which is present in same page (Add Data page).
12) Search for Logstash Logs and select it -> select your OS and follow all the given steps -> 
13) Open filebeat.yml (C:\Program Files\Filebeat) and provide configuration that showed here<<link>>
14) Run this command: filebeat.exe -c filebeat.yml
15) click on menu -> management -> stack management -> data -> index management -> index templates -> create template
16) click on menu -> management -> stack management -> kibana -> index pattern -> create index pattern -> 
  search for create template(created in 1st step) -> choose timestamp field
15) click on discover -> select your index pattern
