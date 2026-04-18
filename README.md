# Tech Challenge 1: ToggleMaster MVP Deployment

Este repositório contém os arquivos e entregáveis do primeiro desafio técnico da pós-graduação em DevOps e Infraestrutura Cloud da FIAP. O desafio envolve a implantação de uma aplicação monolítica chamada ToggleMaster na AWS, seguindo as melhores práticas de arquitetura e segurança.

## Descrição do Desafio

O Tech Challenge é um projeto prático que engloba conhecimentos de DevOps, arquitetura de aplicações e infraestrutura cloud. Neste desafio, a equipe deve colocar no ar uma aplicação MVP (Minimum Viable Product) para gerenciamento de Feature Flags, começando com uma execução local e progredindo para uma implantação na nuvem AWS.

### Objetivos Principais
- Executar a aplicação monolítica localmente para compreensão do funcionamento.
- Analisar o código e discutir vantagens/desvantagens do monolito para MVP.
- Avaliar conformidade com os 12 Fatores (12-Factor App).
- Projetar e provisionar infraestrutura AWS com VPC, EC2 e RDS.
- Estimar custos mensais da arquitetura proposta.
- Demonstrar a aplicação rodando na nuvem com conectividade ao banco de dados.

### Requisitos Técnicos
1. **Cultura DevOps e Arquitetura**: Análise da aplicação monolítica e 12-Factor App.
2. **Arquitetura Cloud**: Diagrama incluindo VPC, sub-redes, EC2, RDS e Security Groups.
3. **AWS Prático**: Provisionamento manual da infraestrutura e configuração da aplicação.

## Entregáveis

- **Vídeo de Demonstração** (até 15 min): Apresentação local, diagrama, demo na AWS, configurações de segurança.
- **Documentação**: Link do diagrama de arquitetura, discussão sobre 12-Factor App.
- **Relatório de Entrega** (.PDF ou .txt): Nomes dos participantes, links, resumo de desafios, estimativa de custos.

## Estrutura do Repositório

O repositório está organizado da seguinte forma, mapeando as pastas aos entregáveis do desafio:

- **`Arquitetura_Estimativa/`**: Contém arquivos relacionados à estimativa de arquitetura e custos.
  - `EstimativaInfra.pdf`: Relatório de estimativa de infraestrutura e custos da AWS.
  - `FIAP - Tech Challenge.drawio.png`: Diagrama de arquitetura (possivelmente exportado do draw.io).
  - **Relacionamento**: Corresponde aos entregáveis de documentação (diagrama) e relatório (estimativa de custos).

- **`CI_CD_Aplicacao/`**: Pasta dedicada à aplicação e possíveis configurações de CI/CD.
  - `toggle-master-monolith-main/`: Código fonte da aplicação ToggleMaster (monolítica).
    - `app.py`: Código principal da aplicação Python.
    - `requirements.txt`: Dependências Python.
    - `docker-compose.yaml`: Configuração para execução com Docker.
    - `Dockerfile`: Instruções para construir a imagem Docker.
    - `entrypoint.sh`: Script de entrada.
    - `README.md`: Documentação específica da aplicação.
    - **Relacionamento**: Usado para execução local (vídeo de demonstração) e implantação na EC2 (requisito AWS prático).

- **`Documentos/`**: Documentos diversos do projeto.
  - `Tech_Challenge_Fase01.pdf`: Relatório de entrega da Fase 1.
  - **Relacionamento**: Corresponde ao relatório de entrega (.PDF).

- **`Infra_Terraform/`**: Código de infraestrutura como código usando Terraform.
  - `infra_techchallenge_1-main/`: Módulos e configurações Terraform para provisionar recursos AWS.
    - `main.tf`, `variables.tf`, etc.: Configurações para VPC, EC2, RDS, Security Groups.
    - **Relacionamento**: Embora o desafio peça provisionamento manual, esta pasta pode conter uma versão IaC da infraestrutura proposta, útil para futuras fases ou automação.

- **`README.md`**: Este arquivo, descrevendo o repositório e o desafio.

## Como Executar Localmente

Para entender o funcionamento da aplicação antes da implantação na nuvem:

1. Navegue para `CI_CD_Aplicacao/toggle-master-monolith-main/`.
2. Instale as dependências: `pip install -r requirements.txt`.
3. Execute a aplicação: `python app.py` ou use Docker: `docker-compose up`.

A aplicação fornecerá uma API simples para CRUD de feature flags.

## Notas Adicionais

- A aplicação é um monolito intencional para MVP, permitindo rápida validação da ideia.
- A infraestrutura AWS proposta segue melhores práticas de segurança com sub-redes privadas para o banco de dados.
- Este é o ponto de partida para evoluir o sistema para uma arquitetura distribuída em fases futuras.

