<script>
  import filminLogo from '../assets/Logo.svg'
  import avatar from '../assets/Avatar.png'
  import search from '../assets/Search.png'
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
        <img src={avatar} class="avatar" alt="Avatar" />
        <img src={search} class="search" alt="Buscador web" />
    </div>
</header>


<style>
    header{
        display: flex;
        justify-content: space-around;
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
        align-items: center;
    }

   button{
        background-color: #01FFA7;
        font-family: Arial, Helvetica, sans-serif;
        font-size: .875rem;
        font-weight: 900;
        color: #060613;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        padding: 0.75rem;  
        height: 2rem;
        min-width: 2rem;
        margin-right: 1rem;
       }

   .avatar{
        cursor: pointer;
        height: 2rem;
        width: 2rem;
    }

    .search{
        cursor: pointer;
        width: auto;
        height: 1.5rem;
        margin-left: 1rem;
    }

</style>