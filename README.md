# O que é HTML? Principais Tags e Dicas do VS Code.

## **O que é HTML?**

HTML (Linguagem de Marcação de HiperTexto) é o que estrutura o conteúdo de uma página através de marcadores.
___

## **O que são Tags?**

São exatamente esses marcadores! Existem inúmeros marcadores/tags para deixar o seu conteúdo o mais estruturado e organizado possível. O HTML5 nos ajudou nessa missão, trazendo muitas tags novas!

Temos tags para botões, formulários, imagens, tabelas, textos, entre outras.

Aaaaahh, é importante avisar que geralmente abrimos uma tag escrevendo o nome dela entre < > e fechamos* uma tag escrevendo o nome dela entre < />. Exemplo:

Temos uma tag chamada body (vou explicar para que ela serve depois). Se quisermos estruturar um conteúdo dentro dela, abrimos a tag digitando \<body>, colocamos o conteúdo em seu interior e depois fechamos a tag digitando \</body>.

```html
<body>
   Conteúdo
</body>
```

*\* Nem todas as tags precisam ser fechadas, não se preocupe com elas agora, o VS Code irá te ajudar durante a digitação e com o tempo você irá se acostumar.*
&nbsp;

Conteúdo é muito genérico neh?!
Então vamos supor que o seu conteúdo seja um artigo que tenha um título e um texto. A estrutura ficaria:

```html
<body>
   <article>
      <h1>Título</h1>
      <p>Texto<p>
   </article>
</body>
```

Analisando o código, temos:
1. A tag \<article> é usada quando vamos escrever um artigo;
2. Todo o conteúdo do artigo deve ser escrito entre a tag de abertura \<article> e da tag de fechamento \</article>;
3. A tag \<h1> representa o "Título" do artigo;
4. A tag \<p> representa o "Texto" do artigo.

___

## **Principais Tags**


As principais tags são aquelas mais importantes, a base para uma página web e o Visual Studio Code (VS Code) nos dá uma pista de quais são, olha só!
&nbsp;

1. Abra o VS Code;
2. Crie um novo arquivo .html;
3. Comece digitando ! e depois aperte Enter.

Teremos como resultado o código abaixo:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
Ou seja, **as tags mais importantes são:**

___

```html
<!DOCTYPE html>
```
A tag acima indica ao navegador que estamos usando o HTML5.
*Nota-se que ela é uma tag que não é necessário fechar.*

___

```html
<html lang="en"></html>
```
A tag html é a principal e possui todas as outras dentro dela. Geralmente temos duas tags importantíssimas dentro dela: a tag \<head> e \<body>.

E lang="en" indica ao navegador que a página está no idioma Inglês, caso o idioma seja Português Brasil, necessário alterar de "en" para "pt-br";
___

```html
<head></head>    
```
A tag \<head> não exibe nenhum conteúdo na página. É dentro dessa tag que colocamos todas as informações de configuração do documento html (codificação de caracteres pelo navegador, como o dispositivo vai interpretar a largura e altura da página, o ícone e o título da página, onde o navegador irá buscar as informações de estilização e interações inteligentes da página).
___

```html
<meta charset="UTF-8">
```
Indica ao navegador que a codificação de caracteres será UTF-8. Essa tag é importante para que os caracteres especiais e acentuação sejam exibidos corretamente para o usuário;
___

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
Indica ao navegador que a largura do dispositivo do usuário deve ser levado em consideração para a estilização e visualização da página. Muito útil para adequar o conteúdo para tela pequenas (smartphones por exemplo).
___

```html
<title>Document</title>
```
Indica ao navegador o título da página; No código acima o título da página é *Document*.
___

```html
<body></body>
```
A última tag, mas não menos importante é a tag \<body>. É uma das mais importantes, pois é nela que fica todo o conteúdo visual que queremos exibir ao usuário.
&nbsp;
**Lembra do exemplo do artigo com um título e um texto?
Agora é o momento que vamos exibí-lo no navegador, olha que simples:**

1. Abra o VS Code;
2. Crie um novo arquivo chamado index.html;
3. Comece digitando ! e depois aperte Enter;
4. Após o VS Code adicionar a base do HTML, altera na linha 2 o idioma para "pt-br" ao invés de "en";
5. Na linha 6, altere o título da página para "Minha primeira página HTML" ao invés de "Document";
6. Na linha 9, entre as duas tags \<body> e \</body> adicione o artigo que estruturamos anteriormente:
```html
<article>
   <h1>Título</h1>
   <p>Texto<p>
</article>
```
&nbsp;
**O código final ficará assim:**

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha primeira página HTML</title>
</head>
<body>
    <article>
        <h1>Título</h1>
        <p>Texto<p>
     </article>  
</body>
</html>
```

&nbsp;
**Abrindo no navegador o arquivo index.html salvo no computador, o resultado será:**

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/kojrph45d04hrt7k3rq8.PNG)

## **Parabéns!!!**
Fico muito feliz que chegou até o final dessa publicação.
Espero que você tenha aprendido muito!

## **Quer aprender mais?**
Te convido a visitar o meu canal na Twitch: https://www.twitch.tv/dwtoledo.
Lá a gente faz muitas lives de front-end e tem uma playlist muito legal sobre conceitos de HTML. 
