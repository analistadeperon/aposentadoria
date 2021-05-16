# aposentadoria
<script> autoria Matheus Deperon 16/05/2021
 var nome = prompt("Informe o seu nome:");
 var sexo = prompt("Informe o seu sexo :'M - Masculino' ou 'F - Femenino'");
 
 if(sexo =="M" || sexo == "m" || sexo == "F" || sexo == "f"){
  var anoNasci = parseFloat(prompt("Informe o seu ano de nascimento!"));
  
  if(anoNasci <= 2018){
   var idade = 2018 - anoNasci;     
   if(idade >= 20){ 
    var anoEmpresa = parseFloat(prompt("Informe o ano que vc entrou na empresa:"));
    var tempoServico = 2021 - anoEmpresa ;
 
    if(sexo == "M" || sexo =="m"){
     if(idade >= 65 || tempoServico >= 30){
      document.write("<p>Senhor:" + nome +
         "A sua idade e de:" + idade +
         "<br />E seu tempo de serviço e de:" + tempoServico+
         "<br />Voce pode Requerer aposentadoria");
     }else{
      document.write("<p>Senhor:" +nome +
          "<br />A sua idade e de:" + idade +
          "<br />E seu tempo de serviço e de:" + tempoServico+
          "<br />Voce ainda não pode Requerer aposentadoria");
     } 
    }else { 
     if(idade >= 60 || tempoServico >= 25){
      document.write("<p>Senhora:" + nome +
          "A sua idade e de:" + idade +
          "<br />E seu tempo de serviço e de:" + tempoServico+
          "<br />Voce pode Requerer aposentadoria");
     }else{
      document.write("<p>Senhora:" +nome +
          "<br />A sua idade e de:" + idade +
          "<br />E seu tempo de serviço e de:" + tempoServico+
          "<br />Voce ainda não pode Requerer aposentadoria");
     } 
    }
   }else{
    document.write("<p>Voce não pode trabalhar no momento"+
        "<br />Voce so pode ter a carteira Assinada apos os 14 anos de idade"+
        "<br />E voce esta com:" + idade +
        "<br />De um F5 para continuar"); 
   }
  }else{
   document.write("Informe a idade correta"+
       "<br />De um F5 para continuar");
  }
 }else{
  document.write("Codigo do sexo invalido"+
      "De um F5 para continuar!");
 }
</script>
_________________________________________________________________________________

No mercado, o preço da laranja varia em função da dúzia. Se o cliente comprar menos do
que 12 laranjas paga $10, mas se comprar pelo menos 12 laranjas paga $8. Desenvolva um
programa que calcule o preço a pagar em função do número de laranjas que o cliente
pretende levar.

<script>
 var quant = parseInt(prompt("Informe a quantia de laranja comprada"));
 if(quant >= 12){
  document.write("Voce vai pagar R$:" +quant * 0.66);
 }else{
  document.write("Voce vai pagar R$:" +quant * 0.83);
 }
</script>
_________________________________________________________________________________
A jornada de trabalho é de 45 horas semanais. O funcionário que trabalhar mais horas do
que essas horas, terá direito a horas extras. O valor da cada hora extraordinária é 30% do
valor da hora normal de trabalho. O funcionário trabalha 22 dias por mês. Faça um
programa que recebe o número de horas mensais de trabalho e o salário de base de um
funcionário e imprime o salário total.

<script>
 
 var nome = prompt("Informe o seu nome");
 var sexo = prompt("Informe o seu sexo :'M - Masculino' ou 'F - Femenino'");
 
 if(sexo =="M" || sexo == "m" || sexo == "F" || sexo == "f"){
  var horasTrab = parseInt(prompt("Informe quantas horas vc trabalhou nesse mes!"));
  var salarioBase = parseFloat(prompt("Informe o seu salario Base!")); 
  var horasExtra = horasTrab - 198; 
  var valorHoraExtra = ((salarioBase / 198)*0.30)+(salarioBase /198); 
  var salarioFinal = salarioBase+(horasExtra * valorHoraExtra); 
 
  if(horasTrab == 198){
   document.write("<p>senhor:" + nome +
       "<br />Horas trabalhada:" +horasTrab+
       "<br />Voce teve em horas extras:" +horasExtra+
       "<br />O seu salario e de:"+ salarioFinal);
  }else if(horasTrab > 198){
   document.write("<p>senhor:" + nome +
       "<br />Horas trabalhada:" +horasTrab+
       "<br />Voce teve em horas extras:" +horasExtra+
       "<br />O seu salario e de:"+ salarioBase+
       "<br />O seu salario final eh:"+ salarioFinal);
  }else{
   document.write("<p>senhor:" + nome +
       "<br />Horas trabalhada:" +horasTrab+
       "<br />Voce esta devendo em horas extras:" +horasExtra+
       "<br />O seu salario e de:"+ salarioBase+
       "<br />O seu salario final eh:"+ salarioFinal);
  }
 }else{
  document.write("Codigo do sexo invalido"+
      "De um F5 para continuar!");
 }
</script>
_________________________________________________________________________________

Numa determinada escola, a prova opcional PO, substitui obrigatoriamente menor nota que
o aluno teve nas duas provas parciais, se está for maior do que uma delas. Dadas as notas
P1, P2 e PO, determinar o valor da media final do um aluno apôs consultar a prova opcional.

<script>
 var p1 = parseFloat(prompt("Informe o valor da primeira prova!"));
 var p2 = parseFloat(prompt("Informe o valor da segunda prova!"));
 var po = parseFloat(prompt("Informe o valor da prova opcional!"));
 
 if(p1 >= po && p2 >= po){
  var media = (p1 + p2)/2;
  document.write("A sua media e de:" +media);
 
 }else if(p1 < po && p1 <=p2){
  var media = (po + p2)/2;
  document.write("A sua media e de:" + media);
 }else{
  var media = (po + p1)/2;
  document.write("A sua media e de:" +media);
 }
</script>
