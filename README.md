# Make Mask

## **Utilização**

Para utilizar as mascaras no seu input basta colar  as linhas de código abaixo no seu html.
```html
<!-- jquery-1.2.6.pack.js -->
        <script type="text/javascript" src="https://www.geradorcpf.com/assets/js/jquery-1.2.6.pack.js"></script>
    
    <!-- jquery.maskedinput-1.1.4.pack.js -->
    <script type="text/javascript" src="https://www.geradorcpf.com/assets/js/jquery.maskedinput-1.1.4.pack.js"></script>
    
    <!--Arquivo de configuração das masks-->
    <script src="js/mask.js"></script>
```

Em seguida, basta definir um input, o qual irá receber a mascara, e passar uma das id que já esta registrada no 
arquivo *mask.js*, vejamos:

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
No Arquivo html:
```html
    <!--No arquivo html-->
    <input name = "cpf" type="text" id = "cpf">
```

Resultado:

GIF

![Alt Text](https://media.giphy.com/media/McyYNoWGYaOkWypMgF/giphy.gif)
