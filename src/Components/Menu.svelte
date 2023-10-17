<script>
  import filminLogo from '/Users/corac/Documents/factoriaf5/p11frontend/projects/p11-project4/src/assets/Logo.svg'
</script>

<header>
    <div id="menu">
        <img src={filminLogo} class="logo" alt="Logo de Filmin" />
        <nav>
            <a href="/">Inicio</a>
            <a href="/">Películas</a>
            <a href="/">Series</a>
            <a href="/">Colecciones</a>
            <a href="/">Festivales</a>
            <a href="/">Más</a>
        </nav>
    </div>
    <div id=buttons>
        <button id="buttonSub">SUSCRÍBETE</button>
        <button id="buttonIniciar">INICIAR SESIÓN</button>
    </div>
</header>


<style>
    header{
        display: flex;
        justify-content: space-between;
    }

    #menu{
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

   #buttons{
    display: flex;
    justify-content: flex-end;
    }

   button{
        font-family: Arial, Helvetica, sans-serif;
        font-weight: 900;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        margin: 20px;
        padding: 10px;
    }

    #buttonSub{
        background-color: #01FFA7;
        color: #060613;
        
    }

    #buttonIniciar{
        background-color: transparent;
        border: white 2px solid;
        color: white;
        
    }
</style>