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

### POST
- Envia informações para o servidor
- POST /test/go.asp 
- dados sigilosos pois não aparece na URL os parametros
- os dados são enviados no corpo da requisição 

### HEAD
- Recupera apenas cabeçalho HTTP das respostas do servidor
- HEAD /test/go.asp?nome=Fulano&curso=Computacao

# Arquitetura da Web – Protocolo HTTP – Códigos de retorno
![codigo retorno](http://i.imgur.com/Vx7CUg7.png)
