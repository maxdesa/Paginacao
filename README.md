# Paginacao
Paginação utilizando Javascript e CSS
Esse Projeto visa disponibilizar um meio para realizar paginação de tabelas HTML muito longas utilizano JS e CSS.
Basicamente utilizando display block e display none. 
Esse projeto não é de minha autoria mas o alterei para comportar duas setas direcionais e uma combo com os numeros de paginas.
Para o mesmo poder funcionar devemos:

* Efetuar o include no HEAD da pagina dos seguintes arquivos: js/paginacao.js e css/paginacao.css conforme exibido abaixo:
```
<head>
<title>Pagina de Exemplo</title>
<link rel="stylesheet" type="text/css" href="css/paginacao.css">
<script src="js/paginacao.js"></script>
</head>
```
* Incluir essa div que será o local aonde aparecerá a barra de navegação
```
<div id="pageNavPosition" style="padding-top: 20px" align="center">
```

* incluir no rodape da pagina o codigo abaixo:
``` 
<script>
var pager = new Pager('tabelaFrutas', 3);
pager.init();
pager.showPageNav('pager', 'pageNavPosition');
pager.showPage(1);
</script>
```
OBS:
No codigo abaixo **tabelaFrutas** corresponde ao ID da tabela o valor **3** corresponde a quantidade de linhas que voce deseja que sejam exibidas por pagina. 
```
var pager = new Pager('tabelaFrutas', 3);
```
No codigo abaixo **pageNavPosition** corresponde ao ID da DIV aonde será renderizado a barra de navegação.
```
pager.showPageNav('pager', 'pageNavPosition');
```
Vale ressaltar que essa paginação considera a primeira linha da tabela como sendo um cabeçalho, sendo assim o mesmo nunca é ocultado.

Exemplo em execução
[https://jsfiddle.net/maxdesa/w5qnkyjx/10/](https://jsfiddle.net/maxdesa/w5qnkyjx/10/)
