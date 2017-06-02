Como Instalar e Usar o Docker magento
===================


atualizar o banco de dados de pacotes:

> sudo apt-get update

----------
Adicione ao sistema a chave GPG oficial do repositório do Docker:

> sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

----------
Adicione o repositório do Docker às fontes do APT:

> sudo apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'

> sudo apt-get update
----------
Certifique-se de que você está instalando a partir do repositório do Docker em vez do repositório padrão do Ubuntu 16.04:

> apt-cache policy docker-engine

----------
instale o Docker:

> sudo apt-get install -y docker-engine

----------
Escolha uma imagem do magento:
> docker search magento

> docker pull magento_escolhido

> docker run magento_escolhido

> docker run -it magento_escolhido

----------
Com este ultimo comando o shell da imagem ficará acessivel.
