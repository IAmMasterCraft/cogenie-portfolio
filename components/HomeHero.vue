<template>
    <!-- home
    ================================================== -->
    <section id="home" class="s-home target-section" data-parallax="scroll" data-image-src="images/hero-bg.jpg" data-natural-width=3000 data-natural-height=2000 data-position-y=center>

        <div class="overlay"></div>
        <div class="shadow-overlay"></div>

        <div class="home-content">

            <div class="row home-content__main">

                <h3>Welcome to Cogenie</h3>

                <h1>
                    We are a creative group <br>
                    of people who <br>
                    design, develop and ship <br>
                    software solutions.
                </h1>

                <div class="home-content__buttons">
                    <nuxt-link to="contact" class="smoothscroll btn btn--stroke">
                        Start a Project
                    </nuxt-link>
                    <nuxt-link to="about" class="smoothscroll btn btn--stroke">
                        More About Us
                    </nuxt-link>
                </div>

            </div>

            <div class="home-content__scroll">
                <nuxt-link to="about" class="scroll-link smoothscroll">
                    <span>Scroll Down</span>
                </nuxt-link>
            </div>

            <div class="home-content__line"></div>

        </div> <!-- end home-content -->


        <ul class="home-social">
            <li>
                <a href=""><i class="fa fa-facebook" aria-hidden="true"></i><span>Facebook</span></a>
            </li>
            <li>
                <a href=""><i class="fa fa-twitter" aria-hidden="true"></i><span>Twiiter</span></a>
            </li>
            <li>
                <a href=""><i class="fa fa-instagram" aria-hidden="true"></i><span>Instagram</span></a>
            </li>
            <li>
                <a href=""><i class="fa fa-behance" aria-hidden="true"></i><span>Behance</span></a>
            </li>
            <li>
                <a href=""><i class="fa fa-dribbble" aria-hidden="true"></i><span>Dribbble</span></a>
            </li>
        </ul> 
        <!-- end home-social -->

    </section> <!-- end s-home -->
</template>

<script>
export default {
    data() {
        return {
            //
        }
    },
    mounted() {
        $('.target-section').parallax({imageSrc: 'images/hero-bg.jpg'});
    },
}
</script>