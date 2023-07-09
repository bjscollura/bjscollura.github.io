<script>
    import { browser } from "$app/environment";
    import { page } from "$app/stores";
    // export const prerender = true;
    import Button from "$lib/Button.svelte";
    
    let lastScrollPosition = 0;
    let isHeaderHover = true;
    
    if (browser) {
      document.addEventListener("scroll", () => {
        isHeaderHover = (lastScrollPosition < window.scrollY) ? false : true;
        lastScrollPosition = window.scrollY;  
      });
    }
</script>

<div class="header-container {isHeaderHover ? 'headerHover' : 'headerFade'}">
    <header>
        <div class="logo"><a href="/" style="color:#e4ebe4;">Brian Collura</a></div>
        <ul class="header-nav">
          <li><a href="/" class:nav-here={$page.route.id === '/'}>Work</a></li>
          <li><a href="/about" class:nav-here={$page.route.id === '/about'}>About</a></li>
        </ul>
        <ul class="header-links">
          <li><a href="http://linkedin.com/in/bjscollura" class="icon-link" target="_blank">
              <i class="fab fa-linkedin-in fa-lg"></i></a>
          </li>
          <li><a href="https://github.com/bjscollura/" class="icon-link" target="_blank">
              <i class="fab fa-github fa-lg"></i></a>
          </li>
          <li>
            <Button url="/Resume_June2023.pdf" text="Resume.pdf" />
              <!-- <a href="/Resume_June2023.pdf" target="_blank" class="button">
              <div>Resume.pdf</div></a> -->
          </li>
        </ul>
    </header>
</div>

<style>
  /* Header */
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    max-width: 1899px;
    height: 80px;
  }
  .header-container {
    display: flex;
    justify-content: center;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 2;
    overflow: hidden;
    padding: 20px 50px;
    background-color: var(--bg-color);
    box-shadow: 0 0 0 black;
    transition: box-shadow .5s ease-in;
  }
  .headerHover {
    box-shadow: 1px 1px .5em black;
    position: fixed;
    opacity: 1;
    transform: scaleY(1);
    transition: opacity 0.3s cubic-bezier(0.55, 0.085, 0.68, 0.53);
  }
  .headerFade {
      position: fixed;
      opacity: 0;
      padding: 0;
      transform: scaleY(0);
      transition: opacity 0.3s cubic-bezier(0.165, 0.84, 0.44, 1),
                transform 0.5s linear 0.4s,
                padding 0.5s linear 0.4s;            
  }
  .header-nav {
    display: flex;
    justify-content: center;
    width: 33.3%;
    list-style: none;
  }
  .header-nav > li {
    margin-right: 2rem;
  }
  .header-nav > li:last-of-type {
    margin-right: 0;
  }
  .header-nav a {
    color: #e4ebe4;
    font-size: 1.1rem;
    padding: 10px 0;
  }
  .nav-here {
    border-bottom: 2px solid #e4ebe4;
  }
  .header-links {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    width: 33.3%;
    list-style: none;
  }
  .header-links > li {
    margin-right: 1rem;
  }
  .header-links > li:last-of-type {
    margin-right: 0;
  }
  .header-links a {
    padding: 10px;
  }
  @media only screen and (max-width: 767px) {
    header {
      flex-direction: column;
      height: auto;
    }
    .logo {
      width: 90%;
      text-align: center;
      margin: .5rem auto .0 auto;
    }
    .header-nav {
      width: 90%;
      margin: .7rem auto;
    }
    .header-links {
      justify-content: center;
      align-items: center;
      width: 90%;
      margin: 1rem auto 0 auto;
    }
  }
</style>