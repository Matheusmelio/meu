css

body {
  --bege: #E6E0D6;
  --marrom-escuro: #816D4F;
  --marrom-claro: #B29463;
  font-family: 'Barlow', sans-serif;
  
  height: 4000px; /* Aumentar o tamanho da tela para aparecer a barra de rolagem */
}

input[type=checkbox] {
  border: 2px solid var(--marrom-claro);
  box-shadow: none;
}

input[type=checkbox]:checked,
input[type="checkbox"]:focus {
  background-color: var(--marrom-claro);
  border-color: var(--marrom-claro);
  box-shadow: none;
  outline: none;
}

.banners-1{
  background-image: url(banner-1.png);
}

.banners{
/* Para a imagem da classe .banners-1 ser exibida é necessário definir width e height */
width: 100%;
height: 100vh;
/* Para a imagem não se repetir */
background-repeat: no-repeat; 
/* para a imagem ocupar todo o espaço da tela */
background-size: cover;
/* para centralizar a imagem */
background-position: center;
/* A tela foi aumentanda para height de 4000px, aparecerá a barra de rolagem, então para fixar a imagem (chaamado de Parallax) */
background-attachment: fixed;
}

.banners-titulo {
  /* testar a opacidade com valores 0, 1 também */
  --bs-bg-opacity: .5;
}

.banner-2{
  background-image: url(banner-2.png);
}

.banner-3{
  background-image: url(banner-3.png);
}



html 

<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Barlow:wght@400;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="estilos.css">
</head>

<body>
  <header>
    <!-- classes expandir o menu responsivo com breakponts - background do nav - menu fixo -->
    <!-- expand-lg tornar responsivo // fixed-top: fico no topo //  -->
    <nav class="navbar-expand-lg navbar bg-body-tertiary fixed-top">
      <div class="container-fluid">
        <a class="navbar-brand" href="#"><img src="logo.png" alt="" srcset=""></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar"
          aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
          <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="offcanvasNavbarLabel"><img src="logo-mobile.png" alt="" srcset="">
            </h5>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Início</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Sobre</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Contato</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">
                  <div class="form-check form-switch">
                    <input class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckDefault">
                    <label class="form-check-label" for="flexSwitchCheckDefault">Modo escuro</label>
                  </div>
                </a>
              </li>

          </div>
        </div>
      </div>
    </nav>

  </header>


  <main>
    <section class="banners banners-1 d-flex flex-column justify-content-center text-center">
      <div class="banners-titulo bg-body-secondary py-5">
        <h2 class="fw-bold">Bem-vindo a cafeteria</h2>
        <p>Cafeteria</p>
      </div>
    </section>


    <!-- SESSÃO NOSSOS SERVIÇOS  -->
    <!-- PARA INSERIR CARDS DO BOOTSTRAP https://getbootstrap.com/docs/4.0/components/card/ -->
    <!-- Cores de botões https://getbootstrap.com/docs/4.0/components/buttons/ -->
    <section class="py-5">
      <h2 class="text-center fw-bold pb-1">Nossos serviços</h2>

      <div class="container d-flex justify-content-around flex-wrap">

        <!-- CARD 1 -->

        <div class="card m-4" style="width: 20rem;">
          <img src="cafe-card.png" class="card-img-top"
            alt="Balcão de padaria tradicional com alimentos diversos">
          <div class="card-body">
            <h5 class="card-title py-2 fw-bold">Café & Bistrô</h5>
            <p class="card-text">Nosso bistrô oferece uma ampla variedade de cafés, smoothies, deliciosos
              salgados e sobremesas. Uma excelente opção para quem busca um lugar tranquilo e
              aconchegante.</p>
            <a href="#" class="btn botao-padrao w-100 fw-bold">Quero detalhes</a>
          </div>
        </div>
        <!-- CARD 2 -->

        <div class="card m-4" style="width: 20rem;">
          <img src="buffet-card.png" class="card-img-top" alt="Mesa de buffet com alimentos diversos">
          <div class="card-body">
            <h5 class="card-title fw-bold">Buffet</h5>
            <p class="card-text">Buffet e catering personalizado para eventos, produções e celebrações. Com
              um menu variado e adaptável às preferências do cliente, atendimento atencioso e
              profissional.</p>
            <a href="#" class="btn btn-primary w-100 fw-bold mt-3">Quero detalhes</a>
          </div>
        </div>
        <!-- CARD 3 -->

        <div class="card m-4" style="width: 20rem;">
          <img src="delivery-card.png" class="card-img-top" alt="Caixa aberta armazenando comidas diversas">
          <div class="card-body">
            <h5 class="card-title fw-bold">Delivery</h5>
            <p class="card-text">Para quem deseja desfrutar no conforto de casa, oferecemos delivery dos
              produtos. Com o mesmo cardápio variado de sempre, sem perder nosso sabor e padrão de
              qualidade.</p>
            <a href="#" class="btn botao-padrao w-100 fw-bold mt-3">Quero detalhes</a>
          </div>
        </div>
      </div>
    </section>





    <!-- d-flex para exibir textos que está oculto no navbar, organizar em colunas e centralizar // fw-bold para negrito -->
    <section class="banners banner-2 d-flex flex-column justify-content-center text-center">
      <div class="banners-titulo bg-body-secondary text-center py-5">
        <h2 class="fw-bold">Portas abertas para todos os públicos.</h2>
        <p>Nosso espaço é aconchegante para receber crianças, pessoas com deficiência e coworking.</p>
      </div>
    </section>


<!-- CARDS COM IMAGENS DE ALIMENTOS -->
    <!-- Espaçamentos: https://getbootstrap.com.br/docs/4.1/utilities/spacing/ -->
    <!-- py-5 é o padding // pb-1 é o padding-bottom para se afastar dos cards inseridos -->

    <section class="py-5">

      <h2 class="fw-bold text-center pb-1">Nossos produtos</h2>

      
        <!-- inserimos o border-0, btn, text-center, fw-bold -->
        <!-- Inserção de classe para responsividade  - - class="col-12 col-md-6 col-lg-4" e colunas row-->

        <div class="row">

          <!-- PRIMEIRO CARD DE ALIMENTOS - CAFÉ TRADICIONAL -->
          <!-- INSERE O data-bs-toggle="modal" data-bs-target="#modal-1 DO MODAL ESCOLHIDO -->
          <div class="col-12 col-md-6 col-lg-4">
              <div class="card border-0 mx-auto btn" data-bs-toggle="modal" data-bs-target="#modal-1"
                  style="width: 18rem;">
                  <img src="produtos-cafe-tradicional.png" class="card-img-top" alt="Café preto.">
                  <div class="card-body">
                      <h3 class="card-text text-center fw-bold text-nowrap">Cafés Tradicionais</h3>
                  </div>
              </div>
          </div>

          <div class="col-12 col-md-6 col-lg-4">
            <div class="card border-0 mx-auto btn" data-bs-toggle="modal" data-bs-target="#modal-1"
                style="width: 18rem;">
                <img src="produtos-cafe-tradicional.png" class="card-img-top" alt="Café preto.">
                <div class="card-body">
                    <h3 class="card-text text-center fw-bold text-nowrap">Cafés Tradicionais</h3>
                </div>
            </div>
        </div>

        <div class="col-12 col-md-6 col-lg-4">
          <div class="card border-0 mx-auto btn" data-bs-toggle="modal" data-bs-target="#modal-1"
              style="width: 18rem;">
              <img src="produtos-cafe-tradicional.png" class="card-img-top" alt="Café preto.">
              <div class="card-body">
                  <h3 class="card-text text-center fw-bold text-nowrap">Cafés Tradicionais</h3>
              </div>
          </div>
      </div>

      <div class="col-12 col-md-6 col-lg-4">
        <div class="card border-0 mx-auto btn" data-bs-toggle="modal" data-bs-target="#modal-1"
            style="width: 18rem;">
            <img src="produtos-cafe-tradicional.png" class="card-img-top" alt="Café preto.">
            <div class="card-body">
                <h3 class="card-text text-center fw-bold text-nowrap">Cafés Tradicionais</h3>
            </div>
        </div>
    </div>

    <div class="col-12 col-md-6 col-lg-4">
      <div class="card border-0 mx-auto btn" data-bs-toggle="modal" data-bs-target="#modal-1"
          style="width: 18rem;">
          <img src="produtos-cafe-tradicional.png" class="card-img-top" alt="Café preto.">
          <div class="card-body">
              <h3 class="card-text text-center fw-bold text-nowrap">Cafés Tradicionais</h3>
          </div>
      </div>
  </div>

  <div class="col-12 col-md-6 col-lg-4">
    <div class="card border-0 mx-auto btn" data-bs-toggle="modal" data-bs-target="#modal-1"
        style="width: 18rem;">
        <img src="produtos-cafe-tradicional.png" class="card-img-top" alt="Café preto.">
        <div class="card-body">
            <h3 class="card-text text-center fw-bold text-nowrap">Cafés Tradicionais</h3>
        </div>
    </div>
</div>


          <!-- INSERIR (TROCAR) MAIS CINCO CARDS E MODAIS CORRESPONDENTES QUES ESTÃO NA <DIV> <\DIV> ACIMA -->

    
<!-- INSERIR O FORMS LOCALIZADOS TAMBÉM NO SITE DO BOOTSTRAP  -->
<!-- py-4: espaçamento da sessão // container: classe de container da sessão do formulário // mx-auto: centralizar // rounded: bolear as bordas // p-3: espaçamento //  -->
            <section class="py-4 container">
              <div class="row">
                <div class="col-10 col-xl-8 mx-auto">
                  <div class="border border-2 rounded p-3">
                    <h3 class="fw-bold p-3">Entre em contato!</h3>
                    <form id="contato">
                      <div class="form-floating mb-3">
                        <input type="text" class="form-control" id="floatingNome" placeholder="Nome">
                        <label for="floatingNome">Nome</label>
                      </div>
                      <div class="form-floating mb-3">
                        <input type="email" class="form-control" id="floatingEmail" placeholder="name@example.com">
                        <label for="floatingEmail">Email</label>
                      </div>
                      <div class="form-floating mb-3">
                        <input type="number" class="form-control" id="floatingTelefone" placeholder="Telefone">
                        <label for="floatingTelefone">Telefone</label>
                      </div>
                      <select class="form-select mb-3" aria-label="Default select example">
                        <option selected>Preferência de contato:</option>
                        <option value="1">WhatsApp</option>
                        <option value="2">Email</option>
                        <option value="3">Ligação</option>
                      </select>
                      <label for="nivel-satisfacao" class="form-label">Nível de satisfação:</label>
                      <input type="range" class="form-range input-range" id="nivel-satisfacao">
                      <div class="form-check">
                        <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
                        <label class="form-check-label" for="flexCheckDefault">
                          Deseja receber novidades por email?
                        </label>
                      </div>
                      <button type="button" class="btn btn-primary w-100 fw-bold mt-3 py-3">Enviar</button>
                    </form>
                  </div>
                </div>
              </div>
      
            </section>
      
            <footer class="text-center bg-body-tertiary">
              <section class="container p-4 pb-0 mb-4" >
                <a class="btn" href="#!"><i class="bi bi-whatsapp"></i></a>
                <a class="btn" href="#!"><i class="bi bi-instagram"></i></a>
                <a class="btn" href="#!"><i class="bi bi-twitter"></i></a>
              </section>
              <div class="p-3">
                  2023 <i class="bi bi-c-circle"></i> Projeto fictício sem fins comerciais - Atividades de aprendizagem.
              </div>
          </footer>
      
          
  </main>


  <!-- Modal 1 -->
  <!-- classes mx-auto: centraliza botão, -->

  <div class="modal fade" id="modal-1" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h2 class="modal-title fs-5 fw-bold" id="exampleModalLabel">Cafés tradicionais</h2>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <img src="produtos-cafe-tradicional.png" class="w-100" alt="Xícara de café preto">
          <p>O café Serenatto é conhecido por seus blends tradicionais e saborosos, que agradam aos amantes da bebida. Nossos grãos são cuidadosamente selecionados e torrados para produzir um aroma rico e sabor equilibrado.</p>
          <p>Entre os cafés mais tradicionais da casa, destaca-se o "Café Serenatto", um blend exclusivo de grãos com notas de chocolate e caramelo. Outra opção popular é o "Café Italiano", um café expresso encorpado e intenso. Já o "Café Cappuccino" é uma escolha clássica para quem prefere uma bebida cremosa e suave.</p>
        </div>
        <div class="modal-footer mx-auto">
          <button type="button" class="btn btn-primary botao-padrao border-0" data-bs-dismiss="modal">Fechar janela</button>
        </div>
      </div>
    </div>
  </div>
        




          <!-- link bootstramp jscript -->

          <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"
            integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL"
            crossorigin="anonymous"></script>
</body>

</html>
