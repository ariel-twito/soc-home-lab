# SOC Home Lab

A virtual security-operations lab I built to practice detection, monitoring

and incident investigation — hands-on, not just theory.

## Environment

- Hypervisor: VMware Workstation / VirtualBox

- Machines: Kali Linux (attacker), Windows 10 (victim/endpoint),
  Metasploitable 2 (vulnerable target), Android VM

- Network: isolated host-only lab network

## What I practice here

| Area | Tools | Examples |
|------|-------|----------|
| Traffic analysis | Wireshark | Following TCP streams, spotting C2 beacons, MITM artifacts |
| Scanning & recon | Nmap | Service/version detection, scan-type comparison from the defender's side |
| Log monitoring | Splunk | Ingesting Windows/Linux logs, writing searches, alert triage |
| File analysis | VirusTotal | Static checks on suspicious samples |
| Attack simulation | Metasploit, Burp Suite | Exploiting Metasploitable, then finding the traces in logs |

## Sample investigation

Malware analysis & incident response exercise: identified the C&C server from packet captures, located registry persistence, and decrypted a ransomware-encrypted file to recover the flag.

## Roadmap

- [ ] Add Suricata IDS and write custom rules

- [ ] Document investigations as write-ups in /writeups

- [ ] Windows event log deep-dive (Sysmon)
