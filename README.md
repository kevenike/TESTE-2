JAVA-ADVANCED
PrevDent
Alunos
Keven Ike Pereira da Silva - RM: 553215
Vitor Cruz dos Santos - RM: 553621
José Ribeiro dos Santos Neto - RM: 553844
Descrição
O OdontoPredict é uma aplicação Java que utiliza análise preditiva para identificar comportamentos de risco em pacientes e dentistas. O sistema tem como objetivo antecipar a necessidade de intervenções preventivas na área de odontologia.

Tecnologias Utilizadas
Java
Spring Boot
Hibernate
JPA
Lombok
Como Rodar o Projeto Usando uma VM com AlmaLinux 9.04
Vídeo com o passo a passo:
Assista aqui

Acessar via SSH à VM
bash
Copiar
nome_usuario@ip_publico
Inserir a senha no terminal
bash
Copiar
sua_senha
Instalando o Projeto na VM
Instalar o gerenciador de pacotes yum

bash
Copiar
sudo yum install -y yum-utils
Instalar o Docker

bash
Copiar
sudo yum-config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
Verificar a versão do Docker

bash
Copiar
docker --version
Clonar o repositório

bash
Copiar
git clone https://github.com/vitorsacz/CHS1-JAVA-ADVANCED.g
Iniciar o Docker

bash
Copiar
sudo systemctl start docker
Habilitar o Docker para iniciar automaticamente

bash
Copiar
sudo systemctl enable docker
Criar uma build do Docker a partir do Dockerfile do projeto

bash
Copiar
sudo docker build -t docker-prevdent-java .
Criar um container com a imagem criada e rodar na porta 8080

bash
Copiar
sudo docker run -d -p 8080:8080 docker-prevdent-java
Estrutura do Projeto
Pacotes Principais
controller: Classes responsáveis por gerenciar as requisições HTTP.
service: Implementação da lógica de negócios do sistema.
repository: Interfaces que estendem o JpaRepository, possibilitando a interação com o banco de dados.
model: Classes que representam as entidades do domínio do sistema.
Classes Principais
Paciente
Representa um paciente no sistema, contendo atributos como idPaciente, nome e dataNascimento.

Dentista
Representa um dentista no sistema, com atributos como idDentista, nome e especializacao.

Controladores
PacienteController
Gerencia as requisições relacionadas aos pacientes, permitindo criar novos pacientes e obter informações sobre os existentes.

DentistaController
Gerencia as requisições relacionadas aos dentistas, permitindo criar novos dentistas e obter informações sobre os existentes.

Serviços
PacienteService
Implementa a lógica de negócios para gerenciar pacientes, permitindo a criação e a busca de pacientes existentes.

DentistaService
Implementa a lógica de negócios para gerenciar dentistas, permitindo a criação e a busca de dentistas existentes.

Conclusão
O OdontoPredict oferece uma estrutura robusta e eficiente para a identificação de comportamentos de risco na odontologia, permitindo que dentistas realizem intervenções preventivas mais eficazes.

Como Executar o Projeto
Clone este repositório.
Certifique-se de ter o Java e o Maven instalados.
Navegue até o diretório do projeto.
Execute o comando abaixo para iniciar a aplicação:
bash
Copiar
mvn spring-boot:run
