<template>
    <div>
        <Header />
        <Nuxt />
        <Footer />
        <PhotoSwipeBg />
        <Preloader v-if="true === false" />
    </div>
</template>

<script>
export default {
    methods: {
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
        this.clSmoothScroll();
    },
}
</script>