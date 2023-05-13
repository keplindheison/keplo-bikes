# keplo-bikes

Repositório destinado ao primeiro projeto do curso [Formação Engenharia de Dados: Domine Big Data!](https://www.udemy.com/course/engenheiro-de-dados/)

### Descrição do projeto
Sistema de banco de dados de uma loja de bicicletas que roda no banco de dados [PostgreSQL](https://www.postgresql.org/) em uma instância do [EC2](https://aws.amazon.com/pt/ec2/?trk=273714db-4e14-42ba-be75-e3e36c4bc786&sc_channel=ps&ef_id=CjwKCAjwx_eiBhBGEiwA15gLN0FldiPzmUbYiG9yqpGB4vVDQMKOC3W0VjoQx3qbP_YwaX_GRZZurhoCmSQQAvD_BwE:G:s&s_kwcid=AL!4422!3!589890540382!e!!g!!ec2!16393914376!135045745338) da [AWS](https://aws.amazon.com/).

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

## Requerimentos:
<img  aling="center"  alt="amazon-web-services"  width="40"  height="40"  src="https://img.icons8.com/color/48/amazon-web-services.png"  />


## Tecnologias Usadas:
<div  style="display: inline_block"><br>
<img  aling="center"  alt="amazon-web-services"  width="40"  height="40"  src="https://img.icons8.com/color/48/amazon-web-services.png"  />
<img aling="center"  alt="linux"  width="40"  height="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" />
<img aling="center"  alt="ubuntu"  width="40"  height="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ubuntu/ubuntu-plain-wordmark.svg" />
<img  aling="center"  alt ="postgresql"  heigth="30"  width="40"  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original-wordmark.svg"  />
</div>

## Como Começar

#### Conta AWS
É necessário que tenha uma conta [AWS](https://aws.amazon.com/).

AWS é uma plataforma de serviços de computação em nuvem, que formam uma plataforma de computação na nuvem oferecida pela  [Amazon.com](http://amazon.com/). Os serviços são oferecidos em várias áreas geográficas distribuídas pelo mundo.

#### EC2
É uma parte central da plataforma de cloud computing da Amazon.com, Amazon Web Services. O EC2 permite que os usuários aluguem computadores virtuais nos quais rodam suas próprias aplicações.
 * [Como criar uma instância Linux EC2](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/EC2_GetStarted.html)

Agora que temos uma instância do Linux, vamos trabalhar dentro dela.

### Instância Linux
Instalar unzip
```
sudo apt-get install unzip
```

Instalar Postgre, criar configuração do repositório
```
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```

Importar chave
```
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```

Atualizar pacotes
```
sudo apt-get update
```

Instalar última versão do Postgre
```
sudo apt-get -y install postgresql
```

Mudar para usuário postgre
```
sudo su - postgres
```

Mostrar diretório atual
```
pwd
```

Criar diretório relacional
```
mkdir relacional
```

Entrar no diretório relacional 
```
cd relacional
```

Baixar arquivos 
```
wget https://github.com/keplindheison/keplo-bikes/archive/refs/heads/master.zip
```

Descompactar arquivo
```
unzip master.zip
```

Logar no Postgres
```
psql
```

Criar banco de dados ed
```
create database ed;
```

Listar banco de dados
```
\list
```

Mudar para o banco ed
```
\c ed;
```

Iniciar a execução dos scripts 1 até 6 (rodar um por vez)
```
\i /var/lib/postgresql/relacional/keplo-bikes/1.tabelas.sql
\i /var/lib/postgresql/relacional/keplo-bikes/2.inserindoClientes.sql
\i /var/lib/postgresql/relacional/keplo-bikes/3.inserindoProdutos.sql
\i /var/lib/postgresql/relacional/keplo-bikes/4.inserindoVendedores.sql
\i /var/lib/postgresql/relacional/keplo-bikes/5.inserindoVendas.sql
\i /var/lib/postgresql/relacional/keplo-bikes/6.inserindoVenda.sql
```

Agora é só fazer suas consultas sobre os dados que injetamos no banco de dados.