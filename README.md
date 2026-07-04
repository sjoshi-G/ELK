# ELK

Welcome to my ELK Security Operations Center (SOC) Lab project!
This lab shows how I used the ELK Stack (Elasticsearch, Logstash, Kibana) to collect, analyze, and visualize security logs from Linux systems. I built this project to learn how real SOC analysts monitor systems, detect suspicious activity, and investigate incidents.


This project demonstrates how security logs flow from computers (Linux) into a SIEM system (ELK), where they can be searched, visualized, and used to detect attacks.

I set up:
Filebeat to send Linux logs to ELK
Kibana dashboards to visualize activity
Simulated attacks like brute force
Incident investigation reports based on real logs

This is a complete beginner‑friendly SOC lab that shows how security monitoring works in real life.

Tools Used
Elasticsearch – stores the logs
Logstash – processes logs
Kibana – dashboards and visualizations
Filebeat – sends Linux logs to ELK

Ubuntu Linux VM

Log sources

Windows Logs: Failed login attempts
Linux Logs : Sudo usage

Dashboards included
Authentication failure panels
Linux Sudo activity
