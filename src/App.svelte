<script>
  import Nav from './components/Nav.svelte'
  let name = "Maïli-Anna";
  let likes = 0
  let a = 1;
  let b = 2;
  $: doubledLiked = likes * 2

  function btnLikesHandler () {
    likes++
  }
</script>

<main>
  <h1>Hello {name.toUpperCase()}!</h1>
  <input type="text" bind:value={name}>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
  <Nav/>
  <button on:click={btnLikesHandler}>Liked {likes} {likes < 2 ? 'Time' : 'Times'}</button>
  <p>Likes * 2 is {doubledLiked}</p>

  <input type="range" bind:value={a} min=0 max=10>
  <input type="range" bind:value={b} min=0 max=10>

  <p>{a} + {b} = {a + b}</p>
</main>

<style lang="scss">
  $main-color: rgb(221, 63, 0);
  
  main {
    text-align: center;
    max-width: 800px;
    margin: 0 auto;

    h1 {
      color: blue;
      text-transform: uppercase;
      font-size: 4em;
      font-weight: 100;
    }

    p {
      color: rgb(51, 51, 51);
    }
  }

  @media (min-width: 1000px) {
    main {
      max-width: none;

      h1 {
        color: $main-color;
      }
    }
  }
</style>
