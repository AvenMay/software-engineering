# Cloud

## 🗂️ 云计算全局 Keyword List (自下而上架构拆解)

这份 List 按照从底层硬件抽象到上层服务交付的逻辑排列，可以直接作为你构建“云安全/云架构” Wiki 的一级和二级目录：

#### L0: 基础设施与虚拟化基石 (Infrastructure & Virtualization)

这是云的物理底座，也是从 HomeLab 等本地虚拟化环境向云端延伸的桥梁。

- **Hypervisor (虚拟机监控器):** Type 1 (Bare-metal) vs. Type 2
- **Compute Virtualization:** KVM, Xen, QEMU
- **OS-Level Virtualization:** LXC (Linux Containers), cgroups, namespaces
- **Software-Defined Networking (SDN):** OpenFlow, VXLAN, NVGRE
- **Software-Defined Storage (SDS):** Ceph, GlusterFS

#### L1: 云部署与服务模型 (Cloud Models)

云的商业和交付抽象。

- **Deployment Models:** Public Cloud, Private Cloud, Hybrid Cloud, Multi-Cloud
- **Service Models:**
  - **IaaS (基础设施即服务):** 提供计算、存储、网络原语。
  - **PaaS (平台即服务):** 提供运行环境和数据库引擎。
  - **SaaS (软件即服务):** 提供最终应用。
  - **FaaS / Serverless (函数即服务):** 按调用次数计费的无状态计算。

#### L2: 核心云原生组件 (Core Cloud Capabilities)

无论哪家云厂商（AWS/阿里云/腾讯云），底层都离不开这三大件的 API 化。

- **Compute (计算):**
  - VM Instances (虚拟机实例)
  - Auto Scaling Groups (弹性伸缩组)
- **Networking (网络 - 极其重要):**
  - **VPC (Virtual Private Cloud - 虚拟私有云):** 云上网络隔离的绝对边界。
  - Subnets (Public/Private 子网), CIDR
  - NAT Gateway, Internet Gateway
  - Load Balancing: L4 (TCP/UDP) vs. L7 (HTTP/HTTPS)
  - Security Groups & Network ACLs (无状态与有状态防火墙)
- **Storage (存储):**
  - Block Storage (块存储 - 挂载给 VM 的硬盘)
  - Object Storage (对象存储 - 通过 HTTP/API 访问的扁平文件，如 S3)
  - File Storage (文件存储 - 支持 NFS/SMB 协议的共享存储)

#### L3: 高可用与系统架构 (Resilience & Architecture)

系统对抗熵增和物理硬件故障的设计模式。

- **Geographic Distribution:** Region (地域) vs. Availability Zone (AZ - 可用区)
- **Disaster Recovery (容灾):** RTO (恢复时间目标), RPO (恢复点目标)
- **Control Plane vs. Data Plane (控制面与数据面分离):** 现代云架构的命脉所在。
- **Infrastructure as Code (IaC):** 将上述所有组件用声明式代码（如 Terraform 语法）进行版本化管理。

#### L4: 身份与边界安全 (Cloud Security Posture)

在云上，网络不再是唯一的边界，身份才是。

- **IAM (Identity and Access Management):** Roles, Policies, RBAC (基于角色的访问控制)
- **Zero Trust (零信任):** 不信任任何内部网络，每次访问都需验证。
- **KMS (Key Management Service):** 硬件安全模块 (HSM) 级别的密钥管理。

------

如果要把这套理论体系映射到你当前的知识库建设中，你倾向于先用通用的标准（如 NIST）把概念搭全，还是直接挑选一个开源的云环境（比如用 PVE 模拟一个小型的 VPC 网络）进行自下而上的实操验证？


