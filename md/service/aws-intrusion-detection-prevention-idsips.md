### Question 1:

A web company is looking to implement an intrusion detection and prevention system into their deployed VPC. This platform should have the ability to scale to thousands of instances running inside of the VPC. How should they architect their solution to achieve these goals?

- A. Configure an instance with monitoring software and the elastic network interface (ENI) set to promiscuous mode packet sniffing to see an traffic across the VPC. 
- B. Create a second VPC and route all traffic from the primary application VPC through the second VPC where the scalable virtualized IDS/IPS platform resides.
- C. Configure servers running in the VPC using the host-based ‘route’ commands to send all traffic through the platform to a scalable virtualized IDS/IPS 
- D. Configure each host with an agent that collects all network traffic and sends that traffic to the IDS/IPS platform for inspection.

<details><summary>Answer:</summary><p>
[D]

Categories:
[VPC, IDS]

Explanation:

Question 1@http://jayendrapatil.com/aws-intrusion-detection-prevention-idsips/

A: virtual instance running in promiscuous mode to receive or“sniff” traffic

C: host based routing is not allowed

</p></details><hr>

### Question 2:

You are designing an intrusion detection prevention (IDS/IPS) solution for a customer web application in a single VPC. You are considering the options for implementing IDS/IPS protection for traffic coming from the Internet. Which of the following options would you consider? (Choose 2 answers)

- A. Implement IDS/IPS agents on each Instance running In VPC
- B. Configure an instance in each subnet to switch its network interface card to promiscuous mode and analyze network traffic. 
- C. Implement Elastic Load Balancing with SSL listeners In front of the web applications 
- D. Implement a reverse proxy layer in front of web servers and configure IDS/IPS agents on each reverse proxy server

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[VPC, IDS, ELB]

Explanation:

Question 2@http://jayendrapatil.com/aws-intrusion-detection-prevention-idsips/

B: virtual instance running in promiscuous mode to receive or“sniff” traffic

C: ELB with SSL does not serve as IDS/IPS

</p></details><hr>

