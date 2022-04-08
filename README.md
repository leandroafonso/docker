# docker

# php 8.1 com as libs oracle OCI8 + sqlserver

Para esta imagem foi utilizado como base uma imagem oficial do debian:
	<b>FROM debian:bullseye-slim</b>
<h2>1. Oracle</h2>
Para preparar a imagem para conexão com o Oracle 12c foi baixado o instantclient basic e sdk.
A lib OCI8 já se encontra compilada e basta ser adicionada ao PHP porém ela depende do instantclient instalado e configurado no ambiente.
O github não permite o deploy de arquivos maiores que 50Mb, sendo assim você [precisará baixar] estes dois pacotes e salvá-los dentro da pasta oracle do repositório.

Acesse ao site (https://www.oracle.com/br/database/technologies/instant-client/linux-x86-64-downloads.html) e realize o donwload destes dois pacotes, a criação da conta é gratuita e será necessário para baixar.
	
<blockquote>
	instantclient-basic-linux.x64-12.2.0.1.0.zip<br>
	instantclient-sdk-linux.x64-12.2.0.1.0.zip
</blockquote>


<h2>2. Sql Server</h2>
	A lib do sqlserver já se encontra compilada e suas dependências são instaladas automaticamente no script da imagem.