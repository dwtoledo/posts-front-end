# 3 - Tags HTML para Tabelas e Dicas do VS Code.

*Publicações anteriores:*

[1 - O que é HTML? Principais Tags e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/README.md)

[2 - Tags HTML mais utilizadas, Código Semântico e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/2%20-%20Tags%20HTML%20mais%20utilizadas%2C%20C%C3%B3digo%20Sem%C3%A2ntico%20e%20Dicas%20do%20VS%20Code.md)

Para mim, Tabelas em HTML é um pouco trabalhoso, pois têm muitas tags. Vou tentar explicar da maneira mais simples possível, pois você merece né! Vamos lá!

### Vamos replicar a tabela abaixo?

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/a2i2bvxzzo414xsw6ehi.png)

Na tabela, temos:
* Os cabeçalhos (em inglês *header*): Nome e Sobrenome e;
* Os dados (em inglês *data*): Douglas Toledo 29 e Lorem Ipsum 35.
* O rodapé (em inglês *footer*): Média 32

____

### **Agora preciso que você abra o seu coração pro HTML:**
#### Em HTML a tabela é divida em três partes:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/i1foa9zghtag5yxbf94x.png)

* \<thead> *table header* (em verde) é onde colocamos os cabeçalhos: Nome, Sobrenome e Idade;
* \<tbody> *table body* (em azul) é onde colocamos os dados: Douglas, Toledo, 29, Lorem, Ipsum e 35;
* \<tfoot> *table footer* (em roxo) é onde colocamos os dados do rodapé: Média e 29.

____

#### Para criamos linhas:

* Tanto em \<thead>, \<tbody> e \<tfoot> usamos a tag \<tr> *table row*:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/a2zpeqhhg7tavr8pdwmo.png)

____

#### Para criamos cabeçalhos no \<thead>:

* Usamos a tag \<th> *table head*:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/7gnx1btxqnkd6fgdf7g4.png)

____

#### Para criamos dados no \<tbody> e no \<tfoot>:

* Usamos a tag \<td> *table data*:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/f4zsn966caz5ixfog7rm.png)

____

### Na prática:
Começamos montando uma tabela abrindo e fechando a tag \<table>:

```html
<table>

</table>
```

### 1 - Table Header
Agora vamos adicionar a primeira parte de uma tabela, os cabeçalhos (usando a tag \<thead>):

```html
<table>
	<thead>

	</thead>
</table>
```

Adicionamos uma linha usando a tag \<tr> para começar a escrever os cabeçalhos:
```html
<table>
	<thead>
		<tr>

		</tr>
	</thead>
</table>
```
E adicionamos cada cabeçalho usando a tag \<th>:

```html
<table>
	<thead>
		<tr>
			<th>Nome</th>
			<th>Sobrenome</th>
			<th>Idade</th>
		</tr>
	</thead>
</table>
```

**Agora presta atenção nessa dica maravilhosa:** no VS Code temos um atalho para escrever tags HTML que irá nos ajudar na criação de tabelas:

1. Abra o VS Code, crie um arquivo .html, digite ! e aperte Enter para criar uma estrutura básica HTML;
2. Entre as tags \<body> e \</body> vai digitando table>thead>tr>th+th+th;
3. Aperte Enter!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/pdantqq0v8hwdk904eut.gif)

Temos todo o código feito acima de maneira rápida. É só colocar os 3 cabeçalhos (Nome, Sobrenome e Idade). Explicando o atalho:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/6ouwjv781i35ox840y0z.png)

O resultado até o momento deverá ser:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/tzm9530vjswwom00n221.png)

### 2 - Table Body
Agora vamos para a segunda parte da tabela adicionando os dados (usando a tag \<tbody>) abaixo do cabeçalho \<thead>:

```html
<table>
	<thead>
		<tr>
			<th>Nome</th>
			<th>Sobrenome</th>
			<th>Idade</th>
		</tr>
	</thead>

	<tbody>

	</tbody>
</table>
```

Como temos duas linhas de dados, vamos inserir duas tags \<tr> *table row*:

```html
<table>
	<thead>
		<tr>
			<th>Nome</th>
			<th>Sobrenome</th>
			<th>Idade</th>
		</tr>
	</thead>

	<tbody>
		<tr>

		</tr>
		<tr>

		</tr>
	</tbody>
</table>
```

E por fim, colocamos cada um dos nossos dados usando a tag \<td> *table data*, uma tag para cada dado:

```html
<table>
	<thead>
		<tr>
			<th>Nome</th>
			<th>Sobrenome</th>
			<th>Idade</th>
		</tr>
	</thead>

	<tbody>
		<tr>
			<td>Douglas</td>
			<td>Toledo</td>
			<td>29</td>
		</tr>
		<tr>
			<td>Lorem</td>
			<td>Ipsum</td>
			<td>35</td>
		</tr>
	</tbody>
</table>
```

**Atalho do VS Code**
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/qhzfuyex1sgzxmd2n57y.gif)

Olha o resultado parcial (sem o \<tfoot>):
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/qy1recibi4crbeupm9wf.png)

### 3 - Table Footer
Agora o \<tfoot> ficou fácil!
Fica como a minha lição de casa para você! rs

## **Parabéns!!!**
Fico muito feliz que chegou até o final dessa publicação.
Espero que você tenha aprendido muito!

## **Quer aprender mais?**
Te convido a visitar e seguir o meu canal lá na Twitch: https://www.twitch.tv/dwtoledo.
Lá a gente faz muitas lives de front-end e tem uma playlist muito legal sobre conceitos de HTML!

*Próximas publicações:*

[4 - Tags HTML para Formulários e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/4%20-%20Tags%20HTML%20para%20Formul%C3%A1rios%20e%20Dicas%20do%20VS%20Code.md)

[5 - Tags HTML que você precisa conhecer e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/5%20-%20Tags%20HTML%20que%20voc%C3%AA%20precisa%20conhecer%20e%20Dicas%20do%20VS%20Code.md)
