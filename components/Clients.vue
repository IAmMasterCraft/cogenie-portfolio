<template>
    <!-- clients
    ================================================== -->
    <section id="clients" class="s-clients">

        <div class="row section-header" data-aos="fade-up">
            <div class="col-full">
                <h3 class="subhead">Our Clients</h3>
                <h1 class="display-2">It has been an honor for COGENIE to work together with these clients</h1>
            </div>
        </div> <!-- end section-header -->

        <div class="row clients-outer" data-aos="fade-up">
            <div class="col-full">
                <div class="clients">
                    
                    <a href="" title="" class="clients__slide"><img src="images/clients/apple.png" /></a>
                    <a href="" title="" class="clients__slide"><img src="images/clients/atom.png" /></a>
                    <a href="" title="" class="clients__slide"><img src="images/clients/blackberry.png" /></a>
                    <a href="" title="" class="clients__slide"><img src="images/clients/dropbox.png" /></a>
                    <a href="" title="" class="clients__slide"><img src="images/clients/envato.png" /></a>
                    <a href="" title="" class="clients__slide"><img src="images/clients/firefox.png" /></a>
                    <a href="" title="" class="clients__slide"><img src="images/clients/joomla.png" /></a>
                    <a href="" title="" class="clients__slide"><img src="images/clients/magento.png" /></a>
                     
                </div> <!-- end clients -->
            </div> <!-- end col-full -->
        </div> <!-- end clients-outer -->

        <div class="row clients-testimonials" data-aos="fade-up">
            <div class="col-full">
                <div class="testimonials">

                    <div class="testimonials__slide">

                        <p>Qui ipsam temporibus quisquam vel. Maiores eos cumque distinctio nam accusantium ipsum. 
                        Laudantium quia consequatur molestias delectus culpa facere hic dolores aperiam. Accusantium quos qui praesentium corpori.
                        Excepturi nam cupiditate culpa doloremque deleniti repellat.</p>

                        <img src="images/avatars/user-01.jpg" alt="Author image" class="testimonials__avatar">
                        <div class="testimonials__info">
                            <span class="testimonials__name">Tim Cook</span> 
                            <span class="testimonials__pos">CEO, Apple</span>
                        </div>

                    </div>

                    <div class="testimonials__slide">
                        
                        <p>Excepturi nam cupiditate culpa doloremque deleniti repellat. Veniam quos repellat voluptas animi adipisci.
                        Nisi eaque consequatur. Quasi voluptas eius distinctio. Atque eos maxime. Qui ipsam temporibus quisquam vel.</p>

                        <img src="images/avatars/user-05.jpg" alt="Author image" class="testimonials__avatar">
                        <div class="testimonials__info">
                            <span class="testimonials__name">Sundar Pichai</span> 
                            <span class="testimonials__pos">CEO, Google</span>
                        </div>

                    </div>

                    <div class="testimonials__slide">
                        
                        <p>Repellat dignissimos libero. Qui sed at corrupti expedita voluptas odit. Nihil ea quia nesciunt. Ducimus aut sed ipsam.  
                        Autem eaque officia cum exercitationem sunt voluptatum accusamus. Quasi voluptas eius distinctio.</p>

                        <img src="images/avatars/user-02.jpg" alt="Author image" class="testimonials__avatar">
                        <div class="testimonials__info">
                            <span class="testimonials__name">Satya Nadella</span> 
                            <span class="testimonials__pos">CEO, Microsoft</span>
                        </div>

                    </div>

                </div><!-- end testimonials -->
                
            </div> <!-- end col-full -->
        </div> <!-- end client-testimonials -->

    </section> <!-- end s-clients -->
</template>

<script>
export default {
    methods: {
        clSlickSlider () {

            $('.clients').slick({
                arrows: false,
                dots: true,
                infinite: true,
                slidesToShow: 6,
                slidesToScroll: 2,
                //autoplay: true,
                pauseOnFocus: false,
                autoplaySpeed: 1000,
                responsive: [
                    {
                        breakpoint: 1200,
                        settings: {
                            slidesToShow: 5
                        }
                    },
                    {
                        breakpoint: 1000,
                        settings: {
                            slidesToShow: 4
                        }
                    },
                    {
                        breakpoint: 800,
                        settings: {
                            slidesToShow: 3,
                            slidesToScroll: 2
                        }
                    },
                    {
                        breakpoint: 500,
                        settings: {
                            slidesToShow: 2,
                            slidesToScroll: 2
                        }
                    }

                ]
            });

            $('.testimonials').slick({
                arrows: true,
                dots: false,
                infinite: true,
                slidesToShow: 1,
                slidesToScroll: 1,
                adaptiveHeight: true,
                pauseOnFocus: false,
                autoplaySpeed: 1500,
                responsive: [
                    {
                        breakpoint: 900,
                        settings: {
                            slidesToShow: 1,
                            slidesToScroll: 1
                        }
                    },
                    {
                        breakpoint: 800,
                        settings: {
                            arrows: false,
                            dots: true
                        }
                    }
                ]
            });
        
        }, // end
    },

    mounted() {
        this.clSlickSlider();
    },
}
</script>