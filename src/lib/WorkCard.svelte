<script>
    import Button from "$lib/Button.svelte";


    export let title = "My Project";
    export let imgUrl = "./";
    export let projectUrl = "/";
    export let tags = ["UXDesign"];
    
</script>

<div class="container">
    <picture>
        <!-- <source srcset="{imgUrl}"> -->
        <img src="/images/Alexa_2.jpg" alt="test">
    </picture>
    <h2>{title}</h2>
    <div class="description">
    <p>this is a study in which</p>
    <p>I did lots of cool stuff.</p>
    <p>Most of it was fun. Some wasn't.</p>
    <p>Let me tell you that story.</p>
    </div>
    <div class="hashtags">
        {#each tags as tag}
        <div>#{tag}</div>            
        {/each}
    </div>
    <Button text="Learn more" url="{projectUrl}" />
</div>

<style>
    div.container {
        border-radius: 7px;
        background-color: var(--fg-color);
        color: var(--bg-color);
    }
    img {
        max-width: 256px;
    }
</style>