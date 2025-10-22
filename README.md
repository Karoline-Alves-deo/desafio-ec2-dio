#  Arquitetura AWS com S3, Lambda e EC2  

Este repositório apresenta a arquitetura desenvolvida durante o **Desafio de Projeto da DIO (Digital Innovation One)**, utilizando os principais serviços da Amazon Web Services (AWS) — S3, Lambda e EC2, para simular um fluxo completo de processamento de dados na nuvem.

---

##  Descrição do Projeto

O objetivo do desafio é compreender a integração entre diferentes serviços da AWS, demonstrando como eventos podem acionar funções automatizadas e interagir com instâncias de processamento.

A arquitetura foi projetada para representar um fluxo **realista e seguro**, no qual um arquivo enviado ao S3 dispara uma função Lambda que, por sua vez, se comunica com uma instância EC2 para processar os dados e armazenar os resultados novamente no S3.

---

##  Arquitetura Desenvolvida

<img width="856" height="311" alt="image" src="https://github.com/user-attachments/assets/69783e76-7995-46a8-80e7-df410acdd3a4" />


> O diagrama acima ilustra o fluxo completo de comunicação entre os serviços AWS, com seus respectivos papéis e interações.

---

##  Fluxo de Funcionamento

1. **Usuário realiza upload** de um arquivo no bucket **Amazon S3** (`PUT Object`).  
2. O **S3** dispara um evento automático (`Object Created`) que aciona a função Lambda.  
3. A **função Lambda** processa os metadados do arquivo e realiza uma requisição HTTP para a instância EC2.  
4. A **instância EC2** (com volume EBS anexado) executa o processamento necessário.  
5. Os **resultados são enviados de volta ao S3** (`PUT Resultados/Registros`) para armazenamento e consulta posterior.  
6. O **Security Group da EC2** controla as portas e o tráfego de entrada/saída, garantindo a segurança da comunicação.  

---

##  Boas Práticas Implementadas

- **IAM Roles** configuradas para acesso seguro (sem uso de chaves fixas).  
- **Security Group** limitando portas e IPs permitidos (por exemplo, TCP 22 e 80).  
- **Armazenamento EBS** vinculado à EC2 para persistência local temporária.  
- **Fluxo de eventos serverless** automatizado via S3 → Lambda → EC2 → S3.  
- **Documentação visual** completa e padronizada conforme boas práticas da AWS.

---

##  Tecnologias Utilizadas

| Serviço | Função |
|----------|--------|
| **Amazon S3** | Armazenamento de arquivos e acionamento de eventos |
| **AWS Lambda** | Função serverless para processamento inicial |
| **Amazon EC2** | Instância de computação para processamento mais pesado |
| **Amazon EBS** | Volume de armazenamento associado à instância EC2 |
| **IAM & Security Groups** | Controle de acesso e segurança da infraestrutura |

---


Este projeto exemplifica o uso integrado de **serviços AWS em um ambiente híbrido (serverless + EC2)**, reforçando conceitos de **segurança, automação e escalabilidade**.  

Desenvolvido com base no **Desafio de Projeto da DIO – AWS na Prática**.  

---

## Autora

 **Karoline Alves**  
Entusiasta em tecnologia, robótica e computação em nuvem   

---
