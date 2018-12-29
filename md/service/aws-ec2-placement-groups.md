### Question 3:

What is required to achieve gigabit network throughput on EC2? You already selected cluster-compute, 10GB instances with enhanced networking, and your workload is already network-bound, but you are not seeing 10 gigabit speeds.

- A. Enable biplex networking on your servers, so packets are non-blocking in both directions and there’s no switching overhead.
- B. Ensure the instances are in different VPCs so you don’t saturate the Internet Gateway on any one VPC.
- C. Select PIOPS for your drives and mount several, so you can provision sufficient disk throughput
- D. Use a placement group for your instances so the instances are physically near each other in the same Availability Zone.

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, VPC]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-placement-groups/

D: (You are not guaranteed 10 gigabit performance, except within a placement group. Using placement groups enables applications to participate in a low-latency, 10 Gbps network)

</p></details><hr>

### Question 4:

You need the absolute highest possible network performance for a cluster computing application. You already selected homogeneous instance types supporting 10 gigabit enhanced networking, made sure that your workload was network bound, and put the instances in a placement group. What is the last optimization you can make?

- A. Use 9001 MTU instead of 1500 for Jumbo Frames, to raise packet body to packet overhead ratios.
- B. Segregate the instances into different peered VPCs while keeping them all in a placement group, so each one has its own Internet Gateway.
- C. Bake an AMI for the instances and relaunch, so the instances are fresh in the placement group and do not have noisy neighbors
- D. Turn off SYN/ACK on your TCP stack or begin using UDP for higher throughput.

<details><summary>Answer:</summary><p>
[A]

Categories:
[VPC]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-placement-groups/

A: (For instances that are collocated inside a placement group, jumbo frames help to achieve the maximum network throughput possible, and they are recommended in this case)

</p></details><hr>

