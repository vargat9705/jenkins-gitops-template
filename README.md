### **1. Core Components**
- **Jenkins**: Main application deployed in **Kubernetes** for CI/CD.
- **GitHub Repository**: Manages the infrastructure as code using **GitOps** principles.
- **ArgoCD**: Handles **continuous deployment** of infrastructure changes.
- **Terraform**: Used to **provision** all infrastructure resources within Kubernetes.
---

### **2. Deployment Flow**
1. **Pull Request (PR) for Infrastructure Changes**
    - ArgoCD **automatically deploys a staging Jenkins** when a PR is opened.
    - This allows testing changes before they go live.
2. **PR Merged into Master**
    - ArgoCD **deploys changes into production** **only after manual approval**.
    - Ensures changes are reviewed before affecting live environments.
---

### **3. Monitoring & Logging**
- **Prometheus & Grafana** → **Monitor Jenkins performance and metrics**.
- **Loki & Grafana** → **Collect and visualize Jenkins logs**.
---

### **4. Tooling & Technologies Used**
| Component | Tool Used |
| ----- | ----- |
| **CI/CD** | Jenkins |
| **GitOps** | ArgoCD |
| **Infra as Code** | Terraform |
| **Monitoring** | Prometheus + Grafana |
| **Logging** | Loki + Grafana |
---

This setup ensures a **controlled, automated, and observable CI/CD pipeline** for Jenkins while following **GitOps** best practices. 🚀



app of apps
helm umbrella
argocd vault plugin for secret management
