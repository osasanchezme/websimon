<script>
  export let navlists = [];
  export let header = {};
</script>

<div class="navbar-container" id="navbar">
  <div class="navbar">
    <a href="/" class="logo-container">
      <img class="logo-icon" src={header.logo} alt="" />
      <span class="logo-text">{header.name}</span>
    </a>
    <ul class="nav-list">
      {#each navlists as list}
        <li><a class="nav-link" href={list.url}>{list.label}</a></li>
      {/each}
    </ul>
  </div>
</div>

<style>
  .navbar-container {
    width: 100%;
    height: 40px;
    background: var(--bgdark);
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    z-index: 10;
  }

  .navbar {
    width: 90%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo-container {
    display: flex;
    align-items: center;
    text-decoration: none;
  }

  .logo-icon {
    height: 2rem;
    margin-right: 0.7rem;
  }

  .logo-text {
    color: var(--ondark);
    font-size: 1.5rem;
    font-weight: 700;
  }

  .nav-list {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    list-style: none;
  }

  .nav-link {
    color: var(--ondark);
    text-decoration: none;
    text-transform: uppercase;
    font-size: 0.7rem;
    font-weight: 700;
    padding: 0 1rem;
  }
</style>
