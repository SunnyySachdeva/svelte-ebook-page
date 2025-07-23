<script lang="ts">
    import {loadStripe} from "@stripe/stripe-js";
    import {PUBLIC_STRIPE_KEY} from "$env/static/public";
    import {goto} from "$app/navigation";

    let {children, ...props} = $props()

    async function onclick() {
        try {
            const stripe = await loadStripe(PUBLIC_STRIPE_KEY)

            const response = await fetch("/api/checkout", {
                method: "POST",
                headers: {
                    "Content-Type": "application/json" 
                }
            }
            )
            const {sessionId} = await response.json()
            await stripe.redirectToCheckout({sessionId})
        } catch(err) {
            console.log(err)
        }
        
    }
</script>

<button class="a" {...props} {onclick}>{@render children()}</button>

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