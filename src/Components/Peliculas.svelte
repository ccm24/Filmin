<script>
    import { onMount } from "svelte";
    import Derecha from '../assets/Derecha.svg'
    import Izquierda from '../assets/Izquierda.svg'


  export let url; 
  const options = {
    method: 'GET',
    headers: {
      accept: 'application/json',
      Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiIzYWVjMTgxNjQ4ZDdlOTA1ZDRlZDZhZjJjNGYzOTAzMiIsInN1YiI6IjY1MmY4ZTFjY2FlZjJkMDBjNTI3Y2RlZiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.hoQnWe4EuKjY8slcLFBdkg6Z9iVALUUSU25T-TDkTBo'
    }
  };

  let movies =[];

  onMount ( () => {
    fetch(url, options)
      .then(response => response.json())
      .then(data => movies = data.results)
      .catch(err => console.error(err));
  });
  
  const rotateLeft = e => {
        const transitioningImage = movies[movies.length -1]
        movies = [movies[movies.length -1],...movies.slice(0, movies.length -1)]
        
    }
    const rotateRight = e => {
        const transitioningImage = movies[0]
        movies = [...movies.slice(1, movies.length), movies[0]]
      
    }
</script>

<div>
  {#each movies as {poster_path}}
    <img id="cover" alt="Cover image" src={`https://image.tmdb.org/t/p/original/${poster_path}`} />
  {/each}
  <button id="left" on:click={rotateLeft}>
    <slot name="=leftControl">
        <img src={Izquierda}>
    </slot>
  </button>
  <button id="right" on:click={rotateRight}>
    <slot name="=leftControl">
        <img src={Derecha}>
    </slot>
  </button>
</div>


<style>
  div{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: nowrap;
    overflow-x: scroll;
    margin: 0rem 4rem;
    padding-left: 15rem;
    max-width: 90%;
  }

  div::-webkit-scrollbar{
    display: none;
  }

  #cover{
    width: 221.333px;
    height: 332px;
    margin: 2rem 1rem;
    border-radius: 5px;
  }

  button{
        position: absolute;
        display: flex;
        align-items: center;
        justify-content: center;
        background: transparent;
        border: none;
        width: 1rem;
        margin-top: 10rem;
        
    }

    #left{
        left: 10px;
    }

    #right{
        right: 10px;
    }
</style>