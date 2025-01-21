# Estudos sobre Docker, Docker-Compose e Docker Swarm Cluster

# Este repositório documenta meus estudos sobre a instalação e uso do Docker, Docker-Compose e Docker Swarm Cluster em um ambiente Ubuntu. Aqui, detalho os comandos que explorei e suas funcionalidades, com o objetivo de criar um guia de referência rápida e bem explicado.

🚀 Instalação

Durante os estudos, aprendi a instalar e configurar:

Docker: 🐳 Ferramenta principal para criar, gerenciar e executar contêineres.

Docker-Compose: 🛠️ Ferramenta para definir e gerenciar aplicações multi-contêineres.

Docker Swarm Cluster: 🤖 Para orquestração de contêineres em cluster.

📜 Comandos Docker Explorados

Abaixo, apresento os principais comandos que utilizei, suas descrições e exemplos.

1. ⚙️ Executar um contêiner

docker run -p 9090:6000 -d laele/app-node:1.0

Descrição: Inicia um contêiner com base na imagem laele/app-node:1.0.

Opções:

-p 9090:6000: Mapeia a porta 6000 do contêiner para a porta 9090 do host.

-d: Executa o contêiner em segundo plano (modo detached).

2. 🛑 Parar um contêiner

docker stop 0882dc841bc7

Descrição: Para um contêiner em execução, especificado pelo ID ou nome.

3. 📋 Listar contêineres em execução

docker ps

Descrição: Lista todos os contêineres em execução no momento.

4. 🖼️ Listar imagens locais

docker images

Descrição: Exibe todas as imagens disponíveis localmente.

5. 🛠️ Criar uma imagem

docker build -t laele/app-node:1.0 .

Descrição: Cria uma imagem a partir do Dockerfile no diretório atual.

Opções:

-t laele/app-node:1.0: Define o nome e a tag da imagem.

6. 🗑️ Remover imagens Docker

docker rmi <IMAGE_ID>

Descrição: Remove uma ou mais imagens Docker.

7. 🕰️ Ver histórico de uma imagem

docker history 62a53e9d30ed

Descrição: Mostra o histórico de camadas de uma imagem específica.

8. 🔍 Listar imagens sem tag (dangling)

docker images -f dangling=true

Descrição: Lista imagens "dangling", ou seja, imagens sem tag associada.

9. ❌ Remover um contêiner em execução

docker rm 12318d6d83b7 --force

Descrição: Remove um contêiner, mesmo que esteja em execução.

Opções:

--force: Força a remoção do contêiner.

10. ⏸️ Pausar processos em um contêiner

docker pause d263bd59de5c

Descrição: Pausa todos os processos dentro de um contêiner.

11. ▶️ Retomar processos pausados

docker unpause d263bd59de5c

Descrição: Retoma os processos pausados no contêiner.

12. ⬇️ Baixar imagem do Docker Hub

docker pull ubuntu

Descrição: Baixa a imagem oficial do Ubuntu do Docker Hub.

13. 🔄 Encerrar distribuições WSL

wsl --shutdown

Descrição: Encerra todas as distribuições do WSL, incluindo o Docker, se ele estiver em execução no WSL.

14. 💻 Acessar terminal de um contêiner

docker exec -it d263bd59de5c bash

Descrição: Abre um terminal interativo dentro de um contêiner em execução.

Opções:

-it: Permite interação com o terminal.

15. 📂 Executar um contêiner com volume montado

docker run -it --mount type=bind,source=D:\docker\volume-docker,target=/app ubuntu bash

Descrição: Inicia um contêiner com um volume local montado no contêiner.

Opções:

--mount type=bind: Define o tipo de volume como bind.

source: Caminho local do volume no host.

target: Caminho onde o volume será montado no contêiner.

📚 Conclusão

Durante meus estudos, explorei diversos comandos e aprendi conceitos fundamentais do Docker. Este repositório reflete meu progresso e serve como referência para projetos futuros e aprendizado contínuo.