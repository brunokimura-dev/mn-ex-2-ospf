# OSPF Routing with Mininet and Quagga

## Prerequisites

This setup requires:
- [https://github.com/brunokimura-dev/mininet-vagrant](https://github.com/brunokimura-dev/mininet-vagrant)

---

## Setup Instructions

### 1. Launch and Access the Vagrant VM

Navigate to the Vagrant directory and reload the virtual machine:

```bash
cd ~/mininet-vagrant/Vbox/
vagrant reload
vagrant ssh
```

---

### 2. Install Quagga (Routing Daemon)

Inside the VM, install the Quagga routing package:

```bash
sudo apt-get update
sudo apt-get install -y quagga
```

---

### 3. Clone This Repository

Navigate to your working directory and clone the repository:

```bash
cd /workstation/
git clone https://github.com/brunokimura-dev/mn-ex-2-ospf.git
cd mn-ex-2-ospf/
```

---

### 4. Run the Mininet Topology

Use the provided wrapper script to launch the Mininet topology with the desired configuration script:

```bash
sh mininet_run.sh mn-ex-2.py
```

---

## Customization

### Modify OSPF Configuration

To edit the OSPF routing behavior for a router (e.g., `r1`), edit its configuration file:

```bash
nano r1.ospf.conf
```

Repeat similarly for other routers (`r2.ospf.conf`, etc.).

---

### Modify Network Topology

To change the network structure or behavior, modify the Mininet script:

```bash
nano mn-ex-2.py
```


