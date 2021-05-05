<script>
  export let bannerData = {};
  const { description, institution, image } = bannerData;
</script>

<div class="" id="banner">
  <div class="container">
    <div class="content">
      <div class="banner-text">
        <h1>{description}</h1>
        <h2>{institution}</h2>
      </div>
      <div class="banner-image">
        <img src={image} alt="" class="image" />
      </div>
    </div>
  </div>
</div>

<style>
  #banner {
    padding: 150px 0;
    background: var(--bgdark);
    color: var(--ondark);
  }

  .content {
    display: flex;
    gap: 50px;
    flex-wrap: wrap;
  }

  .banner-text {
    flex: 3;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }

  .banner-image {
    flex: 2;
    display: flex;
  }

  /* @keyframes showup { */
  /*   0% {opacity: 1;} */
  /*   50% {opacity: 0;} */
  /*   100% {opacity: 1;} */
  /* } */

  /* .image { */
  /*   opacity: 1; */
  /*   animation-name: showup; */
  /*   animation-delay: 1s; */
  /*   animation-duration: 3s; */
  /* } */

  h1 {
    font-size: 36px;
    font-weight: 300;
    padding: 20px 0;
  }

  h2 {
    font-size: 18px;
    font-weight: 700;
    text-transform: uppercase;
  }
</style>
