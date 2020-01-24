# Configurações

[Inicio](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/home.md#pick-n-go) </br>
[Voltar](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/changelog.md#changelog)

## Sumário

1. [O que é](#o-que-%C3%A9)
2. [Acessando](#acessando)
3. [Web API](#web-api) <br>
3.1 [Endereço](#endere%C3%A7o) <br>
3.2 [Métodos para obter pedido](#m%C3%A9todos-para-obter-pedido)
4. [Leitura](#leitura) <br>
4.1 [Camera de Leitura Continua](#camera-de-leitura-continua) <br>
4.2 [Leitor de código de barras](#leitor-de-c%C3%B3digo-de-barras) <br>
4.3 [Leiaute Compacto](#leiaute-compacto)
5. Notificações

#### O que é

A tela de configuração reúne as personalizações que podem ser feitas no aplicativo. Desde à API que deve ser acessada até se a aplicação deve emitir sons.

![image](http://hunes.com.br/imagens/mobile/pickngo/004.png)
> Tela de Configuração.

#### Acessando

Para acessar você não precisará estar logado. Clique na engrenagem no canto inferior esquerdo na tela de login, Ou vá ao menu e clique sob Configurações.

![image](http://hunes.com.br/imagens/mobile/pickngo/005.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/003.png)

> É necessário estar logado para acessar o menu de opções. (Imagem 2)

#### Web API

##### Endereço

O primeiro campo da seção `Web API` é o local para inserir o end point da API. Tal como `http://127.0.0.1`. É indispensável a utilização de `http://` antes de informar o endereço.

##### Métodos para obter pedido

É possível informar:

- Chave NF-e 
- Nota 
- Pedido

Estes métodos indicam o valor que deverá ser informado na tela inicial do aplicativo. Como nas imagens abaixo.

![image](http://hunes.com.br/imagens/mobile/pickngo/006.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/007.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/008.png)

> A Chave da NF-e é composta por 44 dígitos. Exemplo:
> 51080701212344000127550010000000981364117781

#### Leitura

![image](http://hunes.com.br/imagens/mobile/pickngo/009.png)
> Grupo de opções referênte a leitura e utilização das funções de separação.

##### Camera de Leitura Continua

Ao habilitar está função, no momento da leitura dos códigos de barra na tela de separação dos produtos, a camera não será fechada até que seja clicado no botão voltar.

![image](http://hunes.com.br/imagens/mobile/pickngo/010.png)

##### Leitor de código de barras

Está função possibilita remover todos os botões que abrem o leitor de código de barras do aparelho. Deve ser utilizada quando usado um leitor físico.

![image](http://hunes.com.br/imagens/mobile/pickngo/011.png)
> Ícone do leitor de código de barras.

##### Leiaute Compacto

Otimiza o leiaute da tela de separação priorizando a exibição dos produtos na aba `CONSULTA`. Com isso é criado uma nova aba `RESUMO` para apresentar as informações da nota fiscal e finalizar a separação.

![image](http://hunes.com.br/imagens/mobile/pickngo/013.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/012.png)

> Está opção é indicada quando utiliza-se um aparelho com tela pequena

##### Notificações

As opções de notificação vem como padrão ativadas, e indicam se o aplicativo deve emitir sons e/ou vibrar.

![image](http://hunes.com.br/imagens/mobile/pickngo/014.png)

##### Id do Dispositivo

O id do dispositivo é a identifação do aplicativo no dispositivo, dentre os aplicativos, este id é único. A forma como ele é gerado pode ser vista na pagina oficial [Developers](https://developer.android.com/reference/android/provider/Settings.Secure.html#ANDROID_ID).
Utilizamos está identificação para visualizarmos, caso necessário, quem fez a separação de determinado pedido.
