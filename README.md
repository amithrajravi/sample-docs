# 👋 Hi, I'm Amithraj Ravi

## 📚 Docs

- APIMAN Implementation Guide: [View as webpage](docs/api-management-apiman.html)
- SOAP vs REST: [View as webpage](docs/soap-vs-rest.html)

## 🚀 About Me

I'm a **Senior Technical Writer** with over 12 years of experience, specializing in making complex technology accessible through clear, actionable documentation. My passion lies in transforming intricate technical concepts into user-friendly guides that help developers, DevOps engineers, and IT administrators succeed.

**What I do best:**
- 📝 Create comprehensive developer documentation
- 🔧 Write installation and configuration guides
- 🚀 Document API references and SDKs
- ☁️ Explain Cloud and DevOps concepts
- 🛠️ Build documentation workflows and processes

## 💼 Professional Journey

### 🐸 **JFrog** - Senior Technical Writer
**📍 Bengaluru | 🕒 September 2024 - Present**

At JFrog, I focus on creating documentation for self-hosted installations and deployments. My work includes:

- **Kubernetes & Helm Charts**: Writing guides for deploying JFrog products in containerized environments
- **Multi-Platform Installations**: Documenting installation procedures for Docker, Debian, RPM, Linux, and Windows
- **AI-Powered Documentation**: Leveraging Gemini AI to create custom documentation tools and verification processes
- **Release Management**: Creating comprehensive release notes for major, minor, and patch releases

### 🔧 **Digital.ai** - Senior Technical Writer Grade 2
**📍 Bengaluru | 🕒 February 2022 - September 2024**

During my time at Digital.ai, I specialized in DevOps and software delivery documentation:

- **DevOps Documentation**: Created guides for CI/CD pipelines and release orchestration
- **API Documentation**: Collaborated with development teams to document REST APIs
- **Docs-as-Code**: Implemented modern documentation workflows using VS Code, Git, and GitHub Actions
- **Agile Integration**: Aligned documentation timelines with development sprints

### 🏭 **Honeywell Technology Solutions** - Senior Technical Writer
**📍 Bengaluru | 🕒 December 2016 - February 2022**

At Honeywell, I developed expertise in cloud platform documentation:

- **Cloud Platform Guides**: Created comprehensive user guides for Movilizer Cloud components
- **UI Documentation**: Developed reference materials and instruction pages
- **Agile Collaboration**: Participated in scrum meetings and daily stand-ups with engineering teams

### 🎵 **Harman Connected Services** - Technical Writer
**📍 Bengaluru | 🕒 April 2015 - December 2016**

During my time at Harman, I built foundational skills in technical documentation:

- **DITA Documentation**: Created and updated DITA files for various technical guides
- **Project Management**: Used JIRA for documentation story tracking and project management
- **Visual Content**: Edited images and graphics using professional tools like SnagIT
- **Team Collaboration**: Actively participated in weekly project status meetings

### 💼 **Odessa Technologies** - Technical Writer
**📍 Bengaluru | 🕒 February 2013 - April 2015**

At Odessa Technologies, I began my technical writing journey:

- **Help Documentation**: Created comprehensive online help and reference manuals
- **Module Documentation**: Developed documentation for various software modules
- **Stakeholder Collaboration**: Worked closely with Subject Matter Experts (SMEs) for content review
- **Cross-functional Communication**: Interacted with Developers and Business Analysts to gather requirements

## 🛠️ Technical Skills & Tools

### 📝 **Documentation Technologies**
```bash
# My documentation toolkit
$ which markdown dita yaml xml html css
/usr/bin/markdown    # Markdown mastery
/usr/bin/dita        # DITA XML expertise  
/usr/bin/yaml        # YAML configuration
/usr/bin/xml         # XML authoring
/usr/bin/html        # HTML/CSS styling

# Authoring tools I use daily
$ ls -la ~/tools/
drwxr-xr-x 1 amithraj amithraj 4096 cursor AI/
drwxr-xr-x 1 amithraj amithraj 4096 vs-code/
drwxr-xr-x 1 amithraj amithraj 4096 paligo/
drwxr-xr-x 1 amithraj amithraj 4096 confluence/
drwxr-xr-x 1 amithraj amithraj 4096 oxygen-xml/
drwxr-xr-x 1 amithraj amithraj 4096 madcap-flare/
```

### ☁️ **Cloud & DevOps**
```bash
# Check the tools I use (versions shown)
$ aws --version        # Amazon Web Services CLI
$ kubectl version -o yaml | head -n 3   # Kubernetes client
$ docker --version     # Docker

# Simple example: install a chart with Helm
$ helm install artifactory jfrog/artifactory \
  --namespace jfrog --create-namespace
# → Deploys the app to Kubernetes in the 'jfrog' namespace

# Verify that things are running
$ kubectl get pods -n jfrog
# → Pods should show as "Running"
```

### 🔧 **Development & Testing**
```python
# Tiny Python example: turn an API spec into simple docs
import yaml

def list_endpoints(openapi_path):
    with open(openapi_path, "r") as f:
        spec = yaml.safe_load(f)
    for path in spec.get("paths", {}):
        print(f"- Document endpoint: {path}")

list_endpoints("api-spec.yaml")
# → Output: a friendly list you can turn into docs
```

```bash
# Quick API test example (conceptual)
$ curl -s https://api.example.com/health | jq
{
  "status": "ok"
}
# → I validate responses like this before writing the guide

# Using Postman CLI (when available)
$ postman-cli run collection.json --environment production
# → Ensures examples in docs actually work
```

## 📚 Personal Sample Documentation Projects

### 🔗 **Web Services Architecture**
**[SOAP vs REST: Complete Developer Guide](docs/soap-vs-rest.html)**

A comprehensive comparison guide that helps developers choose the right web service architecture for their projects. This documentation covers:

- **Architecture Comparison**: Detailed analysis of SOAP vs REST approaches
- **Use Cases**: Real-world scenarios and decision-making guidelines
- **Performance Analysis**: Technical considerations and best practices
- **Implementation Examples**: Practical code samples and configurations

### 🛡️ **API Management Solutions**
**[APIMAN Implementation Guide](docs/api-management-apiman.html)**

Complete guide for implementing API management solutions, including:

- **Configuration**: Step-by-step setup procedures
- **Security Patterns**: Authentication and authorization best practices
- **Monitoring**: Performance tracking and troubleshooting
- **Integration**: Connecting with existing systems and workflows

## 🏆 Recognition & Achievements

Throughout my career, I've been recognized for my contributions:

- 🏆 **Hall of Fame** - Team Award (Harman)
- ⭐ **Going the Extra Mile** - Individual Award (Harman)
- 🌟 **Become Your Best** - Star Award (Honeywell)
- 🚀 **Go Beyond** - Star Award (Honeywell)
- ⚡ **Act with Urgency** - Bronze Award (Honeywell)

## 📖 My Documentation Philosophy

I believe great documentation should be:

### 🎯 **User-Centric**
- **Developers**: Clear API references with working code examples
- **DevOps Engineers**: Step-by-step installation and configuration guides
- **IT Administrators**: Comprehensive troubleshooting and maintenance documentation

### 🔄 **Process-Driven**
- **Testing First**: Install and test every feature before documenting
- **Version Control**: Use Git workflows for documentation management
- **Continuous Improvement**: Regular updates based on user feedback

### 📱 **Modern Approach**
- **Interactive Elements**: Code snippets, configuration examples, and visual guides
- **Multi-Format**: Supporting various learning styles and preferences
- **Accessibility**: Making technical content understandable for all skill levels

## 🎯 Current Focus & Learning

I'm constantly expanding my knowledge in:

- 🤖 **AI-Powered Documentation** - Exploring AI tools for content generation and verification

## 🤝 Let's Connect!

I'm always excited to discuss new opportunities, technical challenges, and innovative documentation projects. Whether you're looking for technical writing expertise or want to collaborate on documentation initiatives, I'd love to hear from you!

### 📞 **Contact Information**
- **📧 Email**: [raj07tw@gmail.com](mailto:raj07tw@gmail.com)
- **📱 Phone**: +91-9361061776
- **💼 LinkedIn**: [Connect with me on LinkedIn](https://linkedin.com/in/amithrajravi)
- **📍 Location**: Bengaluru, Karnataka, India

### 💬 **What I Can Help With**
- Technical documentation strategy and planning
- API documentation and developer guides
- DevOps and Cloud platform documentation
- Documentation workflow optimization
- Content review and improvement