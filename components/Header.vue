<template>
    <!-- header
    ================================================== -->
    <header class="s-header">

        <div class="header-logo">
            <nuxt-link class="site-logo" to="">
                <img src="images/logo_new_crop.png" alt="Homepage">
                <!-- Cogenie logo -->
            </nuxt-link>
        </div>

        <nav class="header-nav">

            <nuxt-link to="#home" class="header-nav__close" title="close">
                <span>Close</span>
            </nuxt-link>

            <div class="header-nav__content">
                <h3>Navigation</h3>
                
                <ul class="header-nav__list">
                    <li class="current">
                        <nuxt-link class="smoothscroll" to="#home" title="Home">Home</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="smoothscroll" to="#about" title="About">About</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="smoothscroll"  to="#services" title="services">Services</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="smoothscroll"  to="#works" title="works">Works</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="smoothscroll"  to="#clients" title="clients">Clients</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="smoothscroll"  to="#contact" title="contact">Contact</nuxt-link>
                    </li>
                </ul>
    
                <p>
                    When you hear 
                    <i>
                        <nuxt-link to="#home">Zaaazuuu</nuxt-link>
                    </i>;
                    <br />
                    You say 
                    <i>
                        <nuxt-link to='#home'>zeeh</nuxt-link>
                    </i>!!!
                    <br />
                    That's how we rolllll
                </p>
    
                <ul class="header-nav__social">
                    <li>
                        <a href="#"><i class="fa fa-facebook"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fa fa-twitter"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fa fa-instagram"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fa fa-behance"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fa fa-dribbble"></i></a>
                    </li>
                </ul>

            </div> <!-- end header-nav__content -->

        </nav>  <!-- end header-nav -->

        <a class="header-menu-toggle" href="#0">
            <span class="header-menu-text">Menu</span>
            <span class="header-menu-icon"></span>
        </a>

    </header> <!-- end s-header -->
</template>

<script>
export default {
    methods: {
        clMenuOnScrolldown () {
            const menuTrigger = $('.header-menu-toggle');

            $(window).on('scroll', function() {

                if ($(window).scrollTop() > 150) {
                    menuTrigger.addClass('opaque');
                }
                else {
                    menuTrigger.removeClass('opaque');
                }

            });
        }, // end

        clOffCanvas () {
            const menuTrigger     = $('.header-menu-toggle'),
                nav             = $('.header-nav'),
                closeButton     = nav.find('.header-nav__close'),
                siteBody        = $('body'),
                mainContents    = $('section, footer');

            // open-close menu by clicking on the menu icon
            menuTrigger.on('click', function(e){
                e.preventDefault();
                // menuTrigger.toggleClass('is-clicked');
                siteBody.toggleClass('menu-is-open');
            });

            // close menu by clicking the close button
            closeButton.on('click', function(e){
                e.preventDefault();
                menuTrigger.trigger('click');	
            });

            // close menu clicking outside the menu itself
            siteBody.on('click', function(e){
                if( !$(e.target).is('.header-nav, .header-nav__content, .header-menu-toggle, .header-menu-toggle span') ) {
                    // menuTrigger.removeClass('is-clicked');
                    siteBody.removeClass('menu-is-open');
                }
            });
        }, // end

        clSmoothScroll () {
            $('.smoothscroll').on('click', function (e) {
                const target = this.hash,
                $target    = $(target);
                
                    e.preventDefault();
                    e.stopPropagation();

                $('html, body').stop().animate({
                    'scrollTop': $target.offset().top
                }, 800, 'swing').promise().done(function () {

                    // check if menu is open
                    if ($('body').hasClass('menu-is-open')) {
                        $('.header-menu-toggle').trigger('click');
                    }

                    window.location.hash = target;
                });
            });
        }, //end
    },

    mounted() {
        this.clMenuOnScrolldown();
        this.clOffCanvas();
        this.clSmoothScroll();
    },
}
</script>