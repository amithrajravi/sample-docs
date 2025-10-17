# 👋 Hi, I'm Amithraj Ravi

<div align="center">
  
![Profile Views](https://komarev.com/ghpvc/?username=amithraj&color=blueviolet&style=flat-square&label=Profile+Views)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/amithraj)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:raj07tw@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://github.com/amithraj)

</div>

## 🚀 About Me

```bash
$ whoami
amithraj@devdocs:~$ echo "Passionate Technical Writer & Developer Documentation Specialist"
Passionate Technical Writer & Developer Documentation Specialist

$ cat /etc/passwd | grep amithraj
amithraj:x:1000:1000:Amithraj Ravi,Senior Technical Writer,raj07tw@gmail.com:/home/amithraj:/bin/bash

$ ls -la ~/skills/
drwxr-xr-x 1 amithraj amithraj 4096 Dec 2024 cloud-devops/
drwxr-xr-x 1 amithraj amithraj 4096 Dec 2024 technical-writing/
drwxr-xr-x 1 amithraj amithraj 4096 Dec 2024 developer-tools/
```

I'm a **Senior Technical Writer** with 8+ years of experience specializing in **Cloud, DevOps, and Software Delivery** documentation. I transform complex technical concepts into clear, actionable developer guides that make technology accessible to everyone.

## 💼 Professional Experience

### 🐸 **JFrog** - Senior Technical Writer
```yaml
location: Bengaluru
duration: "09/2024 - Current"
role: Senior Technical Writer
focus:
  - Self-hosted installation documentation
  - Kubernetes & Helm charts deployment
  - Docker, Debian, RPM installations
  - AI-powered documentation with Gemini
```

### 🔧 **Digital.ai** - Senior Technical Writer Grade 2
```yaml
location: Bengaluru
duration: "02/2022 - 09/2024"
role: Senior Technical Writer Grade 2
focus:
  - DevOps & CI/CD documentation
  - REST API documentation
  - Release orchestration guides
  - Docs-as-code implementation
```

### 🏭 **Honeywell Technology Solutions** - Senior Technical Writer
```yaml
location: Bengaluru
duration: "12/2016 - 02/2022"
role: Senior Technical Writer
focus:
  - Cloud platform documentation
  - UI reference guides
  - Agile documentation processes
```

## 🛠️ Technical Arsenal

### 📝 **Documentation & Writing**
```bash
$ which markdown dita yaml xml html css
/usr/bin/markdown    # Markdown mastery
/usr/bin/dita        # DITA XML expertise
/usr/bin/yaml        # YAML configuration
/usr/bin/xml         # XML authoring
/usr/bin/html        # HTML/CSS styling
```

### ☁️ **Cloud & DevOps Technologies**
```bash
$ kubectl get nodes
NAME           STATUS   ROLES           AGE   VERSION
aws-node-1     Ready    master,worker   2y    v1.28.0
docker-node-2  Ready    worker          2y    v1.28.0

$ docker ps
CONTAINER ID   IMAGE                    COMMAND                  CREATED
a1b2c3d4e5f6   jfrog/artifactory:7.x   "/entrypoint.sh"        2 months ago
b2c3d4e5f6a7   apache/kafka:latest      "kafka-server-start.sh" 1 month ago

$ helm list
NAME            NAMESPACE       REVISION    STATUS      CHART
artifactory     jfrog          1           deployed    artifactory-7.68.0
kafka-cluster   kafka          1           deployed    kafka-22.1.0
```

### 🔧 **Development Tools**
```python
# Python scripting for documentation automation
import yaml
import markdown
from pathlib import Path

def generate_docs_from_api_spec(api_spec_path):
    """Generate API documentation from OpenAPI spec"""
    with open(api_spec_path, 'r') as file:
        spec = yaml.safe_load(file)
    
    # Process API endpoints
    for endpoint in spec['paths']:
        create_endpoint_docs(endpoint, spec['paths'][endpoint])

# Java for SDK documentation
public class APIDocumentationGenerator {
    public void generateSDKReference(String packageName) {
        // Generate SDK reference documentation
        DocumentationBuilder builder = new DocumentationBuilder();
        builder.addPackage(packageName);
        builder.generateMarkdown();
    }
}
```

## 📚 Featured Documentation Projects

### 🔗 **Web Services Architecture**
**[SOAP vs REST: Complete Developer Guide](docs/soap-vs-rest.md)**
```bash
$ curl -X GET "https://api.example.com/services" \
  -H "Accept: application/json" \
  -H "Content-Type: application/json"

# Response: REST API documentation
{
  "service": "REST API",
  "format": "JSON",
  "transport": "HTTP",
  "advantages": ["Lightweight", "Cacheable", "Stateless"]
}
```

### 🛡️ **API Management & DevOps**
**[APIMAN Implementation Guide](docs/api-management-apiman.md)**
```yaml
# apiman-config.yaml
apiVersion: apiman.io/v1alpha1
kind: APIManager
metadata:
  name: production-api-manager
spec:
  gateway:
    replicas: 3
    resources:
      requests:
        memory: "512Mi"
        cpu: "250m"
  security:
    authentication:
      type: "oauth2"
    authorization:
      policies: ["rate-limiting", "cors"]
```

### 🐳 **Container & Kubernetes Documentation**
```bash
# Helm installation for JFrog Artifactory
$ helm repo add jfrog https://charts.jfrog.io
$ helm repo update
$ helm install artifactory jfrog/artifactory \
  --namespace jfrog \
  --create-namespace \
  --values values.yaml

# Verify installation
$ kubectl get pods -n jfrog
NAME                           READY   STATUS    RESTARTS   AGE
artifactory-0                  1/1     Running   0          5m
nginx-7d4f8b9c5d-xyz12        1/1     Running   0          5m
```

## 🏆 Achievements & Recognition

```bash
$ cat ~/achievements.txt
🏆 Hall of Fame - Team Award (Harman)
⭐ Going the Extra Mile - Individual Award (Harman)
🌟 Become Your Best - Star Award (Honeywell)
🚀 Go Beyond - Star Award (Honeywell)
⚡ Act with Urgency - Bronze Award (Honeywell)
```

## 📖 Technical Writing Philosophy

```markdown
# My Documentation Approach

## 🎯 Audience-First Design
- **Developers**: Clear API references and code examples
- **DevOps Engineers**: Step-by-step installation guides
- **IT Administrators**: Configuration and troubleshooting docs

## 🔄 Docs-as-Code Workflow
```bash
# Documentation development process
$ git checkout -b feature/new-api-docs
$ vim docs/api-reference.md
$ git add docs/api-reference.md
$ git commit -m "docs: Add REST API reference"
$ git push origin feature/new-api-docs
# → Triggers automated review and publishing
```

## 🧪 Testing-Driven Documentation
- Install and test every feature before documenting
- Validate code examples and API calls
- Verify installation procedures in multiple environments
```

## 🎯 Current Focus & Learning

```bash
$ ps aux | grep amithraj
amithraj  1234  0.1  2.3  exploring-microservices-architecture
amithraj  1235  0.2  1.8  implementing-ai-powered-docs
amithraj  1236  0.0  1.2  learning-gitops-patterns
amithraj  1237  0.3  2.1  creating-interactive-tutorials
```

- 🔍 **Microservices Architecture** - Documenting distributed systems patterns
- 🤖 **AI-Powered Documentation** - Leveraging Gemini and ChatGPT for content generation
- 🚀 **GitOps Documentation** - Streamlining deployment documentation
- 📱 **Interactive Tutorials** - Creating hands-on learning experiences

## 📊 Documentation Metrics

<div align="center">
  
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=amithraj&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=amithraj&layout=compact&theme=tokyonight&hide_border=true)

</div>

## 🤝 Let's Connect!

```bash
$ echo "Ready to collaborate on amazing documentation projects!"
Ready to collaborate on amazing documentation projects!

$ contact --method=linkedin --profile=amithraj
$ contact --method=email --address=raj07tw@gmail.com
$ contact --method=phone --number="+91-9361061776"
```

<div align="center">
  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/amithraj)
[![Email](https://img.shields.io/badge/Email-Contact-red?style=for-the-badge&logo=gmail)](mailto:raj07tw@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-Download-green?style=for-the-badge&logo=adobe-acrobat-reader)](resume.pdf)

</div>

---

<div align="center">
  
**⭐ Star this repository if you found the documentation helpful!**

```bash
$ echo "Last updated: $(date '+%B %Y')"
Last updated: December 2024
```

</div>