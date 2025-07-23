<script>
    import ProfilePic from "$assets/profile_pic.jpg";
</script>

<section class="about-section">
    <div class="wrapper">
    <h2 class=" mb-l">About the author</h2>
    <div class="about-author">
        <div class="author-text">
        <p class="mb-xs">
            Niklas Fischer is a seasoned expatriate with over seven years of
            experience living in Spain. Originally from New York, John left behind
            the hustle of corporate America to embrace a more fulfilling life on the
            sun-soaked coasts of Spain. Through his own journey, he has navigated
            the challenges of securing visas, finding the perfect home, and adapting
            to a new culture, making him an expert in the field of relocation.
            </p>
            <p>
            Niklas’ practical advice is rooted in real-life experience, having
            learned firsthand the intricacies of moving to a new country. His goal
            is to help others avoid common pitfalls and make their transition to
            life in Spain as smooth as possible. When not sharing his expertise,
            John enjoys exploring Spain’s rich culture and history, fully embracing
            the lifestyle he once dreamed of.
        </p>
        </div>
        <img class="image" src={ProfilePic} alt="Author profile pic">

    </div>
    </div>
</section>

<style>
    .about-section {
        background-color: rgb(230, 213, 255);
    }
    .wrapper {
        margin: 100px 15%;
        padding: 50px 0;
    }
    .about-author {
        display: flex;
        max-width: 1200px;
        justify-content: space-between;
    }
    .image {
        width: 370px;
        margin-left: 250px;
        border: 4px solid black;
    }

</style>