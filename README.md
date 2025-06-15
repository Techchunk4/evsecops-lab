```markdown
# 🛠️ DevSecOps Lab

![Ansible](https://img.shields.io/badge/automation-ansible-%23EE0000?logo=ansible&logoColor=white)
![K3s](https://img.shields.io/badge/kubernetes-K3s-blue?logo=kubernetes)
![Status](https://img.shields.io/badge/status-active-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

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

Would you like me to:

- Add GitHub Actions CI badge?
- Auto-generate a diagram (e.g., network + app layout)?
- Push it to a GitHub repo for you with `.gitignore`, `LICENSE`, etc.?

Let’s take it to pro level!
```
