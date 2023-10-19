<script>
    import Redes from './Redes.svelte';
    import Sponsors from './Sponsors.svelte';

    

</script>


<footer>
    <hr/>
    <div>
        <p>Centro de Ayuda</p>
        <p>Contacto</p>
        <p>Canjear código</p>
        <p>Regala Filmin</p>
        <p>Aviso Legal</p>
        <p>Prensa</p>   
        <Redes />
    </div>
    <hr>   
    <Sponsors />
</footer>

<style>
    footer{
        margin-top: 4rem;
    }

    hr{
        border: #93959C solid 0.05rem;
        margin-top: 1rem;
    }

    div{
        display: flex;
        align-items: center;
        color: #93959C;
        cursor: pointer;
        gap: 1rem;
        margin: 1rem 4rem;
    }

    p:hover{
        color: #D1DBE3;
    }  
</style>