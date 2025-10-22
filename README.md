## 🏫 Projeto: Aplicativo Escolar na AWS

**Desafio - Gerenciamento de Instâncias EC2**

### 🇧🇷 Descrição em Português

#### 🧠 Contexto

Este projeto foi desenvolvido como parte do desafio proposto pela DIO para consolidar os conhecimentos sobre **instâncias EC2 e infraestrutura em nuvem na AWS**.
A proposta foi criar um ambiente funcional que simulasse um sistema real, aplicando boas práticas de arquitetura, segurança e escalabilidade.

#### 🎯 Ideia do Projeto

O sistema foi pensado como um **aplicativo escolar**, responsável por registrar **notas e presenças dos alunos**.
A ideia é oferecer uma aplicação web acessível, na qual professores possam lançar as faltas e as notas de cada aluno, e esses dados sejam armazenados de forma segura e escalável na nuvem.

#### ☁️ Arquitetura Implementada

A solução foi desenhada na **AWS**, utilizando os seguintes recursos principais:

* **VPC (Virtual Private Cloud):** delimita toda a rede privada do ambiente, garantindo isolamento e segurança.
* **Sub-redes em múltiplas zonas de disponibilidade (AZ-a e AZ-b):** implementadas para **alta disponibilidade**.
* **EC2 (Elastic Compute Cloud):** hospeda a aplicação web e o microserviço de presença.
* **Application Load Balancer (ALB):** distribui o tráfego entre as EC2 para escalabilidade e resiliência.
* **DynamoDB:** banco de dados NoSQL para armazenar **notas e presenças** com alta performance.
* **Subnet privada:** protege o banco de dados de acessos externos.

#### 🧩 Fluxo da Solução

1. O usuário acessa o aplicativo pela internet.
2. O **ALB** recebe e encaminha a requisição para uma **EC2**.
3. A **EC2** processa a requisição e grava/consulta os dados no **DynamoDB**.
4. O resultado é retornado ao usuário com alta disponibilidade e baixa latência.

#### 🔒 Boas Práticas Aplicadas

* Separação entre sub-redes públicas e privadas.
* Redundância entre zonas de disponibilidade.
* Balanceamento de carga via ALB.
* Persistência escalável com DynamoDB.
* Documentação e versionamento no GitHub.

#### 🧾 Conclusão

O projeto representa uma aplicação prática dos conceitos de **infraestrutura em nuvem com AWS EC2**, **configuração de VPC**, **balanceamento de carga** e **armazenamento em banco NoSQL**.
Demonstra como construir uma base sólida e segura para sistemas reais hospedados na nuvem.

---

## 🏫 Project: School Application on AWS

**Challenge - Managing EC2 Instances**

### 🇺🇸 English Description

#### 🧠 Context

This project was developed as part of the DIO challenge to consolidate knowledge about **EC2 instances and AWS cloud infrastructure**.
The goal was to create a functional environment that simulates a real-world system while applying best practices in architecture, security, and scalability.

#### 🎯 Project Idea

The system was designed as a **school application** responsible for recording **students’ grades and attendance**.
It aims to provide a web-based platform where teachers can register grades and attendance, with all data securely stored in the cloud.

#### ☁️ Implemented Architecture

The solution was built on **AWS**, using the following key components:

* **VPC (Virtual Private Cloud):** defines the private network environment for isolation and security.
* **Subnets in multiple Availability Zones (AZ-a and AZ-b):** ensure **high availability** and fault tolerance.
* **EC2 (Elastic Compute Cloud):** hosts the web application and attendance microservice.
* **Application Load Balancer (ALB):** routes traffic across EC2 instances for scalability and reliability.
* **DynamoDB:** NoSQL database used to store **grades and attendance records** efficiently.
* **Private Subnet:** keeps the database protected from external access.

#### 🧩 Solution Flow

1. The user accesses the web application over the internet.
2. The **ALB** receives the request and forwards it to one of the **EC2 instances**.
3. The **EC2** processes the request and interacts with **DynamoDB**.
4. The response is returned to the user with low latency and high availability.

#### 🔒 Applied Best Practices

* Separation between public and private subnets.
* Redundancy across availability zones.
* Load balancing with ALB.
* Scalable data persistence using DynamoDB.
* Documentation and version control via GitHub.

#### 🧾 Conclusion

This project demonstrates a practical application of **cloud infrastructure concepts using AWS EC2**, including **VPC configuration**, **load balancing**, and **NoSQL database integration**.
It showcases how to design a secure and reliable foundation for real-world cloud-based systems.
