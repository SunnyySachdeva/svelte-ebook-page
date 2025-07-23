<script lang="ts">
    import {First, HeroSection, FaqSection, ChapterPreviews, AboutAuthor} from "$components";
    
    let name = $state("");
    let derivedName = $derived(name);

    let buttonClicked = $state(false);
    function onclick() {
        if (buttonClicked) {
            buttonClicked = false;
        } else {
            buttonClicked = true;
        }
    }
</script>


<HeroSection />
<ChapterPreviews />
<AboutAuthor />
<FaqSection />

<!-- 
<h1>Welcome {name}</h1>
<input type="text" bind:value={name}>

<First userName={name}>
    <p>Well done, you got the name</p>
</First>
<button {onclick}>{buttonClicked? "Clicked": "click me"}</button>
 -->

<style>
    button {
        background-color: red;
        border: 1px solid black;
        border-radius: 10px;
        color: white
    }
</style>