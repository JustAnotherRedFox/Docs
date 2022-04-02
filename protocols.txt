           Back-end Initials
TCP – Transfer Control Protocol
UDP – User Datagram Protocol
IMAP/IMAP4 – Internet Message Access Protocol(v.4)
SMTP – Simple Mail Transfer Protocol
ARP – Address Resolution Protocol
IP – Internet Protocol
IPv6 - Internet Protocol(v.6)
Internet - Interconnect Networking
WWW – World Wide Web
http – Hypertext Transfer Protocol
https - HyperText Transfer Protocol Secure
FTP – File Transfer Protocol
DNS – Domain Name System Protocol

------------------------------------
UTF-8 – codigo multibyte(usa bits para representar letras)
bit – binary digit(0, 1)
Byte – 8 bits
KB – KiloByte = 1024B
MB – MegaByte = 1024KB
GB – GigaByte = 1024MB
TB – TeraByte = 1024GB
PB – PetaByte = 1024TB
EB – ExaByte  = 1024PB
ZB – ZetaByte = 1024EB


MB – MegaBytes == Armazenamento ex. 512MB de HD
Mb – MegaBits  == Transferencia ex. 4Mb de banda Larga

---------------------------------------
Domínio – Nome único dado ao site
Hospedagem – espaço onde se armazena os arquivos do site
URL – Uniform Resource Locator

(https://www.github.com.br/usuario)- URL

https – protocolo
www – subdominio
GitHub.com – Dominio
.com.br – TLD = Top-Level Domain
.com – GTLD = Generic TLD
.br – ccTLD = country code TLD
/usuario – path ou caminho

HTTP
conceito :
    *feito para ser simples e legivel para humanos
    *usa um conceito Client/Server,  Request/Response
    *Stateless :
        *nao guarda informacoes
        *nao existe relacoes entre conexoes
        *e dividido entre sesoes
            *Cookies; que guardao dados reutilizaveis
            *Storages; para armazenar dados mais sensiveis
    *extensivel:
        *pode se usar os headers para trocas de informacoes entre client/Server
        *Headers:
            *informacoes para comunicacao
        *Body:
            *corpo do pedido ou da resposta
Client :
    *a entidade que da inicio a comunicacao
    *a partir do User Agent :
        *Browser
        *cURL
    *faz Requests com os metodos:
        *GET
        *POST
        *PUT
        *DELETE
Server :
    *a entidade que responde o request enviado pelo client
    *esta sempre preparado para processar o request
    *e possiver ter varios servers em um computador ou varios computadorer para um Server
    *sempre ira responder em um Header com um Status Code:
        *200, 301, 404, 501, etc
Proxies :
    *sao os representantes
    *ficam entre o client e o server
    *ajudam a fazer o transporte de dados
    *possuem tambem outras funcoes como :
        *Cache
        *Filter (antvirus or parent control)
        *Load balancing (cargo distrobution)
        *Authentication
        *Authorization
URI :
    *Uniform Resource Identifier
        *indentifica um recurso
        *nome ou localizacao
    *Resource
        *o alvo do pedido
        *qualquer coisa indentificavel


 
