<script>
	import Logo from './Logo.svelte';
    import Avatar from './Avatar.svelte';
    import Seatch from './Seatch.svelte';
</script>

<header>
    <Logo />
    <nav>
        <a href="/">Inicio</a>
        <a href="/">Películas</a>
        <a href="/">Series</a>
        <a href="/">Colecciones</a>
        <a href="/">Festivales</a>
        <a href="/">Más</a>
    </nav>
    <div id=buttons>
        <button id="buttonSub">SUSCRÍBETE</button>
        <Avatar />
        <Seatch />
    </div>
</header>


<style>
    header{
        background-color: #060613;
        display: flex;
        justify-content:flex-start;
        align-items: center;
        position: sticky;
        z-index: 1;
        top: 0rem;
        padding: 1rem;
        margin: 1rem 0;
    }

    nav{
        margin-left: 1rem;
    }

    a{
        color: white;
        font-weight: bold;
        font-size: 1rem;
        text-decoration: none;
        margin-right: 1rem;
        margin-left: 1rem;       
    }

    a:hover{
        color: #01FFA7;
    }

   #buttons{
        display: flex;
        align-items: center;
        margin-left: auto;
    }

   button{
        background-color: #01FFA7;
        font-family: 'Graphik';
        font-size: .875rem;
        color: #060613;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        height: 2rem;
        min-width: 2rem;
        margin-right: 1rem;
        padding: 0rem 0.5rem;
    }

    button:hover{
        background-color: #5CFABF;
    }
</style>