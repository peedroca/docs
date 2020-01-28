# Separação de Produtos

[Inicio](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/home.md#pick-n-go) </br>
[Voltar](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/login.md#login)

## Sumário

1. [Definição](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/separacaoProdutos.md#defini%C3%A7%C3%A3o)
2. [Acessando](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/separacaoProdutos.md#acessando)
2. [Separando um produto](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/separacaoProdutos.md#separando-um-produto) <br>
2.1 [Código de Barras Regular](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/separacaoProdutos.md#c%C3%B3digo-de-barras-regular) <br>
2.2 [Código de Barras Único](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/separacaoProdutos.md#c%C3%B3digo-de-barras-%C3%BAnico)
3. [Sinalizando um produto](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/separacaoProdutos.md#sinalizando-um-produto) 

#### Definição

A separação de um produto é o ato de ler seu código de barra, seja utilizando um scanner, a camera do dispositivo ou digitando seu código.
Isto é feito através das abas abaixo:

![image](http://hunes.com.br/imagens/mobile/pickngo/018.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/017.png)
> Na aba `CONSULTA` é possível ver todos os produtos que devem ser separados.

#### Acessando - Tela Inicial

As abas de separação são acessadas através da tela inicial do aplicativo. Onde deverá ser informado a empresa em que será feita a separação. O campo terá como padrão a última empresa que foi utilizada, caso não tenha sido utilizada nenhuma empresa o campo virá com a primeira empresa como padrão.

No campo `Separação de Pedidos` poderá ser lido um código de barras com a camera do disposito ou digitado a Chave NF-e, Número da Nota/Pedido, de acordo com o definido nas configurações.

![image](http://hunes.com.br/imagens/mobile/pickngo/026.png)

#### Separando um produto

Posteriormente a leitura de um produto, seu marcador ficará verde.

##### Código de Barras Regular

![image](http://hunes.com.br/imagens/mobile/pickngo/021.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/022.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/023.png)
> O código de barras pode ser digitado ou lido por scanner/camera do dispositivo.

##### Código de Barras Único

O código de barras único é validado apenas na separação corrente, ou seja, na separação que estiver em aberto. Exemplo de código único: `000000000000000l0000000l` Tendo como separador o carácter 'l'. A primeira parte do código único é a sua embalagem, que deve conter obrigatóriamente 14 caractes. A segunda parte é o código do produto que deve ter um tamanho não superior a 16.

![image](http://hunes.com.br/imagens/mobile/pickngo/024.png)
> Por ser código único, o código da embalagem é permitido apenas uma vez.

#### Sinalizando um produto

Na versão `1.3.0` do aplicativo foi adicionado a função de sinalizar um produto. Isto permite alterar seu marcador de vermelho para amarelo com o intuito de auxiliar na idenficação dos produtos. Para voltar a cor vermelha, basta clicar novamente no produto.

![image](http://hunes.com.br/imagens/mobile/pickngo/020.png)
> Após um produto sinalizado atingir a quantidade necessária de separação, seu sinalizador será alterado para verde.

[Topo](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/separacaoProdutos.md#separa%C3%A7%C3%A3o-de-produtos)
