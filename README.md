# 👋 Ravi Sankar Manem

**Backend Engineer | Security-Focused Systems Builder**

I build backend systems with a focus on **correctness, reliability, security, and observability**.

My primary engineering interests are **Java backend development, secure API design, transactional systems, distributed services, runtime security, audit infrastructure, and security analytics**.

I also work on research-oriented systems involving **graph neural networks, explainable AI, and AI-assisted security analysis**.

Currently exploring **distributed systems, advanced JVM internals, JVM instrumentation, AI runtime security, graph-based security analytics, and digital forensics**.

---

## 🚀 Featured Engineering Projects

### 💳 FinCore — Secure Payment Processing Platform

**Java 21, Spring Boot, PostgreSQL, JWT, Grafana k6**

A secure financial transaction backend focused on **transaction correctness, idempotency, concurrency control, and double-entry accounting**.

* Architected a Java-based transaction engine with PostgreSQL persistence and REST APIs for wallet transfers.
* Implemented **idempotency-key handling** so retries return the original transaction result instead of executing duplicate money movement.
* Prevented concurrent-transfer deadlocks using **PostgreSQL pessimistic locking with deterministic wallet-ID lock ordering**.
* Built a **double-entry ledger** for debit and credit movements with transactional validation across wallet and ledger records.
* Load-tested authenticated APIs with **1,000 virtual users across 25 wallets**, processing **50,682 requests at 281.56 requests/sec with 0% HTTP failures**.
* Designed the system around consistency, failure handling, concurrency safety, and auditable transaction state.

🔗 GitHub: https://github.com/ravimnm/fincore-payment-platform

---

### 🛡️ Secure Multi-Tenant Audit Platform (SMTAP)

**Java 21, Spring Boot, Angular, PostgreSQL, Docker**

A production-inspired microservices platform for **multi-tenant audit logging, tamper detection, security monitoring, investigation timelines, and compliance workflows**.

* Built four independently deployable Spring Boot services: **API Gateway, Auth, Audit, and Security**.
* Implemented **tamper-evident audit storage using SHA-256 hash chaining**, where each audit event cryptographically links to the previous event.
* Added integrity verification to detect modification of historical audit records.
* Optimized tenant-scoped audit retrieval using a PostgreSQL composite index on **`(tenant_id, timestamp)`**, achieving **0.05 ms indexed query execution** against **18.25 ms insert latency**.
* Load-tested the API Gateway with **1,000 virtual users**, sustaining **316 requests/sec at 95% success**.
* Used load-test results to identify application-level concurrency saturation and added **JUnit/Mockito test coverage** for backend services.
* Designed the platform around tenant isolation, auditability, integrity verification, and operational visibility.

🔗 GitHub: https://github.com/ravimnm/secure-multi-tenant-audit-platform

---

### ⛓️ Risk-Aware GraphSAGE for Blockchain Wallet Risk Prediction

**Python, PyTorch, PyTorch Geometric, GNNExplainer**

A collaborative academic research project applying **graph neural networks to blockchain wallet risk prediction** using the Elliptic++ Bitcoin transaction graph.

* Built a **GraphSAGE-based wallet classifier** combining wallet-level features with transaction-neighbor representations.
* Extended the baseline architecture with an **adaptive feature gate, residual connection, and focal loss** to address feature relevance and class imbalance.
* Benchmarked the proposed architecture against **GCN, GAT, and vanilla GraphSAGE** using the same dataset split.
* Achieved **94.65% recall and 90.54% F1** on the illicit-wallet class on held-out test data.
* Integrated **GNNExplainer** to identify influential transaction edges and neighboring wallets behind individual predictions.
* Explored graph-aware feature engineering covering transaction flow, wallet behavior, connectivity, and temporal characteristics.
* **Academic team project with three collaborators.**

🔗 GitHub: https://github.com/ravimnm/blockchain-wallet-risk-prediction

---

### 🧠 AI-Based Log Investigation & Cyber-Forensic Analysis

**Python, Scikit-learn, TensorFlow/Keras, SHAP/LIME**

Collaborative academic security project focused on **multi-source log analysis, anomaly detection, threat classification, and explainable investigation workflows**.

* Contributed **end-to-end to the Windows Security Log pipeline** as part of the college mini-project.
* Worked across the Windows pipeline from **log preprocessing and feature engineering through model development, inference, and risk scoring**.
* Engineered behavioral features from Windows security events to identify suspicious activity patterns.
* Applied machine-learning techniques for Windows security-event classification and anomaly detection.
* Integrated model outputs into the broader investigation workflow for security analysis.
* Worked on explainable security analytics to make model-driven detections more interpretable during investigation.
* The overall project combines multiple security-log domains and was developed collaboratively as an academic research project.

**My contribution:** End-to-end Windows log analysis pipeline.

🔗 GitHub: https://github.com/PavitraLaxmi05/AI-Based-Log-Investigation-System

---

### 🛡️ Java Runtime Security Agent (JRSA)

**Java, ByteBuddy, JVM Instrumentation API**

A zero-code-change JVM security agent for monitoring security-sensitive runtime behavior.

* Built a JVM agent using **ByteBuddy and the Java Instrumentation API** to intercept `Runtime.exec()` calls without modifying the target application.
* Streamed intercepted runtime events into SMTAP for centralized audit and security analysis.
* Investigated JVM instrumentation, class loading, agent lifecycle, and runtime interception behavior.
* Debugged and fixed **recursive instrumentation**, where agent-generated calls re-triggered the interceptor and caused infinite hook recursion.
* Designed the agent as a companion security component to SMTAP for runtime visibility inside Java applications.

🔗 GitHub: https://github.com/ravimnm/java-runtime-security-agent

---

# 🧪 Research & Engineering Interests

My work sits at the intersection of:

* **Backend Engineering**
* **Application & Runtime Security**
* **Security Analytics**
* **Graph Machine Learning**
* **AI Security**
* **Observability & Auditability**
* **Systems Engineering**

I am particularly interested in systems where security properties must be enforced through architecture rather than added as an afterthought.

---

# 🛠️ Core Skills

### Backend Engineering

Java, Spring Boot, REST APIs, Spring Security, JWT, Spring Data JPA, Microservices, API Integration, JSON

### Databases

PostgreSQL, MySQL, MongoDB, SQL, Joins, Subqueries, Indexing, Data Validation

### Systems Engineering

JVM Internals, JVM Instrumentation, Bytecode Manipulation, Concurrency, OOP, SOLID Principles, Design Patterns, Debugging, Performance Optimization, Scalability

### Security & Observability

Runtime Security, Audit Logging, Threat Detection, Security Monitoring, SIEM Fundamentals, ELK Stack, MITRE ATT&CK, Secure API Design

### Machine Learning & AI

Scikit-learn, PyTorch, PyTorch Geometric, Random Forest, Isolation Forest, GraphSAGE, GNNExplainer, SHAP, LIME, Feature Engineering

### Infrastructure & Tooling

Linux/Unix, Shell Scripting, Docker, AWS EC2, Maven, Git, GitHub, Postman, JUnit, Mockito, Grafana k6

### Computer Science

Data Structures & Algorithms, OOP, DBMS, Operating Systems, Computer Networks, Collections, Exception Handling, Concurrency, Software Design

---

# 🔬 Currently Exploring

* Advanced JVM Internals & Instrumentation
* Distributed Systems & System Design
* Secure Backend Architecture
* AI Runtime Security
* Graph-Based Security Analytics
* Digital Forensics & Incident Response
* Scalable Java Backend Systems

---

# 🏆 Engineering & Open Source

### Teckzite 2K25 — Backend Engineering

Extended and maintained the backend of the festival's MERN-based event management platform.

* Implemented REST APIs for participant registration, event management, scheduling, and operational workflows.
* Removed obsolete functionality and improved backend workflows.
* Supported **6,000+ participants across 20+ events** during the live festival.

### Graylog — Open Source Contribution

Contributed to the Graylog Java codebase through **PR #26673**.

* Updated `NodeMetricPeriodical` to honor `disable_native_system_stats_collector`.
* Prevented unnecessary OSHI/JNA native-system-statistics initialization when native collection is disabled.

---

# 📚 Data Structures & Algorithms

**214 LeetCode problems solved**

* **67 Easy**
* **132 Medium**
* **15 Hard**

### Strong areas

* Arrays
* Hash Tables
* Two Pointers
* Strings
* Binary Search
* Trees
* Dynamic Programming
* Backtracking
* Divide and Conquer

LeetCode: https://leetcode.com/u/ravimnm28/

---

# 🎓 Education

**B.Tech — Computer Science & Engineering**

Rajiv Gandhi University of Knowledge Technologies, Nuzvid

**Expected Graduation:** May 2027
**CGPA:** 8.53 / 10.0

---

# 📜 Certifications

* Oracle Generative AI Certificate
* NPTEL — Artificial Intelligence
* NPTEL — Deep Learning

---

# 🌐 Connect

* **GitHub:** https://github.com/ravimnm
* **LinkedIn:** https://linkedin.com/in/ravi-sankar-manem
* **LeetCode:** https://leetcode.com/u/ravimnm28/
* **Email:** [manemravisankar28@gmail.com](mailto:manemravisankar28@gmail.com)

---

## 💻 Core Technologies

![Java](https://img.shields.io/badge/Java-21-%23ED8B00?style=for-the-badge\&logo=openjdk\&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge\&logo=springboot\&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge\&logo=postgresql\&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge\&logo=mongodb\&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge\&logo=docker\&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge\&logo=amazonaws\&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge\&logo=pytorch\&logoColor=white)

---

## 🔐 Security & Observability

![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge\&logo=elasticsearch\&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge\&logo=linux\&logoColor=black)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge\&logo=postman\&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge\&logo=grafana\&logoColor=white)

---

## ⚙️ Development & Tooling

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge\&logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge\&logo=github\&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge\&logo=githubactions\&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge\&logo=apachemaven\&logoColor=white)
![JUnit](https://img.shields.io/badge/JUnit-25A162?style=for-the-badge\&logo=junit5\&logoColor=white)

---

## 📊 GitHub Statistics

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=ravimnm\&show_icons=true\&theme=dark\&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=ravimnm\&layout=compact\&theme=dark\&hide_border=true)

---

<!-- Recruiter-focused profile: backend engineering, security systems, and research-oriented projects. -->
