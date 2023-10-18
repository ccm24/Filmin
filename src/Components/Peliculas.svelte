<script>
  const url = 'https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=es-ES&page=1&sort_by=popularity.desc'
  const options = {
    method: 'GET',
    headers: {
      accept: 'application/json',
      Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiIzYWVjMTgxNjQ4ZDdlOTA1ZDRlZDZhZjJjNGYzOTAzMiIsInN1YiI6IjY1MmY4ZTFjY2FlZjJkMDBjNTI3Y2RlZiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.hoQnWe4EuKjY8slcLFBdkg6Z9iVALUUSU25T-TDkTBo'
    }
  };

  let movies =[];

  fetch(url, options)
    .then(response => response.json())
    .then(data => movies = data.results)
    .catch(err => console.error(err));
</script>

<div>
  {#each movies as movie}
    <img alt="Cover image" src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`} />
    <img alt="Cover image" src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`} />
    <img alt="Cover image" src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`} />
  {/each}
</div>


<style>
  div{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
  }

  img{
    width: 221.333px;
    height: 332px;
    margin-top: 2rem;
  }
</style>