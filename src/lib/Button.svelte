<script>
    export let url = "#";
    export let text = "Button";
    export let style = 'primary';
</script>

<a href="{url}" target="_blank" class="{style}">
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
    background-color: #aaeaaa;
    color: #262620;
}
a > div {
  color: #262620;
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