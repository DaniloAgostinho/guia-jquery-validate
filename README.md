Validar formulários com Jquery Validate
===================

![](https://camo.githubusercontent.com/02ed3f6695f288aedec24c2a329c667281efef5f/687474703a2f2f707265636973696f6e2d736f6674776172652e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031342f30342f6a5175726572792e676966)

Web site
----------

### <a href="https://jqueryvalidation.org/">Jquery validate</a>

CDNS Necessarias
----------
``` html
<script src="https://code.jquery.com/jquery-2.1.4.js"></script>

<script  src="http://ajax.aspnetcdn.com/ajax/jquery.validate/1.15.0/jquery.validate.js"></script>
``` 

Estrutura do form simples
-------------

``` html
<form id="validacao">
  <p>
    <label for="nome"></label>
    <input id="nome" name="nome" minlength="2" type="text" placeholder="Nome" required>
  </p>
  
  <p>
    <label for="email"></label>
    <input id="email" type="email" name="email" placeholder="email" required>
  </p>

    
    <p>
      <label for="mensagem"></label>
      <textarea id="mensagem" name="mensagem" placeholder="Mensagem" required></textarea>
    </p>
  
    <p>
      <input class="submit" type="submit" value="Enviar">
    </p>
  
</form>
```

Personalizando as Respostas
----------

``` Jquery
$("#validacao").validate({
       rules : {
             nome:{
                    required:true,
                    minlength:3
             },
             email:{
                    required:true
             },
             mensagem:{
                    required:true
             }                                
       },
       messages:{
             nome:{
                    required:"Por favor, informe seu nome",
                    minlength:"O nome deve ter pelo menos 3 caracteres"
             },
             email:{
                    required:"É necessário informar um email endereço de e-mail válido!"
             },
             mensagem:{
                    required:"A mensagem não pode ficar em branco"
             }     
       }
});
```


Callback com estilos
----------


``` Css
 .error{ color:red;}
 .success{ color:green;}
```

Ver Demo
----------

[Click aqui!](http://daniloagostinho.github.io/tutorial)
