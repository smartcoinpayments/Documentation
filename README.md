Bem vindo à [Smartcoin](https://smartcoin.com.br)

Vamos começar!

### Primeira vez?
Se é sua primeira vez, vamos ser rápidos para você experimentar a Smartcoin. Queremos te mostrar como mudar a forma de fazer pagamentos online no Brasil.


**1)** Se no seu site ainda não tem [jQuery](http://jquery.com/), inclua-o (versão 1.7.0 ou posterior) no head de todas as suas páginas (veja código exemplo abaixo):
````html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
````

**2)** Em seguida inclua o Smartcoin JavaScript no final do head de todas as suas páginas (código exemplo abaixo):
````html
<script type="text/javascript">
  var _smartcoin_api_key = 'pk_test_407d1f51a61756'; //caso já tenha a sua chave, troque-a para a transação aparecer no seu Manage

  var headTag = document.getElementsByTagName("head")[0];
  var smartTag = document.createElement('script');
  smartTag.type = 'text/javascript';
  smartTag.async = false;
  smartTag.src = 'https://js.smartcoin.com.br/v1/smartcoin.js';
  headTag.appendChild(smartTag);
</script>
````

**3)** Por último inclua o código abaixo para inserir o Smart Checkout na sua página de checkout (código exemplo abaixo):
````html
<!-- A URL do action é apenas para o demo deste tutorial. Você deve criar a sua própria para fazer a sua integração  -->
<form id="formId" action="https://smartcheckout.herokuapp.com/" method="POST">
   <script src="https://checkout.smartcoin.com.br/smart_checkout.js"
      data-description="Hello world!"
      data-amount="100"
      data-button-label="Comprar agora!" >
    </script>
 </form>
````
**Aviso 1:** O mais legal é que você pode fazer várias personalizações do Smart Checkout, [veja aqui como](https://github.com/smartcoinpayments/Documentation/wiki/Smart-Checkout).

**Aviso 2:** A URL do atributo action do form é um exemplo e deve ser substituída pela sua. [Veja nosso exemplo](https://github.com/smartcoinpayments/smartcoin-heroku) de como criar um serviço no Heroku para processar as suas transações.

**4)** Agora é só testar e experimentar a nova experiência que o seu e-commerce irá proporcionar para os seus clientes! :)

### Minhas próprias chaves de acesso a API da Smartcoin:
Para obter suas prórias chaves de acesso à API da Smartcoin, visite o website da [Smartcoin](https://smartcoin.com.br/) e crie um [cadastro](https://manage.smartcoin.com.br/#/signup). Ao se cadastrar no Smart Manage vá em **Menu -> Ajustes -> Chaves API**. Lá você encontrará dois pares de chaves, **API Key** e **Secret Key** (Secret Key é secreta e não deve ser publicada), para os ambientes test (sandbox) e live (produção). Enquanto estiver fazendo a integração, use o par de chaves do ambiente test. Quando a integração estiver completa, troque pelo par de chaves do ambiente live. Ah, muito importante: antes de poder usar o par de chaves do ambiente live é preciso fazer a [Ativação da Conta](https://github.com/smartcoinpayments/Documentation/wiki/Ativa%C3%A7%C3%A3o-da-Conta).

### Saiba mais:
1. [Smart Checkout](https://github.com/smartcoinpayments/Documentation/wiki/Smart-Checkout) (personalize o seu Smart Checkout)
2. Bibliotecas (envie as cobranças via servidor para a Smartcoin):
    * [- PHP](https://github.com/smartcoinpayments/smartcoin-php)
    * [- Ruby](https://github.com/smartcoinpayments/smartcoin-ruby)
3. Plugins (faça integração com sua plataforma de e-commerce de forma rápida e fácil):
    * [- WooCommerce](https://github.com/smartcoinpayments/smartcoin-woo)
    * [- PrestaShop](https://github.com/smartcoinpayments/smartcoin-prestashop)
4. [Solução com Heroku](https://github.com/smartcoinpayments/smartcoin-heroku)
