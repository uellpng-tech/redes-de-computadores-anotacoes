# Classes de IP, configurações de rede local e DHCP

## Oque é IP? O IP possui classes?

O IP (Internet Protocol) é um número de identificação atribuído a um dispositivo conectado a rede local ou internet. Em outra palavras um IP é o CPF do seu dispositivo, ele atua como um identificador para rede possibilitando a navegabilidade sem se perder. Dado as informações iniciais vamos as classes.

O IP possui classes que refletem informações sobre a rede. O IP não é composto por números aleatórios, sua grande parte é composta por informações sobre dispositivo e rede, os três primeiros números ( <u>192</u>.168.0.1) identificão o tipo de rede (A, B ou C) sendo a A de 0 a 127, B de 128 a 191 e C de 192 a 223. Essas classes servem para classificar o tamanho no sentido de capacidade de dispositivos conectados a rede, sendo a C a menor e a A a maior, além disso também classifica a ordem das informações. Agora que compreendemos isso vamos a identificação de rede.

## Identificação de Rede e Identificação de Host

Identificação de rede é a parte do IP que corresponde a rede e Identificação de Host e a parte do ip que corresponde ao dispositivo. A rede possui classes como vimos anteriormente, porém o IP não é composto por apenas isso, a também a rede e o host que compõe o IP em ordens diferentes dependendo da classe, para entendermos melhor irei particionar de acordo com a classe:

Rede = <span style="color: red;">vermelho</span><br>
Host = <span style="color: blue;">azul</span><br>

Classe A: <span style="color: red;">10</span><span style="color: blue;">.1.1.10</span>&nbsp;&nbsp;
Classe B: <span style="color: red;">172.16</span><span style="color: blue;">.10.1</span>&nbsp;&nbsp;
Classe C: <span style="color: red;">192.168.0.</span><span style="color: blue;">1</span><br>

Essa identificação de rede e host basicamente serve para configurar um IP, todo IP para ser configurado tem que seguir essas regras sendo o host o número do computador e a rede as informações de rede como explicado anteriormente. Agora que entendemos, vamos aos IPs proibidos.

## IPs Restritos ou Privados

Os IPs possuem endereços que existem apenas em redes locais. Os IPs que vou falar cobre são IPs locais ou seja não existem na internet por tanto não é possivel utilizalo:

- 10.0.0.0
- 172.16.0.0
- 192.168.0.0

Esses IPs são determinados pela RFC 1928 como IPs de Rede Local. Dito isso vamos ao conceito de Máscaras de Rede.

## Máscara de Rede

As Máscaras de rede determina pro computador oque host e rede. A máscara básicamente diz ao computador com quemele pode falar e para onde pode enviar dados, dependendo da classe a máscara é diferente, sendo:

Classe A: 255.0.0.0<br>
Classe B: 255.255.0.0<br>
Classe C: 255.255.255<br>

Essas Máscaras de Rede o computador não sabe, por tanto é importante saber disso. dito isso, alguns IPs possuem funções especiais e vamos entender isso agora.

## IPs com funcionalidades

Os IPs também possuem funcionalidade que efetuam uma tarefa especifica. Os IPs podem executar tarefas dentro da rede, e esses IPs também não podem ser utilizados. Abaixo veremos alguns deles:

- 127.0.0.0: O IP em questão é conhecido como LoopBack e é usados para conversar com sigo mesmo na rede, básicamente é utilizado para testes de rede.
- 169.254.0.0: É o IP que só aparece quando a algum erro na rede (geralmente problema no DHCP), caso o computador/dispositivo não tenha encontrado nada, esse IP ira ser o IP de atuação nesse caso. É conhecido como APIPA.
- 0.0.0.0: É o IP de inicialização, quando o computador inicia, para teste a rede coloca esse IP que serve para ver se tudo está funcionando da maneira correta.
- 255.255.255.255: Esse IP é chamado de BroadCast geral, ele é utilizado para mandar mensagem a todas as redes.

## DHCP

O DHCP é o protocolo utilizado para distribuir configurações de rede de forma automática. O DHCP é um protocolo que distribui IP, máscada, gatway básicamente te da tudo que precisa pra rede rodar no dispositivo, em conjunto a isso vem o DNS que é o ponto para uma compreenção mais inicial do assunto, o DNS é responsavel por traduzir nomes de sites a um endereço de IP númerico.