<script>
    import bookCover from "$assets/book_cover.png";
    import phoneCover from "$assets/phone_cover.png";
    let {children} = $props()
    
</script>

<section class="hero">
    <div class='text-center hero-showcase bold'>
        <h1 class="purple">MOVE TO</h1>
        <h1 class="purple mb-xs">PARIS</h1>
        <h4 class="italic semi-bold">There's no need to make the same mistakes I made.</h4>
        <img class="book-cover" src={bookCover} alt="">
        <img class="phone-cover" src={phoneCover} alt="">
    </div>
    <div class="hero-text white text-center">
        {@render children()}
    </div>
</section>
<style>
    .hero {
        display: flex;
        height: 100vh;
        overflow-y: hidden;
    }
    .hero-showcase {
        position: relative;
        width: 50%;
        padding: 100px 16px 0 16px;
        background: linear-gradient(
            135deg,
            #e2cbff,
            #e2cbff 25%,
            #ece5ff 75%,
            #deeaff 50%,
            #927bce
        );   
    }
    .hero-text {
        position: relative;
        width: 50%;
        padding: 100px 5%;
        background-color: black;
    }
    .book-cover {
        position: absolute;
        right: 2%;
        width: 65%;
        bottom: 0;
        transform: translateY(35%);
    }
    .phone-cover {
        position: absolute;
        right: 52%;
        width: 35%;
        bottom: 0;
        transform: translateY(30%)
    }
</style>