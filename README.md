```markdown
# 🛠️ DevSecOps Lab

![Static Badge](https://img.shields.io/badge/!%5BAnsible%5D(https%3A%2F%2Fimg.shields.io%2Fbadge%2Fautomation-ansible-%2523EE0000%3Flogo%3Dansible%26logoColor%3Dwhite))
![Static Badge](https://img.shields.io/badge/!%5BK3s%5D(https%3A%2F%2Fimg.shields.io%2Fbadge%2Fkubernetes-K3s-blue%3Flogo%3Dkubernetes))
![Static Badge](https://img.shields.io/badge/!%5BStatus%5D(https%3A%2F%2Fimg.shields.io%2Fbadge%2Fstatus-active-brightgreen))
![Static Badge](https://img.shields.io/badge/%20%20%20!%5BLicense%5D(https%3A%2F%2Fimg.shields.io%2Fbadge%2Flicense-MIT-blue))


A fully automated, multi-VM **DevSecOps Lab** powered by **Vagrant**, **Ansible**, and **K3s**. It includes:

- 📦 LAMP-based WordPress app
- ☕ Java app server (Tomcat)
- 📊 Monitoring stack (Prometheus + Grafana)
- 🚀 CI/CD node for future automation


---

## 🚀 Features

- ✅ Spin up 4 VMs using Vagrant
- ✅ Deploy apps using Ansible roles
- ✅ Use a K3s cluster for lightweight Kubernetes automation
- ✅ Automate app deployment (WordPress, Java WAR)
- ✅ Ready for CI/CD integration
- ✅ Infrastructure as Code (IaC) ready for GitOps workflows

---

## 🧱 Tech Stack

| Layer            | Tools                     |
|------------------|---------------------------|
| VM Provisioning  | Vagrant + VirtualBox      |
| Configuration    | Ansible                   |
| Web Apps         | WordPress (LAMP), Java WAR|
| Monitoring       | Prometheus + Grafana      |
| Kubernetes       | K3s                       |
| Security         | Lynis, UFW (optional)     |

---

## 📁 Directory Structure

```

devsecops-lab/
├── Vagrantfile
├── inventory/
│   └── hosts.ini
├── playbooks/
│   ├── deploy\_apps.yml
│   ├── harden.yml
│   └── roles/
│       ├── wordpress/
│       └── java\_app/
├── k3s/
│   └── helm-charts/
├── ci-cd/
│   └── jenkins/
└── README.md

````

---

## ⚡ Quick Start

### 1. 🔧 Clone the repo

```bash
git clone https://github.com/your-username/devsecops-lab.git
cd devsecops-lab
````

### 2. 📦 Start the VMs

```bash
vagrant up
```

### 3. 📡 Deploy WordPress & Java App

```bash
ansible-playbook -i inventory/hosts.ini playbooks/deploy_apps.yml
```

### 4. 🛡️ (Optional) Harden the servers

```bash
ansible-playbook -i inventory/hosts.ini playbooks/harden.yml
```

---

## 🔐 Security

This lab can run **Lynis** audits and enforce **UFW** firewalls. Security roles are modular and can be enabled or customized via `group_vars`.

---

## 🧪 CI/CD (Coming Soon)

* Jenkins setup playbook available in `/ci-cd/jenkins/`
* Future plans include:

  * GitHub Actions runner on `ci-cd-vm`
  * Auto-deploy to `lamp-vm` or `java-vm`

---

## 📊 Monitoring (In Progress)

Prometheus and Grafana Helm charts will be auto-deployed to the K3s cluster on `monitoring-vm`.

---

## 📸 Screenshots (Optional)

> *(Add your screenshots of dashboards, app UIs, etc. here)*

---

## 🤝 Contributing

1. Fork this repo
2. Create a feature branch
3. Submit a pull request

---

## 📜 License

This project is licensed under the MIT License.

---

## 🧠 Author

**Abdelkader — Fullstack DevSecOps Lab Builder**

---

```

---


```
