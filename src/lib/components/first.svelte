<script>
    let {userName, children, ...props} = $props();

</script>

<hr>
<h2>Child file contents</h2>
{@render children()}
<p>I got the name {userName}</p>

<style>
    hr {
        color: green;
        width: 1000px;
    }
    h2 {
        color: red;
    }
</style>