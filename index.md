### Bem-vindo ao Projeto Transístores

Bem-vindo à página oficial do Projeto Transístores.

A população transsexual é excluída do mercado de trabalho e das universidades. Poucas empresas possuem políticas de inclusão, mas mesmo essas tem dificuldade em encontrar profissionais capacitados.

A ideia desse projeto é capacitar tecnicamente a população transsexual, afastada das universidades, para preencher o mercado de trabalho de tecnologia da informação, que é minha área.

Se você é uma pessoa trans que se interessa por informática e deseja se capacitar em desenvolvimento de aplicações web, preencha o formulário abaixo. Esse projeto é e sempre será gratuito.

Se você é uma pessoa especialista em outra área, desenvolva um projeto como esse. As pessoas trans são tão capazes quanto as pessoas cis, mas essas pessoas não encontram aberturas para ingressar. Faça parte dessa iniciativa e torne-se você, também, uma porta para essa mudança.

Se você possue uma empresa, ou faz parte do departamento de RH de uma empresa, desenvolva políticas de inclusão na sua empresa. Isso pode fazer a diferença para a inclusão dessa comunidade marginalizada.

<!-- modify this form HTML and place wherever you want your form -->

<form id="my-form"
  action="https://formspree.io/mrgydjjw"
  method="POST"
>
  <label>Email:</label>
  <input type="email" name="email" />
  <label>Message:</label>
  <input type="text" name="message" />
  <button id="my-form-button">Submit</button>
  <p id="my-form-status"></p>
</form>

<!-- Place this script at the end of the body tag -->

<script>
  window.addEventListener("DOMContentLoaded", function() {

    // get the form elements defined in your form HTML above
    
    var form = document.getElementById("my-form");
    var button = document.getElementById("my-form-button");
    var status = document.getElementById("my-form-status");

    // Success and Error functions for after the form is submitted
    
    function success() {
      form.reset();
      button.style = "display: none ";
      status.innerHTML = "Thanks!";
    }

    function error() {
      status.innerHTML = "Oops! There was a problem.";
    }

    // handle the form submission event

    form.addEventListener("submit", function(ev) {
      ev.preventDefault();
      var data = new FormData(form);
      ajax(form.method, form.action, data, success, error);
    });
  });
  
  // helper function for sending an AJAX request

  function ajax(method, url, data, success, error) {
    var xhr = new XMLHttpRequest();
    xhr.open(method, url);
    xhr.setRequestHeader("Accept", "application/json");
    xhr.onreadystatechange = function() {
      if (xhr.readyState !== XMLHttpRequest.DONE) return;
      if (xhr.status === 200) {
        success(xhr.response, xhr.responseType);
      } else {
        error(xhr.status, xhr.response, xhr.responseType);
      }
    };
    xhr.send(data);
  }
</script>

[http://especiais.correiobraziliense.com.br/transexuais-sao-excluidos-do-mercado-de-trabalho]
[https://www1.folha.uol.com.br/mercado/2020/01/emprego-formal-ainda-e-excecao-entre-pessoas-trans.shtml]
[https://arte.estadao.com.br/focas/capitu/materia/no-ensino-superior-o-espelho-da-exclusao-de-pessoas-trans]
[http://especiais.correiobraziliense.com.br/violencia-e-discriminacao-roubam-de-transexuais-o-direito-ao-estudo]
