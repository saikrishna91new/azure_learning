There are 2 types of azure load balancers
1> Regional load balancer (with in the region)
  - Basic or standerd load blancer (l4) -  tcp & udp,, no application awareness
  - Application gateway (later 7) - http/https

    
2> Global load balncer (multi region)
  - DNS  based load balancing with using azure traffic manager
  - Global http/htpps load balancing using azure front door



>>> Azure standerd load balancer l4
  * supports tcp & udp
  * TCP - ( transmission control protocal)  - need acknowledgement for each packet transferred
  * UDP - is dont ask for any acknowledgement it simply sentthe traffic (us3er daatagram protocal)
  * TCP apps examples: emial, banking, sharess..etc use tcp protocal
  * UDP apps: stereaming applications as exampl
  * Azure standerd load balancer dont support application url based routing
  * ![image](https://github.com/user-attachments/assets/d41f6db4-c10d-4d67-9fe9-8bde1b7fefaf)

>> Creatong lb options:
    * sku : basic , stnaderd, gateway
    * Type: public, interanl
    * Tier: regional, global ( regional within the region, global: on lb from one region to other lb in other region traffic)
    * Front end ip: ip for lb (mandatory while creating the lb)
    * backend pools (can do later)
    * inbound and out bound rules (can do later)

>> options at lb in portal:
 * fornt end ip
 * backedn pools : tha target machines to sent the traffic
 * health probes: for lb to check weather the backend pools are healthy or not to take traffic
   options while creating: name, protocal, port , intrval
 * loadblanacing rules : decides the traffic roting on which frontend ip which port goes to which backend pool on which port
   Other config while creating: forint end ip, port, baclned pool, port , select the heath probe , tcp reset, floating ip 
 * inbound nat
 * outbound
 * properties

>> Once the lb is configured create the dns rule with a record like below
  ![image](https://github.com/user-attachments/assets/6f8f41b4-bfd3-45af-802b-44f2f8ea6b1b)
>> 




