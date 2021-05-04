<script>
  export let aboutData = {};
  const { heading, image, description_list } = aboutData;
</script>

<div id="about-us" class="">
  <div class="container">
    <h3 class="title">{heading}</h3>
    <div class="about-container">
      <div class="about-image">
        <img src={image} alt="" class="image"/>
      </div>
      <div class="about-content">
        <ul>
          {#each description_list as item}
            <li>{item}</li>
          {/each}
        </ul>
      </div>
    </div>
  </div>
</div>

<style>
  #about-us {
    background: var(--bglight);
    padding: 40px 0;
  }

  .title {
    text-align: center;
    font-size: 24px;
  }

  .about-container {
    display: flex;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
  }

  .about-image {
    flex: 2;
  }

  .image {
    width: 90%;
  }

  .about-content {
    flex: 3;
  }
</style>
