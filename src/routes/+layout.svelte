<script>
    import { browser } from "$app/environment";
    import { page } from "$app/stores";
    export const prerender = true;

    let isYScroll = false;
    if (browser) {
        window.onscroll = function() {
            if (window.scrollY > 20) {
                isYScroll = true;
            } else {
                isYScroll = false;
            }
        }
    }
    console.log($page)
</script>

<div class="header-container container {isYScroll ? 'header-shadow' : ''}">
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
            <a href="/Resume_June2023.pdf" target="_blank" class="button">
            <div>Resume.pdf</div></a>
        </li>
        </ul>
    </header>
</div>

<main>
    <slot />
</main>

<div class="footer-container container">
    <hr />
    <footer>
        <p>Brian Collura</p>
        <p>bjscollura@gmail.com</p>
        <p><span class="footer-links">
        <a href="http://linkedin.com/in/bjscollura" class="icon-link" target="_blank">
            <i class="fab fa-linkedin-in fa-lg"></i></a>
        <a href="https://github.com/bjscollura" class="icon-link" target="_blank">
            <i class="fab fa-github fa-lg"></i></a>
        </span></p>
        <p>Made from scratch with good ol' HTML5, CSS3, and Javascript, <br> via Github Pages.</p>
        <p>Check out my code <a href="https://github.com/bjscollura/bjscollura.github.io" target="_blank">here!</a></p>
    </footer>
</div>

<style>
    .header-container {
        justify-content: center;
        background-color: #262620;
        z-index: 2;
        width: 100%;
        position: fixed;
        top: 0;
        left: 0;
        padding: 20px 50px;
        transition: box-shadow .5s ease-in;
    }
    .header-shadow {
        box-shadow: 1px 1px .5em black;

    }
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        height: 80px;
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
/* Footer */
.footer-container {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
.footer-links a {
  margin: 0 .5rem;
  padding: 10px;
}
.footer-container p {
  text-align: center;
}
.footer-container hr {
  margin-bottom: 50px;
}
</style>
