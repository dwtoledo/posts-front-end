# Tags HTML mais utilizadas, Código Semântico e Dicas do VS Code.
**Antes de começar, já vou te dar duas dicas!**
&nbsp;
**Dica 01:** Enquanto estou estruturando um conteúdo HTML eu sempre deixo aberto um guia rápido para possíveis dúvidas.
&nbsp;
Eu gosto bastante desse [Guia de Referências HTML HostingerBR](https://github.com/hostinger/banners/blob/master/br/Guia-de-Refer%C3%AAncias-HTML-HostingerBR.pdf?raw=true).
&nbsp;
**Dica 02:** O Visual Studio Code (VS Code) nos ajuda bastante na digitação de tags HTML, a dica é a mesma para todas as tags dessa leitura:
   * No VS Code comece digitando o nome da tag;
   * Ele irá reconhecer a tag e exibirá um pop-up;
![nome da tag sendo reconhecida pelo Visual Studio Code](https://dev-to-uploads.s3.amazonaws.com/i/3dyrzecig6cam08au90g.png)
   * Aperte Enter e o VS Code irá adicionar automaticamente a tag de abertura e fechamento (se houver).
![preenchimento automático do Visual Studio Code](https://dev-to-uploads.s3.amazonaws.com/i/xjv14o4cm98972kkuksk.png)
   * Para algumas tags ele irá adicionar outros campos essenciais, como o texto alternativo *alt=""* da tag *\<img>* que é muito importante para a acessibilidade de imagens nas páginas que estamos criando.
![preenchimento automático do Visual Studio Code](https://dev-to-uploads.s3.amazonaws.com/i/9l3i85z6bzqg842i0j87.png)

___


### Agora vamos às Tags!
+ **Cabeçalhos:**

Temos 6 tags para cabeçalhos e títulos, elas vão do \<h1> até o \<h6>, quanto menor o número do h, maior a fonte, ou seja, \<h1> é a maior delas e \<h6> é a menor. Veja abaixo:

```html
<h1>Cabeçalho 1</h1>
<h2>Cabeçalho 2</h2>
<h3>Cabeçalho 3</h3>
<h4>Cabeçalho 4</h4>
<h5>Cabeçalho 5</h5>
<h6>Cabeçalho 6</h6>
```

# Cabeçalho 1
## Cabeçalho 2
### Cabeçalho 3
#### Cabeçalho 4
##### Cabeçalho 5
###### Cabeçalho 6

___

* **Parágrafos:** quando queremos adicionar um texto na página, geralmente usamos a tag \<p> *paragraph*.

```html
<p>Isso é um parágrafo de texto</p>
```
Em alguns momentos, quando não é possível usar o CSS para formatar um texto, utiliza-se algumas tags HTML. Exemplo:
* Vamos supor que no *"Isso é um parágrafo de texto"* você quer deixar apenas a palavra *"parágrafo"* em negrito ou itálico?

&nbsp;

Para **negrito** você pode utilizar a tag **\<strong>**:
```html
<p>Isso é um <strong>parágrafo</strong> de texto</p>
```
Resultado: Isso é um **parágrafo** de texto

&nbsp;

Para *itálico* você pode utilizar a tag *\<i>*:
```html
<p>Isso é um <i>parágrafo</i> de texto</p>
```
Resultado: Isso é um *parágrafo* de texto

&nbsp;

*Lembre-se, HTML estrutura, CSS estiliza/formata, então evite utilizar tags de formatação e estilização no HTML. Caso seja realmente necessário há outras tags de formatação no guia disponibilizado no início dessa leitura.*
___

* **Listas Ordenadas:** para a criação de uma lista ordenada, ou seja, a ordem dos itens é importante, utilizamos a tag \<ol> *ordered list* e adicionamos os itens da lista com a tag \<li> *list item*.

```html
<ol>
	<li>Item 1</li>
	<li>Item 2</li>
	<li>Item 3</li>
</ol>
```
1. Item 1
2. Item 2
3. Item 3

*Note que no resultado acima a lista numera cada um dos itens. Como temos 3 itens, a numeração foi de 1 a 3.*
___
* **Listas Não Ordenadas:** para a criação de uma lista não ordenada, ou seja, a ordem dos itens não é importante, utilizamos a tag \<ul> *unordered list* e também adicionamos os itens da lista com a tag \<li> *list item*.

```html
<ul>
	<li>Item 1</li>
	<li>Item 2</li>
	<li>Item 3</li>
</ul>
```

* Item 1
* Item 2
* Item 3

*Note que no resultado acima a lista apenas colocou um símbolo na frente de cada item.*
___
* **Imagens:** para adicionar imagens na página é utilizado a tag \<img>.

```html
<img src="" alt="">
```
*Note que é a primeira vez que temos algo dentro de uma tag. Chamamos src="" e alt="" de atributos da tag \<img>. São nos atributos que colocamos informações básicas de uma tag.*

Na tag \<img> temos dois atributos básicos:
* **src=""** é onde a imagem está localizada e;
* **alt=""** é o texto alternativo (essencial para a acessibilidade das páginas para pessoas que tem deficiência visual ou quando a imagem por algum motivo não for carregada, o texto alternativo será exibido).

Na prática, se formos adicionar a imagem do logo Google, temos:

```html
<img src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" alt="Logo do Google">
```

onde:
* *src="[https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png](https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png) e;*
* *alt="Logo do Google".*

o resultado é:
![Logo do Google](https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)

___

* **Links:** para levar o usuário até um link interno ou externo da página é utilizado a tag \<a> *anchor*. Veja um exemplo:

```html
<a href="https://google.com" target="_blank">Clique aqui!</a>
```
Na tag \<a> temos um atributo básico e outros opcionais:

* *O atributo básico href="" é o link de destino.
No exemplo, ao clicarmos no link ele nos levará ao "https://google.com";*

* *O atributo target="_blank" indica que o link será aberto numa nova aba ou página, esse atributo é opcional.*

O resultado do código é:
[Clique aqui!](https://google.com)

___

**Já que colocamos uma imagem \<img> e um link \<a> do Google, que tal se unirmos os dois?** Sim, podemos usar a tag \<a> para direcionar o usuário a um link após ele clicar numa imagem!

```html
<a href="https://google.com" target="_blank">
    <img src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" alt="Logo do Google">
</a>
```

Resultado:
[![Logo do Google](https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)](https://www.google.com)

___

Ainda tenho que falar das tags de Tabelas e Formulários.
Como essa leitura está ficando um pouco extensa, vou deixar para falar dela na próxima publicação, não percam!

## **Parabéns!!!**
Fico muito feliz que chegou até o final dessa publicação.
Espero que você tenha aprendido muito!

## **Quer aprender mais?**
Te convido a visitar o meu canal na Twitch: https://www.twitch.tv/dwtoledo.
Lá a gente faz muitas lives de front-end e tem uma playlist muito legal sobre conceitos de HTML.
