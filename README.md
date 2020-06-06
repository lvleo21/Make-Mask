# Make Mask

## **Utilização**

Para utilizar as máscaras no seu input basta colar  as linhas de código abaixo no seu html.
```html

    <!-- jquery-1.2.6.pack.js -->
    <script type="text/javascript" src="https://www.geradorcpf.com/assets/js/jquery-1.2.6.pack.js"></script>
    
    <!-- jquery.maskedinput-1.1.4.pack.js -->
    <script type="text/javascript" src="https://www.geradorcpf.com/assets/js/jquery.maskedinput-1.1.4.pack.js"></script>
    
    <!--Arquivo de configuração das masks-->
    <script src="js/mask.js"></script>

```

Em seguida, basta criar uma tag **input** e passar uma das id's que já estão registradas no arquivo **mask.js**, vejamos:

No Arquivo **mask.js**:

```javascript
    $(document).ready(function(){
        $("#cpf").mask("999.999.999-99");
        $("#rg").mask("9.999.999");
        $("#sus").mask("999 9999 9999 9999");
        $("#cnpj").mask("99.999.999/9999-99");
        $("#date").mask("99/99/99");
        $("#time").mask("99:99:99");
        $("#date_time").mask("99/99/99 99:99:99");
        $("#landline").mask("(99) 9999-9999");
        $("#mobile_phone").mask("(99) 99999-9999");
    });
```

No Arquivo **html**:

```html
    <!--No arquivo html-->
    <input name = "cpf" type="text" id = "cpf">
```

### Resultado:

![Alt Text](https://media.giphy.com/media/McyYNoWGYaOkWypMgF/giphy.gif)

## Criando uma Mascara

Para criar uma mascara, primeiro precisamos entender que:

- A mascara só suporta números inteiros;

Com isso em mente, vamos agora para o arquivo **mask.js** e no escopo de function, onde já existe registro de outras máscaras, iremos registrar uma nova linha, vejamos:

```javascript
    $("#").mask("");
```    

Após o **#** iremos definir o nome do identificador da mascara. Em seguida, dentro das aspas duplas, vamos inserir a forma que nossa mascara deve se comportar, para isso precisamos seguir uma regra:

- a identificação do digito da máscara é representado pelo número **9**, ou seja, onde tiver o número **9** será onde haverá um digito no input;

```javascript
    $("#exemplo").mask("9.9.9.9.9");
```    

Para este exemplo, defini o nome da minha máscara como **exemplo** e ela irá receber os valores(onde houver 9 será um número inteiro) **9.9.9.9.9**.

Agora, no Arquivo **html**:

```html
    <!--No arquivo html-->
    <input name = "exemplo" type="text" id = "exemplo">
```

### Resultado:

![Alt Text](https://media.giphy.com/media/j38dsd71fjzSx4dgZq/giphy.gif)