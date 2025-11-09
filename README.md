# OS Fácil - Sprint 2: DevOps e Cloud Computing

## 1. Visão Geral do Projeto

### 1.1. Descrição do Problema

O mercado de reparação e serviços automotivos no Brasil, composto majoritariamente por micro e pequenas empresas, enfrenta um desafio significativo relacionado à gestão ineficiente e desorganizada de seus processos operacionais e financeiros. A dependência de métodos manuais, como cadernos de anotações e planilhas simples, para o controle de Ordens de Serviço (OS), resulta em perda de tempo, dinheiro e dificuldades fiscais. A ausência de um sistema automatizado leva ao descontrole de estoque, com a falta de peças essenciais gerando atrasos e insatisfação dos clientes. Adicionalmente, a falta de uma visão gerencial clara sobre a saúde financeira do negócio e a complexidade do sistema tributário brasileiro, especialmente com as recentes mudanças da Reforma Tributária, criam um ambiente de alto risco e baixa competitividade para esses pequenos empreendedores.

### 1.2. Solução Proposta: OS Fácil

O OS Fácil é um aplicativo de gestão estilo ERP (Enterprise Resource Planning) desenvolvido especificamente para o setor automotivo. A solução visa simplificar a gestão, aumentar o controle e a eficiência operacional de oficinas mecânicas, funilarias e centros automotivos. O sistema se propõe a ser uma ferramenta acessível, intuitiva e completa, quebrando a barreira de entrada para a digitalização e permitindo que mesmo os menores empreendedores possam ter uma gestão de ponta.

### 1.3. Objetivos da Solução

Os principais objetivos do OS Fácil são:

- **Simplificação Operacional:** Eliminar o uso de papel e planilhas, permitindo a criação e o acompanhamento de Ordens de Serviço de forma digital e intuitiva.
- **Controle Financeiro e de Estoque:** Centralizar o controle de estoque de peças, o registro de serviços efetuados e a emissão de recibos e orçamentos, garantindo que o proprietário saiba exatamente o que entra e o que sai da oficina.
- **Análise de Dados (Business Intelligence):** Fornecer análises e relatórios gerenciais sobre faturamento, produtividade da equipe e rentabilidade de serviços, capacitando o proprietário a tomar decisões estratégicas.
- **Inclusão Tecnológica:** Desenvolver uma plataforma intuitiva e abrangente, que seja fácil de usar para proprietários com baixa familiaridade com tecnologia.
- **Conformidade Contábil Simplificada:** Gerar arquivos e relatórios estruturados com todos os dados fiscais e de faturamento, simplificando a comunicação com o contador e garantindo a conformidade com as exigências tributárias.

## 2. DevOps e Cloud Computing - Sprint 2

### 2.1. Estratégia de Virtualização

Para o projeto OS Fácil, a estratégia de virtualização adotada é baseada no uso de **Containers com Docker**. Essa escolha é justificada pela necessidade de um ambiente de desenvolvimento, teste e produção que seja ágil, escalável, confiável e de fácil manutenção. Os containers Docker nos permitem empacotar a aplicação e todas as suas dependências em uma única imagem, garantindo que o software funcione de maneira consistente em qualquer ambiente. A orquestração desses containers será realizada com o **Kubernetes**, permitindo a escalabilidade horizontal e a alta disponibilidade da aplicação, fatores críticos para atender a um mercado com grande potencial de crescimento.

### 2.2. Diagrama da Arquitetura

A arquitetura da solução foi desenhada para ser robusta, escalável e segura, utilizando os serviços da Oracle Cloud Infrastructure (OCI) e do Microsoft Azure.

![Arquitetura OS Fácil]()

*Diagrama da arquitetura da solução OS Fácil.*

### 2.3. Justificativa para a Virtualização com Containers

A adoção da virtualização com containers Docker e a orquestração com Kubernetes trazem uma série de benefícios estratégicos para o projeto OS Fácil:

- **Redução de Custos e Acessibilidade:** A otimização do uso de hardware, compartilhando a mesma infraestrutura para múltiplos serviços (banco de dados, web, BI), reduz o custo operacional (OpEx). Esse modelo de economia de infraestrutura é repassado ao cliente final, garantindo um preço competitivo e acessível para micro e pequenas oficinas.

- **Simplificação Operacional e Confiabilidade:** Os ambientes isolados dos containers garantem que o desenvolvimento e os testes sejam idênticos à produção, reduzindo drasticamente bugs e falhas. A implantação rápida (CI/CD) facilita a entrega contínua de novas funcionalidades e correções, mantendo o sistema sempre atualizado e em conformidade com as regulamentações fiscais.

- **Escala e Potencial de Mercado:** A escalabilidade horizontal, gerenciada pelo Kubernetes, permite replicar instâncias da aplicação em segundos, suportando o crescimento da base de clientes sem perda de performance. A alta disponibilidade garante que a plataforma permaneça rápida e responsiva mesmo em picos de acesso, atendendo com qualidade tanto a micro quanto a grande oficina.

- **Performance e Visão Gerencial (BI):** O isolamento de cargas de trabalho permite que processos pesados, como relatórios de BI ou processamento fiscal, sejam executados em seus próprios ambientes, sem impactar a performance do sistema para o usuário final. Isso garante que a criação de uma Ordem de Serviço (OS) e a análise de dados sejam instantâneas e confiáveis para o proprietário.

## 3. Vídeo de Demonstração da Sprint 2

O vídeo abaixo demonstra o deploy da aplicação OS Fácil, evidenciando o progresso da Sprint 2 e a aplicação dos conceitos de DevOps e Cloud Computing.

[Deploy OsFacil Sprint 2](https://youtu.be/2Fg91YuVZ2U)

**Integrantes**  
Fábio Henrique de Souza Eduardo Rm:560416  
Gabriel Wu Castro             Rm:560210  
Renato Kenji Sugaki           Rm:559810
