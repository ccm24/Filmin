<script>
	import Carousel from './Components/Carousel.svelte';
  import Header from "./Components/Header.svelte";
  import Footer from "./Components/Footer.svelte";
  import Listas from "./Components/Listas.svelte";


  const images = [
    {path: `images/image1.jpg`, id: `image1`},
    {path: `images/image2.jpg`, id: `image2`},
    {path: `images/image3.jpg`, id: `image3`},
    {path: `images/image4.jpg`, id: `image4`},
  ]
</script>

<Header />

<Carousel {images} />


<Listas />
<Footer />



