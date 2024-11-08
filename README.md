<div align="center">
  <img src="https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png" alt="Docker logo" width="100""/>
  <h1>Docker Fundamentals</h1>
</div>

Este projeto foi desenvolvido como parte do curso Ignite da Rocketseat, na trilha de DevOps, com o objetivo de dominar os fundamentos da containerização usando Docker. Ao longo do projeto, foram abordadas técnicas essenciais para criar, configurar e otimizar containers, aplicando práticas recomendadas para o desenvolvimento de ambientes em Docker.

## 💡 Sobre o Projeto

Utilizamos um boilerplate de NestJS para aprender na prática como containerizar uma aplicação Node.js. O projeto serve como material de estudo para entender conceitos fundamentais do Docker, incluindo:

- Criação e otimização de Dockerfiles
- Multi-stage builds
- Gerenciamento de containers com Docker Compose
- Configuração de redes (networks)
- Persistência de dados com volumes
- Integração com banco de dados (MySQL)

## 🛠 Tecnologias Utilizadas

- NestJS
- Docker e Docker Compose
- MySQL
- pnpm (gerenciador de pacotes)
- TypeORM

## 🚀 Estrutura do Projeto

O projeto utiliza uma estrutura multi-stage build para otimização da imagem final:

- **Base**: Configuração inicial com Node.js e pnpm
- **Prod-deps**: Instalação de dependências de produção
- **Build**: Compilação do código
- **Release**: Imagem final otimizada

## 🗄 Configuração do Docker

### Docker Compose

O projeto utiliza Docker Compose para orquestrar dois serviços:

1. **Aplicação (app)**:
   - Porta: 3001 (host) -> 3000 (container)
   - Construída a partir do Dockerfile local

2. **Banco de Dados (mysql)**:
   - MySQL 8
   - Porta: 3306
   - Volume persistente para dados
   - Variáveis de ambiente configuradas para desenvolvimento

### Networks

- Network bridge dedicada para comunicação entre os containers
- Isolamento apropriado dos serviços

### Volumes

- Volume dedicado para persistência dos dados do MySQL

## 🚦 Como Executar

1. Certifique-se de ter Docker e Docker Compose instalados usando:
```bash
docker -v
docker-compose -v
```
   
2. Clone o repositório:
```bash
git clone git@github.com:gbmoraes-dev/docker-fundamentals.git
```

3. Entre na pasta:
```bash
cd docker-fundamentals
```

4. Por fim, execute:
```bash
docker-compose up --build -d
```

A aplicação estará disponível em `http://localhost:3001`

## 📝 Aprendizados

Durante o desenvolvimento deste projeto, foram abordados diversos conceitos importantes:

- Boas práticas na construção de imagens Docker
- Otimização de builds com cache e multi-stage
- Gerenciamento de dependências em containers
- Comunicação entre serviços containerizados
- Persistência de dados com volumes Docker
- Configuração de variáveis de ambiente
- Dockerização de aplicações Node.js

## 🎓 Sobre o Curso

Este projeto integra o módulo de DevOps do curso Ignite da Rocketseat, proporcionando uma abordagem prática para o aprendizado de containers. Ao longo do módulo, exploramos as melhores práticas de containerização de aplicações, entendendo como otimizar, gerenciar e orquestrar containers de forma eficiente.
