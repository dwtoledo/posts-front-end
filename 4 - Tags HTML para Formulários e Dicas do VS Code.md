# 4 - Tags HTML para Formulários e Dicas do VS Code.

*Publicações anteriores:*

[1 - O que é HTML? Principais Tags e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/README.md)

[2 - Tags HTML mais utilizadas, Código Semântico e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/2%20-%20Tags%20HTML%20mais%20utilizadas%2C%20C%C3%B3digo%20Sem%C3%A2ntico%20e%20Dicas%20do%20VS%20Code.md)

[3 - Tags HTML para Tabelas e Dicas do VS Code](https://github.com/dwtoledo/posts-front-end/blob/main/3%20-%20Tags%20HTML%20para%20Tabelas%20e%20Dicas%20do%20VS%20Code.md)


Agora que você já viu [...]
* as principais tags e;
* tabelas em HTML;

[...] chegou a hora dos Formulários!

## Vamos replicar o formulário abaixo?

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ok062ze4v2413e5s2pcp.png)

No formulário, temos:
* Duas entradas de texto ("Nome" e "Senha");
* Uma seleção através de botões radiais ("Selecione a tarefa");
* Uma seleção através de uma lista de dados ("Selecione o status da tarefa");

____

### **Vamos por partes, se não vamos complicar as coisas!**

1. Usamos a *tag \<input>* para o usuário digitar os dados;
2. Definimos qual é o tipo do dado usando o atributo *type=""*;
3. Definimos um nome para esse campo usando o atributo *name=""*;

Exemplo em que o usuário irá digitar a sua idade:

```html
<input type="number" name="idade">
```

Há mais de 20 tipos de dados! **É muito importante você colocar o tipo correto** para que o navegador prepare a página para receber aquele tipo de dado específico.

Exemplos:

* Se você colocar o *type="password"*, o navegador irá entender que o dado é uma senha e ela não ficará visível durante a digitação.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ajsykqbzb0bsp28jxcm7.PNG)

* Se você colocar o *type=color*, o navegador irá entender que o dado é uma cor e irá abrir uma seleção de paleta de cores.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/jzr1rekywcacoffkbl6j.png)

* Se você colocar o *type=date*, o navegador irá entender que o dado é uma data e irá formatar o campo para uma fácil digitação e ou seleção de data.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/l6t1po05ygfuiy5a0m8m.png)

Você pode ver a lista completa de todos os tipos de inputs no link [HTML Input Types - W3Schools](https://www.w3schools.com/html/html_form_input_types.asp)!

____

#### No formulário inicial, para as duas entradas de texto ("Nome" e "Senha"):

Nome é *type="text"*, então vamos começar nosso formulário adicionando o campo *nome*:

```html
<input type="text" name="nome">
```

Senha é *type="password"*, então vamos adicionar o campo *senha* após uma quebra de linha (*tag \<br>*):

```html
<input type="text" name="nome">
<br>
<input type="password" name="senha">
```
O resultado do html é:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/wtsvy3gefvwi85a9h258.jpg)

*Mas Douglas, cadê a legenda ("Nome:" e "Senha:") e a descrição do campo ("Insira seu nome" e "Insira sua senha")?*

* Para a legenda "Nome:", usamos a *tag \<label>*, no seu atributo *for=""* colocamos o nome do campo usado na *tag \<input>* e entre a abertura e fechamento das *tags* digitamos a legenda;

* Para a descrição "Insira seu nome", usamos o atributo *placeholder=""* da *tag \<input>*.

Colocando a legenda e descrição, temos:

```html
<label for="nome">Nome:</label>
<input type="text" name="nome" placeholder="Insira seu nome">
<br>
<label for="senha">Senha:</label>
<input type="password" name="senha" placeholder=""Insira sua senha>
```

Olha o resultado!
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/8hgwo0ucimcyu6z5sqi4.jpg)

____

#### Voltando ao formulário inicial, vamos continuar com a seleção através de botões radiais e seleção através de uma lista de dados:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/dl5koiucofdpc2j4w89b.png)

____

* Para a seleção através de botões radiais usamos *\<input type="radio">*:

```html
<label for="tarefa">Seleciona uma tarefa:</label>
<br>
<input name="tarefa" type="radio" value="varrer-a-casa"> Varrer a casa
<input name="tarefa" type="radio" value="lavar-a-louca"> Lavar a louça
<input name="tarefa" type="radio" value="arrumar-o-quarto"> Arrumar o quarto
```

*Note que usamos o mesmo nome "tarefa" para todas as opções.* Isso faz com que consigamos selecionar somente uma tarefa entre as três. Se os nomes fossem diferentes, seriamos capaz de selecionar mais de um item.

O resultado desse HTML é:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ip8ngamn71rpolpw4i0a.png)

____

* Para a seleção através uma lista de dados usamos a *tag \<input>* e colocamos o nome da lista no atributo *list=""*, ~~não usamos o atributo *type=""*~~ nesse caso;

* A lista de dados vai entre as *tags \<datalist id="lista-status">\</datalist>*, onde *id* é o mesmo nome dado no atributo *list=""* da *tag \<input>* e;

* Cada dado da lista fica na *tag \<option value="">*

```html
<label for="status">Selecione o status da tarefa</label>
<input name="status" list="lista-status" placeholder="clique e selecione">
<datalist id="lista-status">
     <option value="Aguardando">
     <option value="Em Processo">
     <option value="Concluído">
</datalist>   
```

O resultado é:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/oy3pmxlb65hyaszcsttm.png)

____

#### O botão "Enviar" é muito simples, é uma *tag \<input>* do *type="submit"* e o texto do botão fica no atributo *value=""*.

```html
<input type="submit" value="Enviar">
```
O resultado é:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/yn5lhg1912ntb4gzjxuo.png)

____

**Juntando todos os HTML, temos:**

```html
    <form>
        <label for="nome">Nome:</label>
        <input type="text" placeholder="Insira seu nome" name="nome">
        <br>
        <label for="senha">Senha:</label>
        <input type="password" placeholder="Insira sua senha" name="senha">
    
        <label for="tarefa">Seleciona uma tarefa:</label>
        <br>
        <input name="tarefa" type="radio" value="varrer-a-casa"> Varrer a casa
        <input name="tarefa" type="radio" value="lavar-a-louca"> Lavar a louça
        <input name="tarefa" type="radio" value="arrumar-o-quarto"> Arrumar o quarto
        <br>

        <label for="status">Selecione o status da tarefa</label>
        <input name="status" list="lista-status" placeholder="clique e selecione">
        <datalist id="lista-status">
            <option value="Aguardando">
            <option value="Em Processo">
            <option value="Concluído">
        </datalist>         

        <input type="submit" value="Enviar">
    </form>
```

Como resultado:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/7l2hdh0tb33qcrecy2kx.png)

____

**Reparou que está faltando algo ainda?**

Nos campos de seleção há uma divisória, agrupando todos esses campos do formulário (*radio* e *datalist*). Isso se chama *fieldset*!

* Usamos a *tag \<fieldset>* para agrupar e;
* Podemos dar um nome para o agrupamento usando *tag \<legend>*:

```html
        <fieldset>
            <legend>Seleciona uma tarefa:</legend>
            <input name="tarefa" type="radio" value="varrer-a-casa"> Varrer a casa
            <input name="tarefa" type="radio" value="lavar-a-louca"> Lavar a louça
            <input name="tarefa" type="radio" value="arrumar-o-quarto"> Arrumar o quarto
            
            <br>

            <label for="status">Selecione o status da tarefa</label>
            <input name="status" list="lista-status" placeholder="clique e selecione">
            <datalist id="lista-status">
                <option value="Aguardando">
                <option value="Em Processo">
                <option value="Concluído">
            </datalist>
        </fieldset>
```

## O resultado final do HTML completo é:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ok062ze4v2413e5s2pcp.png)

____

## **Parabéns!!!**
Fico muito feliz que chegou até o final dessa publicação.
Espero que você tenha aprendido muito!

## **Quer aprender mais?**
Te convido a visitar e seguir o meu canal lá na Twitch: https://www.twitch.tv/dwtoledo.
Lá a gente faz muitas lives de front-end e tem uma playlist muito legal sobre conceitos de HTML!

*Próximas publicações:*

[5 - Tags HTML que você precisa conhecer e Dicas do VS Code.](https://github.com/dwtoledo/posts-front-end/blob/main/5%20-%20Tags%20HTML%20que%20voc%C3%AA%20precisa%20conhecer%20e%20Dicas%20do%20VS%20Code.md)
