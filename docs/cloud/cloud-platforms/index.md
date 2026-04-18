# ☁️ Cloud Platforms

## Books

- [云计算 概念、技术与架构.pdf]({{ files_server }}/cloud/cloud-platforms/current/%E4%BA%91%E8%AE%A1%E7%AE%97%20%E6%A6%82%E5%BF%B5%E3%80%81%E6%8A%80%E6%9C%AF%E4%B8%8E%E6%9E%B6%E6%9E%84.pdf)


## 🔬 云计算基础层级与模型 (Foundational Layers & Models)

本节清晰界定云计算的不同服务层级，并明确基础设施的边界。

### 1. 常见的云计算服务层级

云计算服务通常分为以下层级：

| 服务层级 | 英文缩写 | 核心概念 | 实例 |
| :--- | :--- | :--- | :--- |
| **软件即服务** | **SaaS** | 最终用户直接使用的软件，无需管理底层架构。 | 微信、Office 365、Salesforce |
| **平台即服务** | **PaaS** | 提供了应用开发和运行所需的完整环境（操作系统、数据库、中间件）。 | AWS Elastic Beanstalk、Google App Engine |
| **基础设施即服务** | **IaaS** | 提供了基础的计算资源（虚拟机、存储、网络）。 | AWS EC2、Azure VM、OpenStack |
| **数据即服务** | **DaaS** | 按需提供的在线数据服务和数据仓库。 | Snowflake、Amazon Redshift |
| **后端即服务** | **BaaS** | 为移动和Web应用提供后端功能（用户认证、推送通知等）。 | Firebase、AWS Amplify |

### 2. 基础设施层的边界与核心

在上述模型中，**IaaS（基础设施即服务）**是云计算平台的**核心基础层级**。

> **🎯 核心聚焦：** **IaaS** 关注的是计算、存储、网络等**底层资源**的虚拟化和按需交付，这是**私有云和公有云平台（如 OpenStack, AWS）**工作的核心。PaaS 在 IaaS 的基础上添加了操作系统和运行环境，而 SaaS 则位于顶层。

### 3. 应用层与云原生 (The Application Layer)

应用层，即 SaaS 或用户自行开发的应用，虽然是用户感知“云”的主要方式，但**它并不是云计算平台本身的核心**。

> **通俗讲解：** > 
> * **云平台**（IaaS/PaaS）就像一座现代化的**超级公寓楼**，负责供水、供电、安全和电梯。
> * **应用**（SaaS）就像公寓楼里各种**定制的家具和电器**。
> 
> 虽然应用可以围绕云平台进行**云原生 (Cloud-Native)** 设计（例如，使用容器、微服务），这使得应用更灵活、可扩展，但应用的**业务逻辑**本身并不能体现云平台的**基础设施**价值，它只是更好地**利用**了云平台提供的能力。

---

## 💻 公有云平台 (Public Cloud Platforms)

主流公有云提供商的技术栈和核心服务解析。

* **[AWS (Amazon Web Services)](public/aws.md)** | S3 存储、EC2 计算、Lambda 无服务器架构。
* **[Microsoft Azure](public/azure.md)** | 与 Microsoft 生态的集成、Azure Arc 在混合云中的作用。
* **[GCP (Google Cloud Platform)](public/gcp.md)** | Kubernetes (GKE)、BigQuery、AI/ML 服务。

---

## 🏰 私有云与虚拟化 (Private Cloud & Virtualization)

私有云平台的架构、部署方案和关键技术。

* **[Open Source vs. Proprietary](private/open_source_vs_commercial.md)** | 私有云方案中商业与开源（如 VMware vs. OpenStack）的选择与权衡。
* **[OpenStack 深入分析](private/openstack.md)** | 核心组件 (Nova, Neutron, Cinder) 架构详解。
* **[CloudStack vs. OpenStack vs. PVE](private/cloudstack_vs_pve.md)** | 三者在易用性、扩展性和功能集上的对比。

---

## 🔗 混合云与多云策略 (Hybrid & Multi-Cloud)

连接不同云环境的技术与管理策略。

* **[混合云架构实践](hybrid/hybrid_architecture.md)** | 公有云延伸产品（AWS Outposts, Azure Stack Hub）。
* **[多云管理与应用迁移](hybrid/multicloud_management.md)** | 使用 Kubernetes 进行跨云应用编排（Anthos, OpenShift）。

---

## 🛠️ 运维与自动化 (Operations & Automation)

在云环境中实现高效运维的技术和工具。

* **[基础设施即代码 (IaC)](ops/iac.md)** | Terraform、Ansible、Pulumi 的使用。
* **[云安全与合规](ops/security_compliance.md)** | 身份与访问管理 (IAM) 实践。


