<script>
    import {Hero,Button} from "$components";
</script>

<Hero>    
<h1>Payment Failed</h1>
<p class="light-grey mb-s">
    We’re sorry, but it looks like there was an issue with your purchase. Don’t
    worry—these things happen, and we're here to help.Please double-check your
    payment details and try again.
  </p>
  <p class="light-grey mb-s">
    We apologize for any inconvenience this may have caused and appreciate your
    patience. We’re committed to ensuring that you get the guide you need to
    make your move to Spain as smooth as possible.
  </p>
  <p class="light-grey mb-m">
    If you’d like to try again, please click the button below to return to the
    checkout page.
  </p>
<div>
<Button>Try Again</Button>
<button><a href="/">GO HOME </a></button>
</div>
</Hero>
<style>
    button {
        margin: 40px;
        background-color: black;
        border: 1px solid white;
        color: white;
        font-weight: normal;
        font-size: 22px;
        padding: 10px;
        text-transform: uppercase;
        transition: all 0.3s;
    }
    button:hover {
        color: black;
        background-color: white;
    }
</style>