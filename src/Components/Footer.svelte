<script>
  export let footerData = {};
  const { logo, description, contact_details } = footerData;
</script>

<div class="" id="footer">
  <div class="container">
    <div class="footer-brand">
      <div class="logo">
        <img src={logo} alt="SIMON" class="img"/>
      </div>
      <p class="copyright">@ 2021 - SIMON - unal</p>
    </div>
    <div class="footer-contact">
      <div class="contact-link">
        <div class="link-icon">
          <a href={contact_details.email} class="fas fa-envelope"> </a>
        </div>
        <div class="link-text">
          <a href={contact_details.email}>{contact_details.email} </a>
        </div>
      </div>
      <div class="contact-link">
        <div class="link-icon">
          <a href={contact_details.youtube} class="fab fa-youtube"> </a>
        </div>
        <div class="link-text">
          <a href={contact_details.youtube}>{contact_details.youtube} </a>
        </div>
      </div>
      <div class="contact-link">
        <div class="link-icon">
          <a href={contact_details.discord} class="fab fa-discord"> </a>
        </div>
        <div class="link-text">
          <a href={contact_details.discord}>{contact_details.discord} </a>
        </div>
      </div>
      <div class="contact-link">
        <div class="link-icon">
          <a href={contact_details.github} class="fab fa-github"> </a>
        </div>
        <div class="link-text">
          <a href={contact_details.github}>{contact_details.github} </a>
        </div>
      </div>
    </div>
    <div class="footer-info">
      <p>{description}</p>
    </div>
  </div>
</div>

<style>
  #footer {
    background: var(--bgdark);
    color: var(--ondark);
    padding: 2rem 0;
  }

  .container {
    width: 90%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .footer-brand {
    flex: 1;
  }

  .copyright {
    font-size: 0.7rem;
  }

  .footer-contact {
    flex: 3;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
  }

  .contact-link {
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }

  .link-icon {
    font-size: 1.2rem;
    width: 1rem;
    margin: 0.2rem 1rem;
    display: flex;
    justify-content: center;
  }

  .link-text {
    font-size: 0.8rem;;
  }

  a {
    text-decoration: none;
    color: var(--ondark);
  }

  a:hover {
    opacity: 0.7;
  }

  .footer-info {
    flex: 2;
  }
</style>
