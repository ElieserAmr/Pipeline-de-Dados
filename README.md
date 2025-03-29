# <h1>Pipeline de dados do telegram :telephone_receiver: <h1>

<li><a href="https://www.kaggle.com/code/elieseramorim/pipeline-de-dados-do-telegram">Storytellyng no kagle </a></li> 
<li><a href="https://www.linkedin.com/in/elieser-amorim-392b03327/">Linkedin </a></li> 
 <h2>Neste repositorio crio uma piplane de dados no telegram.<h2>



  <h3>Tendo em vista o grande volume de dados fornecidos atraves de aplicativos de mensagem, este projeto visa a criação de um bot, juntamente com uma API, para o auxilio da captção de dados e atendimento ao cliente atraves de um grupo no telegram.<h3>

  <h3>Aqui vemos alguns beneficios em utilizar bots para à captura de dados:<h3>
    
  :white_check_mark: Redução do trabalho manual.
  
  :white_check_mark: Integração a bancos de dados e desboards.
  
  :white_check_mark: Organozação de informações.
  

  <h3>Aqui trago algumas das tecnologias e bibliotecas utlizadas:<h3>

  :one: Primeiramente criaremos um chat bot, utilizando a ferramenta **Botfather** do proprio telegram 🤖
  
  :two: Apos a criação do bot é necessario adicionalo em um grupo do telegram, e dar a ele permissão de admininstrador, para que ele possa realizar a captura de mensagens através de uma API.
  
  :three: Utilizando o pacote **json**, vamos denormalizar o contedudo da mensagem.
  
  :four: Utilizando o pacote **pyarrow**, criaremos entao uma tabela com os dados processados.
  
  :five: Com o   **AWS S3**, criaremos um bucket para o armazenamento em nuvem dos dados crus e dos dados limpos, utilizando os sufixos "-raw" e "enriched".      
  
  :six: Utilizaremos também o **AWS LAMBDA**, para persistir as mensagens captadas pelo bot do Telegram em seu formato original, no bucket do s3
  
  :seven: Também sera necessario a criação de uma gatilho para o qual sera utiizado o **AWS API GATWAY**, tendo a função de receber as mensagens do bot e iniciar uma função lambda.
  
  :eight: Por fim utilizaremos o **AWS Event Bridge** que cria uma automação da captação das mensagen e do seu tratamento.
  
