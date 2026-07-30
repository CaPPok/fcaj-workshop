---
title: "Blog 2"
date: 2026-07-29
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# AWS FAULT INJECTION SERVICE – PROACTIVELY INJECTING FAULTS TO TEST SYSTEM STABILITY

Over the past week, I've been learning about how to deploy and operate applications so they run stably. However, when exploring further into the principles of the AWS Well-Architected Framework, I came across a concept called Chaos Engineering – proactively creating fault scenarios to test if a system is truly resilient enough. To support this, AWS provides the AWS Fault Injection Service.

This is a service that helps create controlled experiments on AWS infrastructure to assess the fault tolerance of a system against incidents like network disconnections, CPU spikes, or stopping an EC2 Instance. What I find interesting is that the experiments are executed according to a pre-defined scenario, rather than injecting faults randomly.

## What can AWS FIS do?

After researching, I found that AWS FIS supports various types of experiments, such as:

- Stopping or rebooting an EC2 Instance.
- Increasing CPU utilization on EC2.
- Simulating network latency or disconnection.
- Experimenting with Amazon ECS or Amazon EKS.
- Testing the reaction of Auto Scaling when an Instance encounters an issue.

> [!NOTE]
> Through these experiments, the development team can evaluate whether the system self-heals as expected.

## Fault Injection Experiment

To understand it better, I tried learning how to create a simple experiment on EC2.

**Step 1:** Access the AWS Console and search for AWS Fault Injection Service.

**Step 2:** Select Create experiment template.

The Template will describe the entire experiment, including resources, actions, and stop conditions.

**Step 3:** Select target resources.

For example: An EC2 Instance in the Development or Testing environment.

> [!TIP]
> In my opinion, you should not test directly on the Production environment without carefully evaluating the impact.

**Step 4:** Select actions.

For example:

- Stop EC2 Instance.
- Reboot EC2 Instance.
- Stress CPU.

**Step 5:** Configure Stop Conditions. This is a step I find quite important.

It can be configured so the experiment stops automatically if a CloudWatch Alarm changes to the ALARM state, helping to limit the impact if the system encounters unexpected issues.

**Step 6:** Review and create Experiment Template.

**Step 7:** Run the experiment.

After starting, AWS will execute the actions according to the scenario and display the status of each step on the Dashboard.

## Advantages

After researching, I found that AWS FIS has some advantages such as:

- Helps evaluate the fault tolerance of the system in a real-world environment.
- Supports multiple resource types and various experiment scenarios.
- Can integrate with CloudWatch to automatically stop the experiment if a critical issue is detected.
- No need to build custom scripts to inject faults.
- Suitable for testing mechanisms like Auto Scaling, Load Balancing, or Disaster Recovery.

> [!NOTE]
> Proactively testing resilience will help uncover weaknesses before a real incident occurs.

## Some points to note

Besides the advantages above, I also found a few things to consider.

AWS FIS should not be used directly in the Production environment without an appropriate plan and control process. In addition, for the results to be meaningful, the system needs to be monitored using tools like Amazon CloudWatch or AWS X-Ray to observe the impact of each experiment.

Designing experiment scenarios also needs to closely follow situations that could occur in reality, instead of injecting faults randomly.

## When to use it?
In my opinion, AWS FIS is suitable in cases such as:
- Testing the self-healing capability of a system.
- Evaluating Auto Scaling or Load Balancers.
- Testing Disaster Recovery procedures.
- Testing before deploying critical systems.
- Practicing Chaos Engineering in Development or Testing environments.

## Conclusion

After exploring, I find the AWS Fault Injection Service to be quite an interesting service. Instead of just focusing on preventing errors, AWS encourages users to proactively create controlled fault scenarios to assess system resilience.

This is an approach I had never thought of before. If given the opportunity to work with large systems or high availability requirements, I think AWS FIS would be a tool worth learning more about.

If you or anyone else has used AWS FIS or has experience with Chaos Engineering, I would love to hear more about real-world scenarios to discuss together.

## References
1. [AWS Fault Injection Service – Features](https://aws.amazon.com/fis/features/)
2. [AWS Well-Architected Framework – Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/)
3. [AWS Fault Injection Service Pricing](https://aws.amazon.com/fis/pricing/)
4. [AWS Documentation – AWS Fault Injection Service](https://docs.aws.amazon.com/fis/latest/userguide/what-is.html)