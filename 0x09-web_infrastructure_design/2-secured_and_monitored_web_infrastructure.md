![image](https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Diagramme%20sans%20nom5.drawio#Uhttps%3A%2F%2Fraw.githubusercontent.com%2FRhadbane%2Falx-system_engineering-devops%2Fmain%2FDiagramme%2520sans%2520nom5.drawio)

### For every additional element, why you are adding it

- 3 Firewalls: The first Firewall checks the rules after receiving the requests and could deny following requests. The second firewall is working in the server to prevent someone hacking depending of the requests, and the third firewall acts as a circuit-level firewalls, inspect the transaction of the information.
- SSL certificate: 1 SSL certificate: is added to secure https protocols and encrypt communication. Then, the ‘plain text’ won’t be easy accessed or viewed by a third person, making the protocol communication and data transfer form the browser and web server more secure (Instant SSL, 2021)

### What are firewalls for

Firewalls is a network security device that monitors network traffic, it can be understood as a division or “wall” between a private network and public network which limits and blocks network traffic based on a set of security rules in the hardware or software by analyzing data packets that request entry to the network. Additionally, firewalls are used to allow remote access to a private network through secure authentication (Beal, 1996)

### Why is the traffic served over HTTPS

HTTPS stands for HyperText Transfer Protocol Secure, and the traffic is served in order to bring protection by using the secure port 443, which encrypts outgoing information. Then it is more difficult to spy or get access to the site’s information.

### What monitoring is used for

Monitoring is practice used for quality control. As Peter Ducker said, “What can’t be measured, it can’t be improved”. Then, monitoring not only helps to make sure to maintain high quality levels, keeping the established standards and consistency, but also to help in the continuous improvement of the resources performance.

The way data monitoring is performed, relies on checking new data against predefined rules and metrics. If data quality anomalies are detected, an alert is sent in order to give information about the metrics and rules violation, so data can be checked (Informatica, 2021).

3 monitoring clients: 2 monitoring deployed in each master-server, and one monitoring client for the load balancer. This will help understand the metrics of the performance of the resources according to the users requests. The information gathered will help us improve users’ experience and make decisions on the future whether to scale up the web infrastructure system.

### How the monitoring tool is collecting data

IT monitoring is composed of three parts: 1) Fundation; 2) Software, and 3) Interpretation in order to function.

- Foundation: Are related to the infrastructure at its lowest layer of the software stack. This includes physical and virtual devices, such as servers, CPUs and VMs.
- Software: The software is the monitoring section which analyzes what is happening in the devices (physical or virtual machines) in terms of CPU usage, load, memory, and running count.
- Interpretation: Here is where collected data is turned into metrics and are presented through graphs or data charts (mostly on GUI dashboard). This is often integrated with tools of data visualization to help better understand and do data analytics of performance (Gillis, 2020).

### Explain what to do if you want to monitor your web server QPS

Queries per second is a measure of the rate of traffic going in a particular server serving a Web domain. It is an important metric to monitor, because it can help you decide whether to scale the server in order to cope with the demand of usage, and resource requirement so the web page won’t collapse in the future with overload server request.

## Issues with the secured and monitored web infrastructure
