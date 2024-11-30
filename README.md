Meu Portfólio - README
Visão Geral
Este repositório contém um portfólio pessoal que exibe informações sobre minha carreira, habilidades, certificações e recomendações. Ele foi projetado com HTML, CSS, e JavaScript, utilizando o Bootstrap para responsividade e a biblioteca Owl Carousel para um carrossel de depoimentos. Este projeto foi criado com o intuito de mostrar minhas habilidades em desenvolvimento web, incluindo a criação de layouts interativos e responsivos.

Estrutura do Projeto
O projeto é composto pelas seguintes partes principais:

1. Carrossel de Depoimentos (Testimonials)
Este script permite que depoimentos sejam exibidos em um carrossel com três itens. A biblioteca Owl Carousel é usada para criar um carrossel funcional, que é ajustável para diferentes tamanhos de tela (responsivo). O comportamento do carrossel pode ser modificado com as opções de configuração:

Itens visíveis: 1, 2 ou 3 dependendo do tamanho da tela.
Navegação: Ativada para telas grandes (acima de 1000px) e desativada em telas menores.
Código JavaScript (main.js):
javascript
Copiar código
(function () {
    "use strict";
  
    var carousels = function () {
      $(".owl-carousel1").owlCarousel({
        loop: true,
        center: true,
        margin: 0,
        responsiveClass: true,
        nav: false,
        responsive: {
          0: {
            items: 1,
            nav: false
          },
          680: {
            items: 2,
            nav: false,
            loop: false
          },
          1000: {
            items: 3,
            nav: true
          }
        }
      });
    };
  
    (function ($) {
      carousels();
    })(jQuery);
})();
2. Troca de Conteúdo de Cards (Portfolio Sections)
Este script permite que, ao clicar em um botão, o conteúdo de uma seção de cards seja substituído dinamicamente, exibindo diferentes informações de portfólio. São três seções: App, Design e Web, com conteúdo específico sendo adicionado no container de cards quando cada botão é clicado.

Código JavaScript (Testimonials.js):
javascript
Copiar código
const cardsContainer = document.getElementById('cardsContainer');
const btnApp = document.getElementById('btnApp');
const btnDesign = document.getElementById('btnDesign');
const btnWeb = document.getElementById('btnWeb');

btnApp.addEventListener('click', () => {
  cardsContainer.innerHTML = `
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Card 1</h5>
        <p class="card-text">Conteúdo do Card 1.</p>
      </div>
    </div>
  `;
});

btnDesign.addEventListener('click', () => {
  cardsContainer.innerHTML = `
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Card 2</h5>
        <p class="card-text">Conteúdo do Card 2.</p>
      </div>
    </div>
  `;
});

btnWeb.addEventListener('click', () => {
  cardsContainer.innerHTML = `
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Card 3</h5>
        <p class="card-text">Conteúdo do Card 3.</p>
      </div>
    </div>
  `;
});
3. Portfólio HTML - Estrutura do Layout
O HTML contém várias seções principais, incluindo Sobre Mim, Licenças e Certificados, Soft Skills e Hard Skills.

Sobre Mim: Apresentação pessoal com foto e texto descritivo sobre a trajetória e experiência profissional.
Licenças e Certificados: Cards exibindo informações sobre certificações.
Soft Skills & Hard Skills: Seções de habilidades com ícones representando as habilidades do usuário e uma barra de progresso que indica o nível de conhecimento em cada habilidade.
Exemplo de HTML (Para a seção "Sobre Mim"):
html
Copiar código
<section class="mt-2" id="about">
    <div class="container">
        <div class="text-center">
            <h1 class="d-inline-flex title-section underline-text">
                Sobre mim
            </h1>
            <p class="lead text-white roboto-300">
                Conheça um pouco sobre mim e minha história com a tecnologia!
            </p>
        </div>

        <div class="row align-items-center">
            <div class="col-md-6">
                <img src="minha-foto.jpg" class="rounded-end-4 border-img img-fluid" alt="Foto de perfil" />
            </div>
            <div class="col-md-6">
                <h2 class="my-5 title title-section ">Cientista de Dados Junior</h2>
                <p class="lead text-white roboto-300">
                    Graduando em Ciências de Dados pela UFC, sou Técnico em Comércio pela EEEP de Uruburetama...
                </p>
            </div>
        </div>
    </div>
</section>
4. Uso de Bibliotecas e Recursos Externos
Bootstrap: Usado para o layout responsivo e componentes como botões, navegação e cards.
Font Awesome: Ícones para representar habilidades como HTML, CSS, JavaScript, Python, entre outros.
Owl Carousel: Biblioteca usada para o carrossel de depoimentos.
Personalização CSS: Personalizações são feitas com o arquivo custom.css para adaptar o design ao estilo desejado.
Tecnologias Utilizadas
HTML5
CSS3
JavaScript (ES6+)
Bootstrap 5
Font Awesome
Owl Carousel
Como Usar
Clone este repositório em sua máquina.
Abra o arquivo index.html em seu navegador para visualizar o portfólio em ação.
Modifique os conteúdos de cada seção conforme necessário para personalizar o portfólio com suas informações pessoais.
Dependências
Bootstrap: Para responsividade e componentes visuais.
Font Awesome: Para ícones.
Owl Carousel: Para o carrossel de depoimentos.
Licença
Este projeto é licenciado sob a Licença MIT - veja o arquivo LICENSE para mais detalhes.

