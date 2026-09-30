# Awesome-Distributed-Order-Management

# Top Distributed Order Management (DOM) Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Omnichannel Order Orchestration, Inventory Sourcing & Fulfillment Optimization*  
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Distributed Order Management (DOM)**. These tools orchestrate order fulfillment across distributed inventory nodes — warehouses, stores, dark stores, and drop-ship partners — using real-time inventory visibility and optimization algorithms to decide what to promise, where to source from, and how to route orders for cost-effective, on-time delivery.

**Examples** include IBM Sterling DOM, Manhattan Active Omni, Kibo Commerce, Fluent Commerce, Oracle DOM, Salesforce OMS, Magento OMS, SAP Order Management, OneStock, and Radial (the category leaders).

**Open-source emphasis**: This section is expanded with active projects for self-hosting, custom order routing logic, and transparent fulfillment orchestration — ideal for retailers, developers, and researchers building vendor-independent DOM solutions. The open-source ecosystem is anchored by **Apache OFBiz** (full ERP/eCommerce/OMS stack), **ecommerce-erp** (cross-border ERP with fulfillment), and a growing set of event-driven microservices reference implementations demonstrating DOM architecture patterns.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[IBM Sterling DOM](https://www.ibm.com/products/sterling-order-management)**  
  Enterprise-grade distributed order management platform for omnichannel fulfillment. Provides real-time inventory visibility, intelligent order sourcing, and fulfillment orchestration across complex supply chain networks.

- **[Manhattan Active Omni](https://www.manh.com/)**  
  Unified commerce platform with DOM capabilities for order orchestration, inventory sourcing, and fulfillment optimization across stores, DCs, and drop-ship partners.

- **[Kibo Commerce](https://kibocommerce.com/)**  
  Composable commerce platform with order management, inventory, and fulfillment capabilities for B2C and B2B retailers.

- **[Fluent Commerce](https://fluentcommerce.com/)**  
  Cloud-native DOM platform specializing in complex omnichannel fulfillment orchestration with real-time inventory and intelligent sourcing.

- **[Oracle DOM](https://www.oracle.com/)**  
  Distributed order management within Oracle Retail and Oracle Fusion Cloud, providing order orchestration and fulfillment optimization.

- **[Salesforce OMS](https://www.salesforce.com/)**  
  Order Management System within Salesforce Commerce Cloud, enabling omnichannel fulfillment and inventory visibility.

- **[Magento OMS](https://business.adobe.com/products/magento/magento-commerce.html)**  
  Order management capabilities within Adobe Commerce (Magento), with extensions for distributed fulfillment.

- **[SAP Order Management](https://www.sap.com/products/order-management.html)**  
  Cloud-native, composable order management solution for omnichannel order orchestration, inventory visibility, and fulfillment management. Named a Leader in the IHL Group Order Management Market 2025 report . Includes AI capabilities (Joule copilot, Order Reliability Agent) and low-code/no-code process customization .

- **[OneStock](https://www.onestock-retail.com/)**  
  European DOM platform for omnichannel retailers with order routing, inventory unification, and fulfillment optimization.

- **[Radial](https://www.radial.com/)**  
  Order management and fulfillment solutions for retailers, including distributed order management and omnichannel capabilities.

## Open-Source GitHub Projects

- **[Apache OFBiz](https://ofbiz.apache.org/)**  
  The most mature open-source ERP with integrated eCommerce, PIM, CMS, OMS, and WMS capabilities. Has been used for over a decade to build eCommerce stores and service online retail businesses . For organizations starting fresh without legacy systems, OFBiz can serve as the complete stack (PIM, eCommerce API, OMS, WMS) without additional development or maintenance effort. For established brands with legacy platforms, OFBiz can function as the OMS layer integrated with existing PIM, sales channels, WMS, and ERP systems . Features include real-time inventory visibility, order routing based on defined strategies, order splitting for faster fulfillment, BOPIS/BORIS/Endless Aisle support, and preorder/backorder management . No vendor lock-in, no licensing costs, and backed by the Apache Software Foundation.

- **[ecommerce-erp](https://developer.aliyun.com/article/1753673)**  
  Open-source cross-border e-commerce ERP built with ThinkPHP, Vue, MySQL, and Redis, MIT licensed . Connects products, procurement, warehousing, orders, shipping, finance, and reporting in a unified back office. Key DOM-relevant features: platform SKU mapping for unified product/inventory semantics across stores, inventory module distinguishing physical/virtual/FBA warehouses with real-time, locked, and in-transit stock queries, sales order processing by type (normal, abnormal, FBA), and shipping module covering label printing, logistics, and batch operations . Docker deployment with demo data covering the full business chain. Supports commercial use and secondary development.

- **[Distributed Order Management System (AbhashK1)](https://github.com/AbhashK1/Distributed-Order-Management-System)**  
  Event-driven microservices architecture built with Spring Boot, Kafka, Redis, and PostgreSQL, demonstrating how large e-commerce platforms process orders using asynchronous communication . Four independent services communicate via Kafka events: Order Service (creates orders, publishes `order.created`), Inventory Service (consumes events, reserves stock in Redis, publishes `inventory.reserved`), Payment Service (consumes inventory events, simulates payment, publishes success/failure), and Notification Service (consumes payment events, logs notifications) . Includes a lightweight Streamlit web UI for visualizing and testing the entire order flow in real time without reading logs. Demonstrates key design patterns: Event-Driven Architecture, Saga-style workflow, loose coupling via Kafka, idempotent message handling, and Redis atomic operations .

- **[cloud-native-order-platform](https://github.com/Paraselli/cloud-native-order-platform)**  
  Cloud-native, event-driven microservices order processing platform with Spring Boot, Kafka, Redis, AWS integration, and React frontend . Demonstrates production-style distributed system design including JWT authentication, API gateway routing, Kafka event streaming, Redis caching with TTL, and AWS services (S3, SQS, SNS) . Dockerized with CI/CD via GitHub Actions. Explicitly positioned as more than a CRUD project — showcases scalable distributed system design and cloud integration patterns.

- **[delivery-system](https://github.com/StepanShushakov/delivery-system)**  
  Order processing system for online stores built with microservices architecture and distributed transactions using the SAGA pattern . Services include Order, Payment, Inventory, Delivery, Authentication, API Gateway, and Discovery/Configuration. Asynchronous processing via Apache Kafka with PostgreSQL per service. Tracks order states through the full lifecycle: `registered`, `paid`, `payment_failed`, `invented`, `inventment_failed`, `delivered`, `delivery_failed`, `unexpected_failure` . Includes SAGA pattern for distributed transaction management with rollback support.

- **[async-order-system](https://pkg.go.dev/github.com/MDmitryM/async-order-system)**  
  REST API service for order management written in Go with microservices architecture . API service, billing service, and shipping service communicate through Kafka with three-broker cluster for fault tolerance. PostgreSQL with pgxpool and sqlc. Swagger UI documentation at `/swagger/`. Kafka UI available for monitoring topics and messages. Go 1.23+ required .

- **[ordersgo](https://pkg.go.dev/github.com/nmarsollier/ordersgo)**  
  Go microservice for order management using CQRS pattern with MongoDB and RabbitMQ . Features GraphQL federation server alongside REST and RabbitMQ controllers. Requires authentication (Auth microservice) and catalog integration for article validation, stock deduction, and returns processing . Demonstrates event sourcing and projections for business state.

- **[wb-order-service](https://pkg.go.dev/github.com/deimossy/wb-order-service)**  
  Go demonstration microservice for order handling with PostgreSQL, Kafka, and in-memory cache . Subscribes to Kafka for order messages, persists to PostgreSQL, caches recent orders in memory with recovery from DB on startup. HTTP API and web interface for querying orders by ID . Docker Compose deployment with Makefile commands.

- **[Openfront](https://railway.com/deploy/openfront--openfront)**  
  Open-source Shopify alternative based on Next.js and Keystone.js with complete e-commerce solution including order management with automated workflows, inventory tracking, and multi-provider payment support . Self-hostable with complete data ownership. Industry-specific templates for restaurants, automotive, healthcare, and fitness. While not a full DOM platform, its order management workflows and multi-region deployment support provide a foundation for omnichannel fulfillment .

- **[Cloud-Native Order Platform (Paraselli)](https://github.com/Paraselli/cloud-native-order-platform)**  
  Event-driven microservices platform demonstrating scalable distributed system design with Kafka, Redis, AWS, JWT, and React . Auth Service, Order Service, Notification Service, and API Gateway. AWS S3 (file storage), SQS (queue processing), SNS (notifications) integration.

### Additional Strong Open-Source Options

- **moqui/mantle-usl** — Universal Service Library for Moqui Framework providing business logic components for order management and fulfillment .
- **vanilophp/order** — Order Module for Vanilo (Laravel e-commerce framework) .
- **GLPI Order Plugin** — Order management plugin for GLPI (IT asset management) .
- **Magento2 Edit Order Email** — Magento 2 extension for editing order email from admin .
- **Inventory-Order-Management-System** — ASP.NET Core MVC implementation with warehouse, product, vendor, customer, purchase order, sales order, shipment, and goods receive .

**Frameworks for building custom DOM solutions**: Combine **Apache OFBiz** for a complete open-source OMS/WMS/eCommerce stack with order routing and BOPIS/BORIS support . Use **ecommerce-erp** for cross-border fulfillment with SKU mapping and multi-warehouse inventory . Leverage the **Distributed Order Management System** reference implementation for event-driven microservices architecture patterns with Kafka and Redis . Note that true enterprise DOM platforms with MIP-based optimization, real-time carrier rate shopping, and complex order sourcing rules remain primarily commercial territory; open-source stacks provide strong event-driven architecture foundations and inventory management that require significant customization for production omnichannel fulfillment .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Distributed order management tools handle sensitive customer, inventory, and financial data. Self-hosted solutions require proper security hardening, PCI DSS compliance for payment processing, and data privacy compliance (GDPR, CCPA).
- Open-source DOM platforms are significantly less mature than commercial offerings for complex omnichannel fulfillment. Most available projects are reference implementations or academic demonstrations of architecture patterns rather than production-ready platforms. Evaluate gaps in real-time inventory synchronization, carrier integration, and optimization algorithms before deployment.
- The open-source ecosystem provides strong event-driven architecture foundations, ERP/eCommerce integration, and inventory management, but MIP-based order optimization, real-time carrier rate shopping, and enterprise-grade order sourcing remain primarily commercial offerings .

---

**Made for retail operations teams, omnichannel fulfillment managers, supply chain engineers, and e-commerce platform developers.**  
Let's make distributed order management more open, transparent, and efficient.
