# 🛡️ Suricata IDS Setup and Configuration on Linux

This project demonstrates how to set up and configure **Suricata**, an open-source Intrusion Detection System (IDS), on a Linux (Ubuntu) system. It includes installation steps, rule integration, alert testing, and log analysis.

---

## 🔧 What I Did

- Installed Suricata on Ubuntu using the official PPA repository.
- Integrated the **Emerging Threats** community ruleset for threat detection.
- Configured Suricata to monitor a live network interface.
- Triggered and validated alerts using simulated HTTP traffic (`curl http://testmyids.com`).
- Analyzed Suricata logs (`fast.log`) to confirm successful detections.

---

## 💡 Skills Practiced

- Network traffic monitoring and analysis  
- Linux command-line usage and service management  
- Open-source IDS deployment and rule integration  
- Real-time alert handling and log analysis  

---

## 📄 Sample Alert

```
[**] [1:2024218:3] ET POLICY curl User-Agent Outbound [**]
```

This alert was generated during testing, confirming that Suricata is actively detecting HTTP user-agent patterns.

---

## 📂 Files in This Repo

- `setup_steps.md` – All steps used to configure and test Suricata  
- `fast.log` – Sample alert log output from Suricata (anonymized)  
- `suricata.yaml` – (Optional) Configuration file (only include safe parts)  

---

## ✅ Next Steps

- Explore integration with the **ELK Stack** for visualizing alerts  
- Practice writing custom Suricata rules  
- Expand detection coverage using PCAP replay and advanced rule sets  

---

## 🧠 Reference

- [Suricata Official Docs](https://docs.suricata.io/)
- [Emerging Threats Rules](https://rules.emergingthreats.net/)
