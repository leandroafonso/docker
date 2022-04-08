# docker

## php 8.1 com as libs oracle OCI8 + sqlserver

Para esta imagem foi utilizado como base uma imagem oficial do debian 
	FROM debian:bullseye-slim

1. Oracle
	Para preparar a imagem para conexão com o Oracle 12c foi baixado o instantclient basic e sdk.
	A lib OCI8 já se encontra compilada e basta ser adicionada ao PHP porém ela depende do instantclient instalado e configurado no ambiente.
	O github não permite o deploy de arquivos maiores que 50Mb, sendo assim você [precisará baixar] estes dois pacotes e salvá-los dentro da pasta oracle do repositório.

	Acesse ao site (https://www.oracle.com/br/database/technologies/instant-client/linux-x86-64-downloads.html) e realize o donwload destes dois pacotes, a criação da conta é gratuita e será necessário para baixar.
	
	``` instantclient-basic-linux.x64-12.2.0.1.0.zip

	``` instantclient-sdk-linux.x64-12.2.0.1.0.zip


2. Sql Server
	A lib do sqlserver já se encontra compilada e suas dependências são instaladas automaticamente no script da imagem.