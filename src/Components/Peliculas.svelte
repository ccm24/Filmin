<script>
    import { onMount } from "svelte";

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
  
</script>

<div>
  {#each movies as {poster_path}}
    <img alt="Cover image" src={`https://image.tmdb.org/t/p/original/${poster_path}`} />
  {/each}
</div>


<style>
  div{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: nowrap;
    overflow: scroll;
    margin: 0rem 4rem;
  }

  img{
    width: 221.333px;
    height: 332px;
    margin: 2rem 1rem;
  }
</style>