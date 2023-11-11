<script>
    export let url = "#";
    export let text = "Button";
    export let style = 'primary';
    export let newTab = false;
</script>

<a href="{url}" target="{newTab ? '_blank' : '_self'}" class="{style}">
    <div>{text}</div>
</a>

<style>
a {
    display: block;
    border-radius: 7px;
    border: none;
    text-decoration: none;
    text-align: center;
    font-weight: 700;
    padding: .8rem 1.6rem;
}
.primary {
    background-color: var(--primary-color);
    color: var(--bg-color);
}
a > div {
  color: var(--bg-color);
  position: relative;
  width: 100%;
  height: 100%;
}
a:hover > div {
  animation: button .2s ease-in-out;
  animation-fill-mode: forwards;
}
@keyframes button {
  0%   { top: 0px; right: 0px; }
  100% { top: 2px; right: 1px; }
}
</style>