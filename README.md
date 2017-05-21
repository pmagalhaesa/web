# Conceito

- A World Wide Web é um sistema de informação interligado por hipertextos (textos, imagens, vídeo, som, etc), cujo acesso se dá por meio de software denominados navegadores.

# Evolução

### Web 1.0
- Na década de 1990 surgiu o HTML (Hyper Text Markup Language). 
- Os primeiros navegadores visuais foram Netscape e Internet Explorer.
- Esta Web só estava lendo, uma vez que o usuário não pode interagir com o conteúdo da página
- Vantagem: exposição ao mundo inteiro através da internet.
- Desvantagem: só podia ler, não tinha como interagir.

### Web 2.0
- variedade especial de serviços, tais como redes sociais, blogs e wikis, que promovem a colaboração e a troca rápida de informações entre os usuários.
- Páginas repletas de vídeos, wikis, blogs e outros serviços com um traço em comum: a participação efetiva do usuário nos dois sentidos do tráfego de informação: recebe-se conteúdo dinâmico, fornece-se o mesmo tipo de informação com a mesma facilidade.

### Web 3.0
- Pesquisas em tempo real, notificações, estatísticas.
-  Com algoritmos capazes de aprender e em seguida recomendar, começou a nos informar sobre aniversário de alguém, amigos em comum, artistas, livros, publicidade em geral.
- Vantagem: código é mais fácil de desenvolver e manter e os buscadores encontram mais fácil as informações relevantes.
- Desvantagem: ter que tomar mais cuidado com a segurança das informações no site.

### Web 4.0
- Sistemas automaticos que já irão responder suas perguntas utilizando um sistema de inteligencia artificial avançado.

# W3C – World Wide Web Consortium

-Comunidade internacional que mantém e evolui os padrões da Web tais como:
  - Design e Aplicações Web (HTML, CSS, SVG, Ajax, Acessibilidade);
  - Arquitetura da Web (Protocolo HTTP, URI);
  - Web Semântica (Linked Data - RDF, OWL, SPARQL);
  - Tecnologia XML (XML, XML Schema, XSLT);
  - Entre outros.
  
 # Arquitetura da Web – Modelo Cliente-Servidor
 
 ![Modelo Cliente Servidor](http://i.imgur.com/NcVMGz5.png)
 
 - Web funciona com base no protocolo HTTP
 - Cliente envia uma requisição ao servidor. O servidor processa a requisição e retorna uma resposta.
 - O **Cliente Web** é um programa ou aplicação específica, na maioria das vezes um Navegador que envia requisições via protocolo HTTP(S) a uma outra aplicação.
 - O **Servidor Web** é um programa que recebe requisições HTTP(S), interpreta a URL e em seguida envia resposta ao Cliente Web com o recurso solicitado (arquivo HTML, CSS, JavaScript, imagens, vídeos, folhas de estilo) por meio da rede.
 - A **Internet** é uma rede mundial de computadores baseada no protocolo TCP/IP, onde todo computador conectado é denominado host (hospedeiro) e possui um identificador endereço IP (Internet Protocol).
 - O **protocolo HTTP** é a forma como clientes e servidores se comunicam na rede. As requisições e as respostas obedecem aos padrões estabelecidos pelo protocolo HTTP.
 - A **requisição HTTP** é um pacote de dados enviado pela rede pelo Cliente Web para o Servidor Web e identifica o recurso solicitado. A **resposta HTTP** é formada por pacotes de dados enviados pelo Servidor Web para o Cliente Web com os recursos solicitados.
 
 # Arquitetura da Web – URI, URL e URN
 
 ### URI (Identificador Uniforme de Recursos)
 - é um padrão para o endereçamento de recursos disponíveis na rede que engloba os conceitos de URL (Uniform Resource Locator) e URN (Uniform Resource Name).

![uri](http://i.imgur.com/qaEb9NH.png)

 ### URL (Uniform Resource Locators)
 - é um padrão de URI que serve para referenciar um recurso e sua localização, normalmente na Internet.
 
 ![url](http://i.imgur.com/9ClUDDj.png)
 
- Esquema – identifica a forma de interação entre a aplicação cliente e a aplicação servidor, como por exemplo http, https, ftp, entre outros
- User:pass – informações de usuário
- Host – nome ou número IP onde se encontra a aplicação servidor
- Porta – identifica a porta TCP/IP associada ao servidor. No caso padrão do HTTP, a porta é 80 e pode ser omitida
- Caminho – indica o local exato onde o recurso se encontra
- Query – dados não hierárquicos que detalham uma consulta normalmente sob a forma de pares nome e valor
- Fragmento – identifica uma seção no recurso
 
 ### URN (Uniform Resource Names)
 - urn:isbn:978-1-491-91866-1 
 
 # Arquitetura da Web – Protocolo HTTP – Definição
 
- O Hypertext Transfer Protocol (HTTP) é um protocolo da camada de aplicação para sistemas distribuídos e colaborativos de informação no formato de hipertextos. 

- A comunicação entre o cliente/servidor é realizada através de conexões TCP/IP
- Normalmente utilizando a porta 80
- Protocolo que não guarda estado do cliente (stateless)
- Atualmente possui duas versões ativas HTTP 1.0 e HTTP 1.1 compatíveis entre si
- O HTTP 1.1 usa conexões TCP persistentes diferentemente do HTTP 1.0

 # Arquitetura da Web – Protocolo HTTP – Navegação
 1- Usuário informa a URI (ex. http://www.exemplo.com.br) pelo navegador
 2- O browser monta uma requisição HTTP e encaminha ao servidor
 3- O servidor recebe a requisição e processa. Em seguida, monta uma resposta que é devolvida ao navegador
 4- A resposta é recebida e interpretada pelo navegador, o resultado é exibido para o usuário
 5- Sendo uma página Web, novas requisições são realizadas para os objetos aninhados (Imgs, JavaScript, CSS, etc.)

# Arquitetura da Web – Protocolo HTTP – Requisição/Resposta
### GET
- busca dados no servidor
- GET /test/go.asp?nome=Fulano&curso=Computacao 
- os dados são enviados na URL
- criando formulario
```html
<form action="receptor.php" method="GET">
<label>nome</label>
<input type="text" name="nome"/>
<label>senha</label>
<input type="password" name="senha"/>
<input type="submit" value="enviar"/>
<input type="reset" value="limpar" />
</form>
```

- pegando requisição no PHP
```php
<?php
echo "ola,".$_GET["nome"];
//echo "ola,".$_REQUEST["nome"];
?>
```


### POST
- Envia informações para o servidor
- POST /test/go.asp 
- dados sigilosos pois não aparece na URL os parametros
- os dados são enviados no corpo da requisição 
- criando formulario
```html
<form action="receptor.php" method="POST">
<label>nome</label>
<input type="text" name="nome"/>
<label>senha</label>
<input type="password" name="senha"/>
<input type="submit" value="enviar"/>
<input type="reset" value="limpar" />
</form>
```
- pegando requisição no PHP
```php
<?php
echo "ola,".$_POST["nome"];
//echo "ola,".$_REQUEST["nome"];
?>
```

### HEAD
- Recupera apenas cabeçalho HTTP das respostas do servidor
- HEAD /test/go.asp?nome=Fulano&curso=Computacao

# Arquitetura da Web – Protocolo HTTP – Códigos de retorno
![codigo retorno](http://i.imgur.com/Vx7CUg7.png)


# CSS
- Existem 3 formas de escrever um css
  - inline
```html
<label style="color:red">senha</label>
```
  - dentro do html na tag head
```html
<style>
input{background-color:blue}
</style>
```
  - arquivo externo
```html
<head>
<link rel="stylesheet" type="text/css" href="theme.css">
</head>
```
  
# JavaScript

- Linguagem criada em 1995 por Brendan Eich
- Em 2005, com o advento do AJAX alavancou o uso do JavaScript
- Javascript adiciona a interatividade e permite a criação de aplicações ricas
- JavaScript é uma linguagem de script cross-platform (roda em várias plataformas)
-  O objetivo da criação da linguagem foi atender as seguintes demandas:
  - Validação de formulários no lado cliente (programa navegador)
  - Interação com a página
- Atualmente é utilizada tanto no ambiente cliente (client side) quanto no ambiente servidor (server side)
- DOM é uma API (application programming interface) orientada a objetosque permite acessar e manipular um documento (conteúdo, estrutura e estilos)
- JavaScript é baseada em objetos
- Oferece tipagem dinâmica, tipos de variáveis não são definidos previamente
- JavaScript é uma linguagem interpretada
- JavaScript é case sensitive e utiliza conjunto de caracteres Unicode / Nome é diferente de nome que é diferente de NOME
- O operador (+) pode ser utilizado para concatenar strings
- criando variavel em JavaScript
```javascript
var a = 1;
```
  - Existem 3 formas de escrever um Javascript
  - inline
```html
<p onClick="alert('Voce clicou no parágrafo');">...</p>
```
  - dentro do html na tag head
```html
<script type="text/javascript">
alert ('Passei por aqui!');
</script>
```
  - arquivo externo
```html
<head>
<script type="text/javascript" src="script.js" />
</head>
  ```
  
### Funções

- Podem ter qualquer número de parâmetros
- Os parâmetros não são obrigatórios
- Mais parâmetros podem ser passados do que especificados pela função
- Podem retornar um valor explícito ou undefined
- escrevendo uma função

```javascript
function soma( x, y ) {
var total = x + y;
return total;
}
soma() // retorna NaN
soma(2,3) // retorna 5
```

### Ajax
- XML e JavaScript assincrono
- usado para carregar informações sem precisar recarregar a página
- usando as tecnologias para:
  - apresentação baseada em padrões como XHTML e CSS
  - exibição dinâmica através do DOM
  - troca e manipulação de dados com XML
  - JavaScript para juntar tudo isso
- no modelo classico a lógica é feita toda no servidor, no ajax a lógica é dividida entre cliente e servidor
- Vantagem:
  - Melhoria significativa na experiência do usuário
  - Redução do tráfego na rede
  - Redução na carga do servidor web
  - Flexibilidade de desenvolvimento do lado servidor
- Desvantagens
  - Maior complexidade no desenvolvimento de aplicações
  - Exigência um equipamento melhor no lado cliente
  - Requer compatibilidade do browser com padrões Javascript, HTML e CSS
  - Possui tratamento diferenciado de um browser web para outro
  - Tratamento complexo para uso das opções de avançar e voltar do browser
  
- estrutura padrão do ajax
  - GET = BUSCAR
    - Se nao passar parametro ID na URL ele busca TODOS, se passar ele busca apenas por aquele ID
  - POST = SALVAR NOVO
    - Definir HEADER
    - Manda dados no .send(dados);
  - PUT = EDITAR EXISTENTE
    - Passar na URL o ID para editar
    - Definir HEADER
    - Manda dados no .send(dados);
  - DELETE = DELETAR EXISTENTE
    - Passar na URL o ID para deletar
    
```javascript
//criação de requisiçao AJAX
    var xmlhttp = new XMLHttpRequest();

    //Função que tem a resposta da requisição
    xmlhttp.onreadystatechange = function () {

      //status ve se deu tudo certo
      if (xmlhttp.readyState == 4 && xmlhttp.status == 200) {
      }
    }

      // =================ENVIANDO GET =================================================================================
    //abrindo uma requisição GET para determinada URL
    xmlhttp.open("GET", "http://www.smartsoft.com.br/webservice/restifydb/Employees/cliente?_view=json", true);
          //send chama onreadystatechange
    xmlhttp.send();

     // =================ENVIANDO GET COM PARAMETRO URL===========================================================================
    //abrindo uma requisição GET para determinada URL
        xmlhttp.open("GET", "http://www.smartsoft.com.br/webservice/restifydb/Employees/cliente/"+codigo+"?_view=json", true);
          //send chama onreadystatechange
    xmlhttp.send();

     // =================ENVIANDO DELETE COM PARAMETRO URL===========================================================================
    //abrindo uma requisição DELETE para determinada URL
        xmlhttp.open("DELETE", "http://www.smartsoft.com.br/webservice/restifydb/Employees/cliente/"+codigo+"?_view=json", true);
          //send chama onreadystatechange
    xmlhttp.send();


    // =================ENVIANDO POST =================================================================================
    //abrindo uma requisição POST para determinada URL
    xmlhttp.open("POST", "http://www.smartsoft.com.br/webservice/restifydb/Employees/cliente?_view=json", true);

  // definindo opções no header da requisição
  xmlhttp.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
  // mandando requisição passando os dados do formulário 
      xmlhttp.send(dados);

      // =================ENVIANDO PUT =================================================================================
    //abrindo uma requisição PUT para determinada URL
    xmlhttp.open("PUT", "http://www.smartsoft.com.br/webservice/restifydb/Employees/cliente?_view=json", true);

  // definindo opções no header da requisição
  xmlhttp.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
  // mandando requisição passando os dados do formulário 
      xmlhttp.send(dados);
```
# Servidor
![imagem-servidor](http://i.imgur.com/q1qKfoI.png)

## Servidor Web
- Autenticação
  - Esquemas de Autenticação
    - Usuário Anônimo + Forms da aplicação (Algumas vezes precisa de login outras nao)
    - Autenticação Básica (Autenticão pela URL ou pelo próprio browser- envia usuario e senha na base 64)
    ![imagem-autenticacao-basica](http://i.imgur.com/QbheCZl.png)
    - Autenticação Digest (Quando um usuário solicita informações de um servidor web, uma caixa de diálogo para inserir o nome de usuário e senha aparece na tela - nao envia usuario e senha, envia apenas hash)
    ![imagem-autenticacao-digest](http://i.imgur.com/4F4LY6f.png)
  - Provedores / Integrações
    - LDAP (Active Directory, Novell NDS)
    - Kerberos (autentificação de três etapas)
    - Formulários de login providos pelas aplicações Web
- Conectividade
  - Protocolo HTTPS
  ![imagem-conectividade-https](http://i.imgur.com/hgoJdSI.png)
    - Um certificado pode apresentar diversos problemas tais como:
      - Certificado Expirado
      - Certificado de um site diferente do acessado
      - Certificado revogado pela autoridade certificadora
      - Certificados de autoridades certificadoras desconhecidas
      - Certificados assinados pelo próprio site

  - Criptografia (SSL) (é um certificado que garante a integridade dos dados criptografando eles e garante que o site é confiavel)
    - Fornece uma conexão criptografada com identificação de cliente e servidor
    - Baseado em certificados digitais emitidos por autoridades certificadoras
    - Requer que servidores Web sejam configurados com certificados digitais
    - Requer que os navegadores reconheçam as autoridades certificadores emissoras dos certificados do servidor
  - Domínios, IPs e Portas
  - Controle de Sites
  - Cache de recursos
- Gestão do FileSystem (faz a gestão dos arquivos do sistema)
- Auditoria (Logs de acesso, sistema e erros)

## Servidor de Aplicações
- Gestão de Aplicações
- Controle de Sessões
- Controle de Transações
- Pool de recursos
- Integração com bancos de dados
OBS: Alguns AS possuem módulos que atuam como Servidor web.

### Servidor de Aplicações – Tecnologias
- PHP
  - Linguagem de Scripts de código aberto
  - Pequena curva de aprendizado e desenvolvimento muito simplificado
  - Compatível com diversos sistemas operacionais e bancos de dados
  ![imagem-autenticacao-digest](http://i.imgur.com/2RGZMfK.png)
- ASP.NET
  - Tecnologia proprietária da Microsoft baseada no servidor Internet Information Server (IIS) e na plataforma Windows
  - Linguagem de Scripts que permite diversas linguagens de programação (C#, VB, etc.)
  - Requer o .NET Framework
  ![imagem-autenticacao-digest](http://i.imgur.com/hQCZ9um.png)
- Java Server Pages (JSP) e Servlets
  - Linguagem de scripts baseada em Java
  - Pode prescindir do servidor Web
  - Requer um servidor de aplicações Java
  ![imagem-autenticacao-digest](http://i.imgur.com/QhnYM0P.png)
- Comparação
  ![imagem-autenticacao-digest](http://i.imgur.com/xyMd4vH.png)
