<script>
  export let networkData = {};
  const { heading, network_list } = networkData;
</script>

 <div id="network" class="">
  <div class="container">
    <h2 class="title text-center">{heading}</h2>
    <div class="all-network">
      {#each network_list as item}
        <div class="network-card">
          <img src={item.img} alt={item.name} />
          <h3>{item.name}</h3>
          <b>{item.institution}</b>
          <a href={item.url}>{item.url}</a>
        </div>
      {/each}
    </div>
  </div>
</div>

<style>
  #network {
    background: var(--bglight);
    background-image: url(/images/bg-img.svg);
    color: var(--onlight);
    padding: 40px 0;
  }

  .title {
    text-align: center;
    text-transform: uppercase;
    font-size: 24px;
    padding: 10px 0 30px 0;
  }

  .all-network {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    column-gap: 20px;
    row-gap: 20px;
  }

  .network-card {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  h3 {
    padding: 5px 0;
  }
</style>
