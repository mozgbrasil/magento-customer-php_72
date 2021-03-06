[checkmark]: https://raw.githubusercontent.com/mozgbrasil/mozgbrasil.github.io/master/assets/images/logos/logo_32_32.png "MOZG"
![valid XHTML][checkmark]

[getcomposer]: https://getcomposer.org/
[uninstall-mods]: https://getcomposer.org/doc/03-cli.md#remove
[tickets]: https://cerebrum.freshdesk.com/support/tickets/new
[preco]: http://www.cerebrum.com.br/preco/
[requerimentos]: http://mozgbrasil.github.io/requerimentos/
[artigo-composer]: http://mozg.com.br/ubuntu/composer
[ioncube-loader]: http://www.ioncube.com/loaders.php
[acordo]: http://mozg.com.br/acordo-licenca-usuario-final/

# Mozg\Customer

## Sinopse

Personalização dos formulários de clientes

## Demonstração

[![Clique para visualizar o vídeo](https://img.youtube.com/vi/P6uZ1FUvABc/0.jpg)](https://youtu.be/P6uZ1FUvABc "Clique para visualizar o vídeo")

## Motivação

Atender o mercado de módulos para Magento oferecendo melhorias e um excelente suporte

## Suporte / Dúvidas

Para obter o devido suporte [Clique aqui][tickets], relatando o motivo da ocorrência o mais detalhado possível e anexe o print da tela para nosso entendimento

## Preço

[Clique aqui][preco]

## Recursos

* Montagem de formulário personalizado

* Suporte a máscaras

* Suporte a validadores

* Preenchimento do endereço pelo CEP

* Checagem de documento "CPF" ou "CNPJ" impedindo registro duplicado

## Suporte / Dúvidas

Para obter o devido suporte [Clique aqui][tickets], relatando o motivo da ocorrência o mais detalhado possível e anexe o print da tela para nosso entendimento

## Preço

[Clique aqui][preco]

## Testando na Heroku

Gostaria de apresentar o aplicativo que disponibilizei para a plataforma Heroku

Com apenas 1 clique, o aplicativo cria sua loja virtual usando a plataforma de comércio eletrônico Magento e instala os módulos da MOZG

[https://github.com/mozgbrasil/heroku-magento#descrição](https://github.com/mozgbrasil/heroku-magento#descrição)

## Instalação - Atualização - Desinstalação - Desativação

--

Sugiro "printar" as telas com todos os procedimentos executados

Envie para nós as imagens das telas na eventualidade de quaisquer dificuldades

--

Este módulo destina-se a ser instalado usando o [Composer][getcomposer]

Execute o seguinte comando no terminal, para visualizar a existencia do Composer e sua versão

	composer --version

Caso não tenha o Composer em seu ambiente, sugiro ler o seguinte artigo [Clique aqui][artigo-composer]

--

É necessário que o servidor tenha o suporte a extensão [ionCube PHP Loader][ioncube-loader]

Para visualizar a existência da extensão nesse ambiente denominado PHP CLI, execute o seguinte comando no terminal

	php -v

Para visualizar se essa extensão está ativa em seu servidor no ambiente denominado PHP WEB

Certique se da presença do arquivo phpinfo.php na raiz do seu projeto

	<?php phpinfo(); ?>

Caso não exista o arquivo phpinfo.php na raiz do projeto Magento, crie o mesmo adicionado o conteúdo acima

Acesse o arquivo pelo browser

Em seguida pesquise pelo termo "ionCube PHP Loader"

Caso o seu servidor não tenha o suporte a extensão, entre em contato com sua empresa de hospedagem e peça para que eles ativem a extensão

Caso tenha a permissão e queira ativar a extensão, [Clique aqui][ioncube-loader]

Em "Loader Downloads API", efetue download do pacote compatível com o seu servidor

Descompacte o pacote e faça upload do arquivo "loader-wizard.php" para seu servidor, onde será demonstrado o passo a passo para a ativação da extensão

[Clique aqui](https://youtu.be/GZ2J6MLkko4) para ver os processos executados

--

Na presença do "ionCube PHP Loader" efetue o download do seguinte arquivo e coloque na raiz do seu servidor e acesse, se funcionar quer dizer que o "ionCube" está lendo esse tipo de encriptação

https://raw.githubusercontent.com/mozgbrasil/heroku-magento/master/phpinfo-ioncube-encoder10-x86-64-php_72.php

--

Para utilizar o(s) módulo(s) da MOZG é necessário aceitar o [Acordo de licença do usuário final][acordo]

--

Sugiro manter um ambiente de testes para efeito de testes e somente após os devidos testes aplicar os devidos procedimento no ambiente de produção

--

Sugiro efetuar backup da plataforma Magento e do banco de dados

--

Antes de efetuar qualquer atualização no Magento sempre mantenha o Compiler e o Cache desativado

--

Certique se da presença do arquivo composer.json na raiz do seu projeto Magento e que o mesmo tenha os parâmetros semelhantes ao modelo JSON abaixo

	{
	  "minimum-stability": "dev",
	  "prefer-stable": true,
	  "license": [
	    "proprietary"
	  ],
	  "repositories": [
	    {
	      "type": "composer",
	      "url": "https://packages.firegento.com"
	    }
	  ],
	  "extra": {
	    "magento-root-dir": "./",
	    "magento-deploystrategy": "copy",
	    "magento-force": true
	  }
	}

Caso não exista o arquivo composer.json na raiz do projeto Magento, crie o mesmo adicionado o conteúdo acima

### Para instalar o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

	composer require mozgbrasil/magento-customer-php_72:dev-master

Você pode verificar se o módulo está instalado, indo ao backend em:

	STORES -> Configuration -> ADVANCED/Advanced -> Disable Modules Output

--

### Para atualizar o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

Antes de efetuar qualquer processo que envolva atualização no Magento é recomendado manter o Compiler e Cache desativado

	composer update

Na ocorrência de erro, renomeie a pasta /vendor/mozgbrasil e execute novamente

Para checar a data do módulo execute o seguinte comando

	grep -ri --include=*.json 'time": "' ./vendor/mozgbrasil

--

### Para [desinstalar][uninstall-mods] o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

	composer remove mozgbrasil/magento-customer-php_72

--

### Para desativar o módulo

1. Antes de efetuar qualquer processo que envolva atualização sobre o Magento é necessário manter o Compiler e Cache desativado

2. Caso queira desativar os módulos da MOZG renomeie a seguinte pasta app/code/local/Mozg

A desativação do módulo pode ser usado para detectar se determinada ocorrência tem relação com o módulo

--

## Como configurar o método

Para configurar o método, acesse no backend em:

	∞ MOZG ∞ -> Cadastro de Clientes -> Cadastro de Clientes - (powered by MOZG)

Você terá os campos a seguir

### • **Ativar campos de endereço em /customer/account/create/**

Exibe os devidos campos relativo ao endereço

### • **Ativar suporte aos formulários**

Ao ativar o recurso deve ser utilizado o template presente no módulo, podemos visualizar que no template temos:

- Mascara aos campos: zip "cep", telephone, fax, taxvat "geralmente usado para armazenar o cpf ou cnpj", cpf "modelo de possível novo atributo", cnpj "modelo de possível novo atributo"

- Validador aos campos: zip, street_1, cpf, cnpj, taxvat

- Preenchimento do endereço pelo CEP

- Preenchimento automático para testes

- Reordenação de campos

### • **Armazenamento do endereço**

O procedimento de separar o número do endereço do campo "street1" não é uma prática nativa do Magento

Quando instalado o Magento com banco de dados demonstrativo não vemos no registro de clientes essa pratica de separar o número do endereço

Vemos preenchido para o campo "street1" da seguinte forma

	10441 Jefferson Blvd, Suite 200

Representando o logradouro o numero e nesse caso também o complemento, ambas informações armazenada no atributo "street1"

Na forma nativa do Magento

É feito o armazenamento da seguinte forma

	logradouro_com_numero_complemento = getStreet(1)
	bairro = getStreet(2)
	complemento/referencia = getStreet(3)
	complemento/referencia = getStreet(4)

Para projetos que tem o número do endereço armazenado no campo street2

Pode ser usado o recurso presente no módulo de usar a opção "armazenamento separado"

Nesse caso o nosso módulo deve ler os armazenamentos da seguinte forma

	logradouro = getStreet(1)
	numero = getStreet(2)
	complemento/referencia = getStreet(3)
	bairro = getStreet(4)

Conheço 1 projeto que adota o armazenamento alternativo como é o caso do módulo "Inovarti_Onestepcheckout"

É feito o armazenamento da seguinte forma

	logradouro = getStreet(1)
	numero = getStreet(2)
	complemento/referencia = getStreet(3)
	bairro = getStreet(4)

Conforme

https://github.com/deivisonarthur/OSC-Magento-Brasil-6-Pro#tutoriais-e-observações

#### • **A opção armazenamento padrão**

Armazena nos 2 campos nativos com os seguintes rótulos:

- Para o primeiro campo nativo *

endereço, numero, complemento

* Embora seja criado exibido 3 campos fictícios o armazenamento é feito no primeiro campo nativo de endereço no Magento

- Para o segundo campo nativo

bairro

#### • **A opção armazenamento separado**

No uso dessa opção, acesse no backend em:

	Sistema -> Configuração -> Clientes -> Configuração -> Opções de Nome e Endereço

Altere para o campo "Número de linhas em um endereço de rua" para 4

Armazena nos 4 campos nativos com os seguintes rótulos:

- Para o primeiro campo nativo

endereço

- Para o segundo campo nativo

numero

- Para o terceiro campo nativo

complemento

- Para o quarto campo nativo

bairro

## Perguntas mais frequentes "FAQ"

### Como funciona o preenchimento do endereço pelo CEP

Para o retorno dos dados do endereço através do CEP

É feito requisição ao serviço http://republicavirtual.com.br

Se não houver retorno é feito requisição ao método "consultaCEP" do Correios

### O módulo é compatível com o Bling quando importado do Magento

No Magento o atributo "taxvat" é geralmente usado para armazenar documentos como CPF/CNPJ

Nosso módulo faz o uso desse atributo para os formularios de registros !

### Como ocultar o campo "País"

**

Deve ser editado o arquivo CSS do template adicionando os seguintes itens

	#li-billing-country_id { display:none }
	#li-shipping-country_id { display:none }

**

Vemos que pelo módulo da MOZG é disponibilizado o seguinte arquivo, que se encontra vazio

/skin/frontend/base/default/css/mozg_base/style.css

**

Para o template RWD, deve ser criado o seguinte arquivo, com devido conteudo

/skin/frontend/rwd/default/css/mozg_base/style.css

**

Para o template PORTO, deve ser criado o seguinte arquivo, com devido conteudo

/skin/frontend/smartwave/porto/css/mozg_base/style.css

**

E assim sucessivamente

**

### Como adicionar novos atributos ao formulário

1)

Pode ser utilizado qualquer módulo de terceiros para a criação de atributos de clientes

https://www.magentocommerce.com/magento-connect/catalogsearch/result/?id=&s=7&pl=0&eb=0&hp=0&q=customer+attribute&t=1&p=1

Caso queira utilize esse que está nessa lista como 1 dos mais relevantes nesse quesito

https://www.magentocommerce.com/magento-connect/manage-customer-attributes-1.html

	composer require connect20/clarion_customerattribute

No uso do módulo CustomerAttribute

Podemos acessar o recurso pelo menu no backend do Magento: Clientes -> Gerenciar atributos

Tenha cautela no uso desse recurso

Recomendo o uso apenas para a criação de novos atributos

Como os módulos de gerenciamento de atributos "free" não oferece de forma gratuita o recurso de salvar os atributos no /checkout/ o nosso módulo contem recurso para essa necessidade

2)

Para aplicar o suporte do novo atributo ao formulário

Deve ser inserido no formulário o campo tendo o mesmo identificador usado na criação do atributo

Para a exibição de algum atributo contendo algum tipo de condição sempre será necessário escrever a devida programação, nessa necessidade me informe sua necessidade

[![Clique para visualizar o vídeo](https://img.youtube.com/vi/uhusB6oTinA/0.jpg)](https://youtu.be/uhusB6oTinA "Clique para visualizar o vídeo")

### Como personalizar o formulário de criação de conta em /customer/account/create/

Deve ser ativado o Debug nativo do Magento a fim de ser exibido o caminho do arquivo phtml

Caso tenha o módulo CustomerAttribute, edite na configuração do módulo para desativar, pois esse módulo aplicado o suporte aos formulários

Nunca devemos editar o arquivo disponibilizado pelo módulo, pois quando houver uma atualização o mesmo será sobrescrito

Devemos criar a mesma estrutura de diretório para o nosso template

Você deve levar em consideração o caminho exibido no debug do seu projeto

Como o debug ativo em meu projeto exibiu o seguinte caminho

frontend/base/default/template/mozg_customer/customer/form/register.phtml

Nessa pasta temos o arquivo modelo que iremos usar como base

E o template nativo está localizado em

/app/design/frontend/rwd/default/template

Então devo ter a seguinte estrutura

/app/design/frontend/rwd/default/template/mozg_customer/customer/form/register.phtml

### Como personalizar o formulário de criação de conta em /customer/account/edit/

Deve ser ativado o Debug nativo do Magento a fim de ser exibido o caminho do arquivo phtml

Caso tenha o módulo CustomerAttribute, edite na configuração do módulo para desativar, pois esse módulo aplicado o suporte aos formulários

Nunca devemos editar o arquivo disponibilizado pelo módulo, pois quando houver uma atualização o mesmo será sobreescrevido

Devemos criar a mesma estrutura de diretório para o nosso template

Você deve levar em consideração o caminho exibido no debug do seu projeto

Como o debug ativo em meu projeto exibiu o seguinte caminho

frontend/base/default/template/mozg_customer/customer/form/edit.phtml

Nessa pasta temos o arquivo modelo que iremos usar como base

E o template nativo está localizado em

/app/design/frontend/rwd/default/template

Então devo ter a seguinte estrutura

/app/design/frontend/rwd/default/template/mozg_customer/customer/form/edit.phtml

### Como personalizar o formulário de criação de conta em /checkout/

Deve ser ativado o Debug nativo do Magento a fim de ser exibido o caminho do arquivo phtml

Caso tenha o módulo CustomerAttribute, edite na configuração do módulo para desativar, pois esse módulo aplicado o suporte aos formulários

Nunca devemos editar o arquivo disponibilizado pelo módulo, pois quando houver uma atualização o mesmo será sobreescrevido

Devemos criar a mesma estrutura de diretório para o nosso template

Você deve levar em consideração o caminho exibido no debug do seu projeto

1.

Como o debug ativo em meu projeto exibiu o seguinte caminho

frontend/base/default/template/mozg_customer/persistent/checkout/onepage/billing.phtml

Nessa pasta temos o arquivo modelo que iremos usar como base

E o template nativo está localizado em

/app/design/frontend/rwd/default/template

Então devo ter a seguinte estrutura

/app/design/frontend/rwd/default/template/mozg_customer/persistent/checkout/onepage/billing.phtml


2.

Como o debug ativo em meu projeto exibiu o seguinte caminho

frontend/base/default/template/mozg_customer/checkout/onepage/shipping.phtml

Nessa pasta temos o arquivo modelo que iremos usar como base

E o template nativo está localizado em

/app/design/frontend/rwd/default/template

Então devo ter a seguinte estrutura

/app/design/frontend/rwd/default/template/mozg_customer/checkout/onepage/shipping.phtml

### Como instalar o módulo de compra em 1 passo

Acesse

https://github.com/mozgbrasil/magento-iwd-opc#mozgiwd_opc

### Como alterar a tradução de algum campo ?

Caso queira alterar a tradução de algum campo utilize a ferramenta nativa do Magento "tradução em linha" indo ao backend em:

	STORES -> Configuration -> ADVANCED/Developer -> Translate Inline

### Modificando a tradução do módulo para o template

Cada módulo tem o seu arquivo de tradução com a mesma nomenclatura do módulo

Os arquivos de tradução para português do Brasil no Magento é armazenado no diretório  

	/app/locale/pt_BR/

Recomendo não editar os arquivos nesse diretório pois em uma nova atualização de módulo esse arquivo deve ser atualizado com as informações do módulo

Na necessidade de trocar algum item

Edite o arquivo translate.csv presente no diretório do seu template para ser exibido um novo resultado

	/app/design/frontend/default/default/locale/pt_BR/translate.csv

Caso não exista a estrutura "/locale/pt_BR/translate.csv" em seu template apenas crie o arquivo nessa estrutura de diretório

Obs.

No Windows ou Mac sugiro usar o programa UltraEdit para edição do arquivo, dessa forma será mantido a codificação do arquivo em UTF-8

### Sobre o campo "Profissão"

Informo que tem alguns item no pacote de tradução do MarioSam que está equivocado em

/app/locale/pt_BR/Mage_Api2.csv:"Company","Profissão"  
/app/locale/pt_BR/Mage_Customer.csv:"Company","Profissão"  
/app/locale/pt_BR/Mage_Checkout.csv:"Company","Profissão"

Edite os arquivos e atualize "Profissão" para "Empresa"

### Sobre separação e armazenamento dos dados de endereço

O nosso módulo contem a separação dos dados de endereço

Mas o armazenamento é feito no padrão nativo do Magento

Armazenando da seguinte forma

Para o atributo de endereço de clientes

"street_1" = logradouro com número e/ou complemento

"street_2" = Bairro

Quando utilizado o banco de dados demonstrativo ou "sample_data"

Vemos preenchido para o campo "street_1"

10441 Jefferson Blvd, Suite 200

Representando o número o logradouro e nesse caso também o complemento, ambas informações armazenada no atributo "street_1"

Eu não recomendo o procedimento que seria separar o número do endereço para o atributo "street_2" pois pode gerar problemas de formatação e em integrações

## Contribuintes

Equipe Mozg

## License

[Comercial License](LICENSE.txt)

## Badges

[![Join the chat at https://gitter.im/mozgbrasil](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mozgbrasil/)
[![Latest Stable Version](https://poser.pugx.org/mozgbrasil/magento-customer-php_72/v/stable)](https://packagist.org/packages/mozgbrasil/magento-customer-php_72)
[![Total Downloads](https://poser.pugx.org/mozgbrasil/magento-customer-php_72/downloads)](https://packagist.org/packages/mozgbrasil/magento-customer-php_72)
[![Latest Unstable Version](https://poser.pugx.org/mozgbrasil/magento-customer-php_72/v/unstable)](https://packagist.org/packages/mozgbrasil/magento-customer-php_72)
[![License](https://poser.pugx.org/mozgbrasil/magento-customer-php_72/license)](https://packagist.org/packages/mozgbrasil/magento-customer-php_72)
[![Monthly Downloads](https://poser.pugx.org/mozgbrasil/magento-customer-php_72/d/monthly)](https://packagist.org/packages/mozgbrasil/magento-customer-php_72)
[![Daily Downloads](https://poser.pugx.org/mozgbrasil/magento-customer-php_72/d/daily)](https://packagist.org/packages/mozgbrasil/magento-customer-php_72)
[![Reference Status](https://www.versioneye.com/php/mozgbrasil:magento-customer-php_72/reference_badge.svg?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-customer-php_72/references)
[![Dependency Status](https://www.versioneye.com/php/mozgbrasil:magento-customer-php_72/1.0.0/badge?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-customer-php_72/1.0.0)

:cat2:
