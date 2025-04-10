# 🛠️ Suricata IDS Setup Steps

## 1. Update and Install Dependencies
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install software-properties-common -y
```

## 2. Add Suricata Repository and Install
```bash
sudo add-apt-repository ppa:oisf/suricata-stable
sudo apt update
sudo apt install suricata -y
```

## 3. Check Network Interfaces
```bash
ip a
```

## 4. Test Suricata Installation
```bash
suricata --build-info
```

## 5. Configure Suricata
```bash
sudo nano /etc/suricata/suricata.yaml
```
- Set the interface in the `af-packet` or `pcap` section (e.g., `eth0`, `ens33`, etc.)

## 6. Download and Update Rules
```bash
sudo suricata-update
```

## 7. Start Suricata in Live Mode
```bash
sudo suricata -c /etc/suricata/suricata.yaml -i <your-interface>
```

## 8. Trigger an Alert (Policy Violation)
```bash
curl http://testmyids.com
```

## 9. View Alerts
```bash
cat /var/log/suricata/fast.log
```
