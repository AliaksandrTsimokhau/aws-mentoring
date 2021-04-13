# SERVICE: High availability vs Fault tolerance 

## Service Overview  

**High availability** means that a system will almost always maintain uptime, albeit sometimes in a degraded state. With regard to AWS, a system has high availability when it has 99.999% uptime, also known as "five nines". To put that in perspective, the system would be down for a mere five minutes and fifteen seconds a year. 

Fault tolerance**** means that a system will almost always maintain uptime — and users will not notice anything different during a primary system outage. 

We can reach HA with the following services: 
- LB
- ...


## Use cases / Considerations  

Let's imagine that you are in charge of architecting a website for your employees, and it is not accessible from the internet. It's only accessible from the company's intranet. On this site, employees need to look up data 80% of the time and write to a database 20% of the time. In a situation like this, high availability would be perfectly acceptable. 

In the event that the database server goes down, it would crossover to a read-only database. Now the employees can conduct 80% of their business unhindered until the primary system comes back up. As mentioned previously, SQS would be useful in this situation as well. The employees would be able to write to the database, but the request would simply be queued until the primary database is back up and running. 

Whether or not to utilize high availability over fault tolerance depends on your budget, and consequently the importance of the system. If you are running an e-commerce website with millions of hits a day, a fault tolerant system is your best bet. 

According to Google, sites that load within 5 seconds have 70% longer sessions. That being said, high availability might not cut it, and you will need to architect a fault tolerant website. If the system is running in a degraded state, there is a good chance that you will lose customers either way. So, you may as well up the budget to accommodate fault tolerance capabilities. 

## Governance
No

## Cautions 
No

## Pricing considerations  

If high availability was expensive in pre-AWS days, fault tolerance was exceedingly expensive. At a bare minimum, multiple servers would have to be load balanced, databases would have to be consistently replicated, and availability would have to span multiple regions. All of this would need to be maintained by the company itself.  


## More details:
- https://www.youtube.com/watch?v=miEHdzqlRsY&ab_channel=CloudAcademy 
- https://aws.amazon.com/legal/service-level-agreements/?nc1=h_ls 
- https://docs.aws.amazon.com/whitepapers/latest/fault-tolerant-components/fault-tolerant-components.pdf 

 