# OS Fácil - Sprint 2: DevOps e Cloud Computing

## 1. Visão Geral do Projeto

O **OS Fácil** é um aplicativo de gestão estilo ERP (Enterprise Resource Planning) desenvolvido para o setor automotivo (oficinas, funilarias). O objetivo é simplificar a gestão, eliminar processos manuais e fornecer análises de Business Intelligence (BI) para micro e pequenas empresas.

### Objetivos da Solução

* **Simplificação Operacional:** Criação e acompanhamento de Ordens de Serviço (OS) de forma digital e intuitiva.
* **Controle Financeiro e de Estoque:** Centralização do controle de peças, serviços e emissão de orçamentos.
* **Análise de Dados (BI):** Fornecimento de relatórios gerenciais sobre faturamento e produtividade.
* **Conformidade Contábil Simplificada:** Geração de relatórios estruturados para o contador.

---

## 2. DevOps e Cloud Computing - Sprint 2

A Sprint 2 foca na infraestrutura da aplicação. A solução é arquitetada em **Containers Docker** com orquestração futura em **Kubernetes**, garantindo alta disponibilidade e escalabilidade.

### Estratégia de Deploy

* **Virtualização:** Containers com Docker.
* **Infraestrutura:** Máquina Virtual (IaaS) no **Microsoft Azure**.
* **Servidor Web:** Nginx.

### Diagrama da Arquitetura

A arquitetura utiliza serviços Cloud da Oracle (OCI) e Azure para uma solução robusta e multicloud.

  ![Arquitetura OS Fácil](https://github.com/Wugabriel/Sprint2DevOps/blob/main/Arquitetura%20macro.png?raw=true)

---

## 3. Instruções de Execução (Deployment)

Para rodar a aplicação web no ambiente de contêineres Docker, siga os passos abaixo:

### Pré-requisitos

* Docker Engine e Docker Compose instalados (na sua VM ou localmente).
* Repositório clonado (pasta `osfacilDevOps`).
* Porta 80 liberada no Firewall (Azure NSG).

### Comandos de Deployment

Execute a sequência de comandos abaixo a partir da pasta **osfacilDevOps**:

1.  **Parar o Nginx Nativo (Liberação da Porta 80):**
    *(Necessário para garantir que o Docker possa se vincular à porta 80 da VM)*
    ```bash
    sudo systemctl stop nginx
    ```

2.  **Iniciar a Aplicação (Construção da Imagem e Início do Contêiner):**
    ```bash
    sudo docker compose up -d --build
    ```

3.  **Verificar o status do Contêiner:**
    ```bash
    docker ps
    ```
    *Confirme que o container `osfacil_web_devops` está no status **Up**.*

4.  **Acesso:**
    Acesse a aplicação no navegador via HTTP:
    `http://[IP_da_VM]/`

  ![Aplicação em funcionamento](https://github.com/Wugabriel/Sprint2DevOps/blob/main/Captura%20de%20tela%202025-11-09%20054223.png?raw=true)  

---

## 4. Vídeo de Demonstração

O vídeo abaixo demonstra a execução do *deploy* e a aplicação rodando no ambiente Cloud, conforme os requisitos da Sprint 2.

[![Vídeo de Demonstração da Sprint 2](https://img.youtube.com/vi/2Fg91YuVZ2U/hqdefault.jpg)](https://youtu.be/2Fg91YuVZ2U)

---

## Integrantes

* Fábio Henrique de Souza Eduardo Rm:560416 
* Gabriel Wu Castro Rm:560210
* Renato Kenji Sugaki Rm:559810
