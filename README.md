# desafio-ec2-dio
Documentação do laboratório de EC2 na AWS realizado na DIO
# Projeto AWS EC2 - Laboratório DIO

Este repositório documenta minha experiência prática com **instâncias EC2** na **Amazon Web Services (AWS)**, como parte do desafio da DIO.  
O objetivo é demonstrar meu entendimento sobre criação, configuração e gerenciamento básico de uma máquina virtual na nuvem.

---

## Objetivo do Projeto

Consolidar o aprendizado sobre:
- Criação e configuração de instâncias EC2
- Conexão remota via SSH
- Gerenciamento básico de servidores Linux
- Uso do GitHub para documentação técnica

---

## Conceitos Aplicados

- **Instância EC2**: Máquina virtual hospedada na nuvem AWS.
- **AMI (Amazon Machine Image)**: Imagem do sistema operacional usada para iniciar a instância.
- **Key Pair (.pem)**: Chave de autenticação usada para acesso seguro.
- **Security Group**: Conjunto de regras que controlam o tráfego de rede.
- **Elastic IP / IPv4 Público**: Endereço usado para acessar a instância pela internet.

---

## Passo a Passo Realizado

### 1- Criação da Instância
- AMI: *Amazon Linux 2*
- Tipo: *t2.micro (Free Tier)*
- Par de chaves: `minha-chave-aws.pem`
- Porta liberada: 22 (SSH)
- Status: em execução

### 2- Conexão via SSH
```bash
ssh -i "minha-chave-aws.pem" ec2-user@<ip-da-instancia>

### 3- Configuração Básica




