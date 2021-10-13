I will try to ans this question in four parts 


1. Initial typing 
2. URL parsing
3. Protocol deciding 
4. DNS look up


## Initial typing 
when ever we type any thing , It look up in our local history if not found then in our local cache memory 

Still not found ? then we goto second step i.e, URL parsing

## URL parsing

Here it checks, wheather is it a URL ? if yes then we will visit it , but for visiting a website we must be known about the protocol it is using to visiting the website.

So the next step is to decide which protocol is to be use, HTTP or HTTPS ?

## Protocol deciding

If we do not mention the protocol the browser its preloaded HSTS ( HTTP strict transport security ) list. 
If searched website is in the list then browser use HTTPS ( port no. 443 ) protocol else it will use HTTP ( port no. 80 ).

Now we know that 
 first | second
-|-
domain name | google.com 
Protocol | HTTPS  
Port | 443
Ip | ?

For IP address, we need to Look up upon DNS ( Domain name server )

## DNS loop up 

The first server to which our query interacts with is the **DNS resolver or recursive resolver** which can be operated by our ISP (Internet Service Provider) or a third party provider.

If website is found is cache memory of DNS resolver then ok , else  

* The first type of DNS server to which recursive resolver talks to is the root server. 

  * There are 13 root servers are running all over the world ( A - M ) and each one knows DNS information about TLD (top-level domain) and root server 
  will give the IP adress of corresponding TLD to recursive resolver. 

* TLD refers to the last part of a domain name. For example( .com is TLD in google.com). 
   * Some other examples of TLD are .com for Commercial businesses, .gov for government, .edu for Educational purpose, .org for non-profit Organizations, .mil for 
   Military purpose, .net for Network organizations, and Country code TLDs represent specific geographic locations. For example: .in represents India.
   
* Now the TLD server for the ‘.com’ will respond and it will return the IP adress of nameserver with the records of ‘google.’ portion of the domain name in Authorative server to recursive reslver.
* The authoritative name server is the final stop for a DNS query and return the IP adress of google to recursive resolver. 
* Recursive resolver give it back to our browser and then our browser connect to the servers of IP address it received.  

    
All this process take place in 10th of second. ( Amazing right ? ) 

