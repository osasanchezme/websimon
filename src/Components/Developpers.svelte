<script>
  export let developpersData = {};
  const { heading, developpers_list } = developpersData;
</script>

<div id="developpers" class="">
  <div class="container">
    <h2 class="title">{heading}</h2>
    <div class="all-talks">
      {#each developpers_list as devel}
        <div class="talk-card">
          <div class="card-img">
            <img src={devel.img} alt={devel.label} class="img" />
          </div>
          <div class="card-body">
            <h4 class="card-title">{devel.label}</h4>
            <div class="card-text">
              <p>{devel.description}</p>
            </div>
          </div>
          <div class="card-links">
            <a href={devel.youtube_url} class="fab fa-youtube"> </a>
            <a href={devel.github_url} class="fab fa-github"> </a>
          </div>
        </div>
      {/each}
    </div>
  </div>
</div>

<style>
  #developpers {
    background: var(--bgdark);
    color: var(--ondark);
    padding: 40px 0;
  }

  .title {
    font-size: 24px;
    padding: 10px 0 30px 0;
  }

  .all-talks {
    display: flex;
    column-gap: 20px;
    row-gap: 20px;
    flex-direction: column;
  }

  .talk-card {
    border-radius: 5px;
    background: #222;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    width: 100%;
  }

  .card-img {
    flex: 4;
    margin-right: 10px;
  }

  .img {
    max-width: 100%;
    min-width: 300px;
    object-fit: scale-down;
  }

  .card-body {
    flex: 7;
  }

  .card-title {
    font-size: 24px;
    margin-bottom: 10px;
  }

  .card-links {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  a {
    font-size: 24px;
    margin: 10px;
    text-decoration: none;
    color: var(--ondark);
  }

  a:hover {
    opacity: 0.7;
  }
</style>
