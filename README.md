
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Surpresa para Evelyn 💖</title>
  <style>
    /* Estilos gerais */
    body {
      font-family: 'Poppins', Arial, sans-serif;
      background-image: url('https://wallpapercave.com/wp/wp9602008.jpg'); /* Coloque o URL da sua imagem aqui */
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      text-align: center;
      color: white;
      margin: 0;
      padding: 0;

      
    }

    .container {
      max-width: 900px;
      margin: 5% auto;
      padding: 40px;
      background-color: rgba(0, 0, 0, 0.8);
      border-radius: 30px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.7);
      animation: fadeIn 1s ease-in-out;
    }

    @keyframes fadeIn {
      0% { opacity: 0; }
      100% { opacity: 1; }
    }

    h1 {
      font-size: 50px;
      color: #FFC0CB;
      text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.4);
      margin-bottom: 20px;
    }

    p {
      font-size: 22px;
      line-height: 1.6;
      margin-bottom: 20px;
    }

    select {
      padding: 15px;
      font-size: 18px;
      border-radius: 8px;
      border: none;
      background-color: rgba(255, 255, 255, 0.9);
      color: black;
      width: 100%;
      margin-bottom: 20px;
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
      transition: 0.3s ease;
    }

    select:hover {
      background-color: rgba(255, 255, 255, 0.6);
    }

    button {
      padding: 15px 30px;
      font-size: 20px;
      background-color: #FF77A9;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(255, 119, 169, 0.5);
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: #ff4d8d;
      transform: scale(1.05);
    }

    #feedback {
      color: #FFC0CB;
      font-size: 18px;
      margin-top: -10px;
      display: none;
    }

    #finalMessage {
      display: none;
      font-size: 24px;
      font-weight: bold;
      color: #FFC0CB;
      margin-top: 20px;
      padding: 20px;
      background-color: rgba(0, 0, 0, 0.7);
      border-radius: 10px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
      text-align: center;
      max-width: 800px;
      margin: 30px auto;
    }

    blockquote {
      font-size: 22px;
      color: #FFB6C1;
      font-style: italic;
      margin-top: 20px;
      text-align: center;
    }

    .question {
      display: none;
    }

    .question.active {
      display: block;
    }

    #quiz {
      display: none;
    }

    .start-button {
      padding: 20px 40px;
      font-size: 24px;
      background-color: #FF4D8D;
      border: none;
      border-radius: 15px;
      color: white;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 5px 15px rgba(255, 77, 141, 0.6);
    }

    .start-button:hover {
      background-color: #e43a69;
      transform: scale(1.1);
    }
    

  </style>
</head>
<body>

<div class="container">
  <h1>💖 Bem-vinda, Evelyn! 💖</h1>
  <p>Preparei uma surpresa especial para você! Feliz 2.2 💖💖💖. Responda as perguntas até o final 😊</p>
  <button class="start-button" id="startBtn">Começar</button>

  <div id="quiz">
    <!-- Perguntas -->
    <div class="question" data-question="1">
      <p>Onde foi nosso primeiro encontro?</p>
      <select id="q1" onchange="validateAnswer(0)">
        <option value="">Selecione...</option>
        <option value="amazonas shopping">Amazonas Shopping</option>
        <option value="ponta negra">Ponta Negra</option>
        <option value="praia">Praia</option>
        <option value="casa">Nossa casa</option>
        <option value="academia">Academia</option>
      </select>
    </div>

    <div class="question" data-question="2">
      <p>Nosso aniversário de namoro é no dia 26 ou 27 de setembro?</p>
      <select id="q2" onchange="validateAnswer(1)">
        <option value="">Selecione...</option>
        <option value="27/09">27 de setembro</option>
        <option value="26/09">26 de setembro</option>
        <option value="29/09">29 de setembro</option>
        <option value="28/09">28 de setembro</option>
        <option value="25/09">25 de setembro</option>
      </select>
    </div>

    <div class="question" data-question="3">
      <p>O que eu mais amo em você?</p>
      <select id="q3" onchange="validateAnswer(2)">
        <option value="">Selecione...</option>
        <option value="tudo">Tudo</option>
        <option value="seu sorriso">Seu sorriso</option>
        <option value="seu cabelo">Seu cabelo</option>
        <option value="seu olhar">Seu olhar</option>
        <option value="seu carinho">Seu carinho</option>
      </select>
    </div>

    <div class="question" data-question="4">
      <p>Onde começou nossa química?</p>
      <select id="q4" onchange="validateAnswer(3)">
        <option value="">Selecione...</option>
        <option value="academia">Na academia</option>
        <option value="shopping">No shopping</option>
        <option value="faculdade">Na faculdade</option>
        <option value="praia">Na praia</option>
        <option value="restaurante">No restaurante</option>
      </select>
    </div>

    <div class="question" data-question="5">
      <p>Em uma escala de 0 a 10, o quanto eu te amo?</p>
      <select id="q5" onchange="validateAnswer(4)">
        <option value="">Selecione...</option>
        <option value="10">10</option>
        <option value="infinito">Ao infinito</option>
        <option value="5">5</option>
        <option value="20">20</option>
        <option value="100">100</option>
      </select>
      <div id="feedback" style="display: none;"></div>
    </div>

    <div class="question" data-question="6">
      <p>O nome do seu fã número 1?</p>
      <select id="q6" onchange="validateAnswer(5)">
        <option value="">Selecione...</option>
        <option value="gustavo">Gustavo</option>
        <option value="pedro">Pedro</option>
        <option value="felipe">Felipe</option>
        <option value="lucas">Lucas</option>
        <option value="bruno">Bruno</option>
      </select>
    </div>

    <div class="question" data-question="7">
      <p>Quem é a pessoa mais linda, inteligente, cheirosa, carismática, gentil e doce do mundo???</p>
      <select id="q7" onchange="validateAnswer(6)">
        <option value="">Selecione...</option>
        <option value="eu">Eu</option>
        <option value="você">Você</option>
        <option value="deus">Deus</option>
        <option value="mãe">Minha mãe</option>
        <option value="irma">Minha irmã</option>
      </select>
    </div>

    <div class="question" data-question="8">
      <p>Qual a nossa música preferida?</p>
      <select id="q8" onchange="validateAnswer(7)">
        <option value="">Selecione...</option>
        <option value="you are the right one">You Are the Right One</option>
        <option value="perfect">Perfect</option>
        <option value="thinking out loud">Thinking Out Loud</option>
        <option value="amazing grace">Amazing Grace</option>
        <option value="marry me">Marry Me</option>
      </select>
    </div>

    <div class="question" data-question="9">
      <p>Gostaria de permanecer ao meu lado até a eternidade?</p>
      <select id="q9" onchange="validateAnswer(8)">
        <option value="">Selecione...</option>
        <option value="sim com certeza sim">Sim, com certeza sim</option>
        <option value="sim">Sim</option>
        <option value="nao">Não</option>
        <option value="talvez">Talvez</option>
        <option value="quem sabe">Quem sabe</option>
      </select>
    </div>

    <!-- Mensagem final -->
    <div id="finalMessage">
      <h2>💖 Você acertou todas as respostas, meu amor! 💖</h2>
      <p>Como presente para você, uma mensagem especial:</p>
      <blockquote>
        "Te amo mais do que palavras podem expressar, mais do que todos os idiomas podem traduzir. Você é o meu sonho realizado, a razão do meu sorriso e do meu coração. Quero passar o resto da minha vida ao seu lado, crescendo juntos e enfrentando tudo com amor. Cada dia com você é uma bênção, e eu prometo amar você até o infinito, até a eternidade. Obrigado por ser a minha razão de viver, a minha maior alegria, minha melhor amiga e minha alma gêmea. Não há palavras suficientes para agradecer por ter você ao meu lado, e vou continuar a te amar com todo o meu coração, sempre e para sempre."
      </blockquote>
    </div>
  </div>
</div>

<script>
  document.getElementById("startBtn").onclick = function() {
    document.getElementById("quiz").style.display = "block";
    this.style.display = "none";
    showQuestion(0);
  }

  let currentQuestion = 0;
  const totalQuestions = 9;

  function showQuestion(questionIndex) {
    const questions = document.querySelectorAll(".question");
    questions.forEach(question => {
      question.classList.remove("active");
    });
    questions[questionIndex].classList.add("active");
  }

  function validateAnswer(questionIndex) {
    const correctAnswers = [
      "amazonas shopping",
      "27/09",
      "tudo",
      "academia",
      "infinito",
      "gustavo",
      "eu",
      "you are the right one",
      "sim com certeza sim"
    ];

    const userAnswer = document.getElementById(`q${questionIndex + 1}`).value;

    if (userAnswer === correctAnswers[questionIndex]) {
      currentQuestion++;
      if (currentQuestion < totalQuestions) {
        showQuestion(currentQuestion);
      } else {
        document.getElementById("finalMessage").style.display = "block";
      }
    }
  }
</script>

</body>
</html>
