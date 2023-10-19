<script>
	import Titulo from './Titulo.svelte';
    import Peliculas from './Peliculas.svelte';
</script>

<Titulo text="Populares" />
<Peliculas url='https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=es-ES&page=1&sort_by=popularity.desc'/>

<Titulo text="En el cine" />
<Peliculas url='https://api.themoviedb.org/3/movie/now_playing?language=es-ES&page=1'/>

<Titulo text="Las más valoradas" />
<Peliculas url='https://api.themoviedb.org/3/movie/top_rated?language=es-ES&page=1'/>

<Titulo text="Próximamente" />
<Peliculas url='https://api.themoviedb.org/3/movie/upcoming?language=en-US&page=1'/>