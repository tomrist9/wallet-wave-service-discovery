# Wallet-Wave: Service Discovery (Kubernetes-Based)

`wallet-wave-service-discovery` is part of the **Wallet-Wave Banking Platform**, a production-grade microservices-based financial system.  
This module provides **service discovery capabilities** using **Kubernetes-native mechanisms**, replacing traditional Eureka Server setups.

---

## 🚀 Why Kubernetes Service Discovery?

In cloud-native environments, relying on platform-native service discovery is more efficient, scalable, and easier to maintain.  
Kubernetes handles service registration and DNS resolution automatically, eliminating the need for manual discovery systems like Eureka.

---

## 🧩 Features

- ✅ Zero-configuration service registration via Kubernetes Services
- ✅ Built-in load balancing with ClusterIP or Headless services
- ✅ DNS-based service discovery (`http://service-name.namespace.svc.cluster.local`)
- ✅ High availability & scalability using Kubernetes primitives
- ✅ Secure inter-service communication (e.g., via Istio or Linkerd, optional)

---

## 🔧 How It Works

- Each microservice in **Wallet-Wave** is deployed as a **Kubernetes Deployment**
- Services are exposed via `Service` resources
- Other microservices use standard DNS to locate and call them

> Example: If `account-service` is exposed as a Kubernetes `Service`, other pods can call it via:
