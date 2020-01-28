# Erros Mapeados

[Inicio](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/home.md#pick-n-go)

## Sumário

1. [Definição](https://github.com/peedroca/documentations/new/master/Pick%20'n'%20Go#defini%C3%A7%C3%A3o)
2. [Necessário estar logado para separar pedidos!](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/errosMapeados.md#necess%C3%A1rio-estar-logado-para-separar-pedidos)
3. [O código XXXXXXXX não consta para separação!!](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/errosMapeados.md#o-c%C3%B3digo-xxxxxxxx-n%C3%A3o-consta-para-separa%C3%A7%C3%A3o)

#### Definição

Aqui serão exibidos todos os erros mapeados/tratados no aplicativo. Os erros que não forem exemplificados e/ou explicados aqui deverão ser informados pelas formas de contato no [item anterior](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/sobre.md#sobre).

#### Necessário estar logado para separar pedidos!

Ocorre ao clicar em `SEPARAR` na tela inicial do aplicativo. Há uma validação de segurança no sistema que desloga o usuário todos os dias, para que force-o a reinserir seu código. 

![image](http://hunes.com.br/imagens/mobile/pickngo/027.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/028.png)
>Caso o aplicativo tente deslogar o usuário e não obtenha êxito, ele deverá ser deslogado manualmente acessando o menu e clicando em `Logout`

#### O código XXXXXXXX não consta para separação!!

Ocorre ao digitar/ler o código de barras de um produto na aba `LEITURA` da separação de produtos. Está validação se dá do fato de que o código digitado/lido não corresponde a nenhum produto da lista de itens da aba `CONSULTA`.

![image](http://hunes.com.br/imagens/mobile/pickngo/029.png)
> Talvez o código tenha sido lido de forma incorreta, tente repetir a leitura.

#### Erros na leitura de Código Único

![image](http://hunes.com.br/imagens/mobile/pickngo/030.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/031.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/032.png)
![image](http://hunes.com.br/imagens/mobile/pickngo/033.png)

```C#
/// <summary>
/// Validate if fullBarcode is correct form.
/// </summary>
/// <param name="fullBarcode">Combination of barcode with packing.</param>
/// <param name="barcode">Barcode of item.</param>
/// <param name="packing">Packing of item.</param>
private void ToValidateBarcode(string fullBarcode, out string barcode, out string packing)
{
    var matriz = fullBarcode.Split('l');

    if (matriz.Count() != 2)
        throw new Exception("Identificador da identificação única não encontrado.");
    else if (string.IsNullOrWhiteSpace(matriz[0]) || string.IsNullOrWhiteSpace(matriz[1]))
        throw new Exception("Identificador da identificação única está ausente ou inválido.");
    else if (matriz[0].Length != 14)
        throw new Exception("Numeração da identificação única com tamanho inválido.");
    else if (itemPicked.Any(a => a.Emabalagem == fullBarcode))
        throw new Exception("A identificação única já está sendo utilizada.");

    barcode = matriz[1];
    packing = fullBarcode;
}
```

##### Formato de Código único correto.

A primeira parte com 14 caracteres, separado com um 'l' e em seguida de 1 a 16 caractes.
`Exemplo: 00000000000000l0000000000000000`

##### Identificador da identificação única não encontrado.

Erro ocorrido quando o código único possuí mais ou menos de duas partes.
`Exemplo 1: 00000000000000l000000l000000` `Exemplo 2: 00000000000000000l`

##### Identificador da identificação única está ausente ou inválido.

Ocorre quando uma das duas partes está em branco.
`Exemplo 1: 00000000000000000l` `Exemplo 2: l00000000000000000`

##### Numeração da identificação única com tamanho inválido.

Ocorre quando a primeira parte do código tem a quantidade de caracteres diferente de 14
`Exemplo : 0000l00000000000000000`

##### A identificação única já está sendo utilizada.

Ocorre quando é lido o código de um produto que já está separado.

[Topo](https://github.com/peedroca/documentations/blob/master/Pick%20'n'%20Go/errosMapeados.md#erros-mapeados)
