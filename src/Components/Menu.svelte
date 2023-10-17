<script>
  import filminLogo from '/Users/corac/Documents/factoriaf5/p11frontend/projects/p11-project4/src/assets/Logo.svg'
</script>

<main>
    <img src={filminLogo} class="logo" alt="Logo de Filmin" />
  <nav>
    <a href="/">Inicio</a>
    <a href="/">Películas</a>
    <a href="/">Series</a>
    <a href="/">Colecciones</a>
    <a href="/">Festivales</a>
    <a href="/">Más</a>
  </nav>
</main>

<style>
    main{
        display: flex;
        align-items: center;
        justify-content: flex-start;
        margin-top: 33px;
    }
    nav{
        margin-left: 40px;
    }
    a{
        margin-right: 40px;
        text-decoration: none;
        color: white;
        size: 20px;
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
    }
</style>