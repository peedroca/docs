# Separação de Produtos

[Inicio](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/home.md#pick-n-go) </br>
[Voltar](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/login.md#login)

#### Definição

A separação de um produto é o ato de ler seu código de barra, seja utilizando um scanner, a camera do dispositivo ou digitando seu código.
Isto é feito através das abas abaixo:

![image](http://hunes.com.br/imagens/mobile/pickngo/018.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/017.png)
> Na aba `CONSULTA` é possível ver todos os produtos que devem ser separados.

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

[Topo](#)
