<div align="center">

![Magento 2 Easy Template Path Hints](https://i.imgur.com/d8QEHRb.png)
# Magento 2 Easy Template Path Hints

</div>

<div align="center">

![Supported Magento Versions](https://img.shields.io/badge/magento-%202.3_|_2.4-brightgreen.svg?logo=magento&longCache=true&style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?color=%23234&style=for-the-badge)

</div>

##  Visão Geral
O **Hello World** do [Mageplaza](http://www.mageplaza.com/) é apenas um teste que fiz para poder instalar componentes utilizando [composer](https://getcomposer.org/). As instruções para fazer o módulo estão disponíveis no site da [Mageplaza](http://mageplaza.com).


## Funcionalidades
* Apenas um **hello world!**


## Instalações

### 1 Usando composer
```
bin/composer config repositories.rivasalmir-helloworld git https://github.com/rivasalmir/mageplaza-helloworld.git
bin/composer require rivasalmir/helloworld:main
```

### 2 Usando Modman
```
modman init
modman clone https://github.com/rivasalmir/mageplaza-helloworld.git
```

### 3 Usando arquivos Zip
* Download [arquivo zip](https://github.com/rivasalmir/mageplaza-helloworld/archive/refs/heads/main.zip)
* Extrair e enviar arquivos para `/caminho-do-magento/app/code/Mageplaza/HelloWorld/`

Após a instalação por qualquer meio, ative a extensão com as seguintes etapas

1. Ativar módulo
```
php bin/magento module:enable Mageplaza_HelloWorld --clear-static-content
php bin/magento setup:upgrade
```
2. Limpe o cache da loja
```
php bin/magento cache:flush
```
3. Deploy do conteúdo estárico - *apenas no modo de produção*
```
rm -rf pub/static/* var/view_preprocessed/*
php bin/magento setup:static-content:deploy
```
4. Acesse https://{url principal}}/helloworld/index/test

## Changelog
**Version 1.0.0. (2022-05-27)**
* Release inicial

## Autor
- [Almir F Rivas Jr](http://linkedin.com/in/rivasalmir)