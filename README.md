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
ssh -i "minha-chave-aws.pem" ec2-user@<ip-da-instancia>

### 3 - Configuração Básica 
sudo yum update -y
echo "Olá, EC2 com DIO!" > index.html
sudo python3 -m http.server 80

### 4- Resultado 
Servidor ativo e acessível via navegador no IP público.
Veja os prints abaixo:

Instância criada no painel EC2
<img width="1072" height="84" alt="image" src="https://github.com/user-attachments/assets/c2a75192-f221-4640-b9e8-a3ef3f2623eb" />

Conexão via SSH (Git Bash)

<img width="549" height="341" alt="image" src="https://github.com/user-attachments/assets/f923d0be-f1c8-4a13-ae2c-1c3fd53911da" />



### Conclusão
Durante este laboratório, aprendi na prática como:
Criar e gerenciar uma instância EC2 na AWS; 
Acessar o servidor de forma segura via SSH;
Publicar um conteúdo simples na web a partir da instância;
Documentar o processo de forma clara e organizada no GitHub.

Este repositório servirá como referência para estudos futuros sobre computação em nuvem e infraestrutura como serviço (IaaS).

Obs: A intância foi encerrada.





