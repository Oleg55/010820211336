<template>
    <div>
        <div class="site-wrapper container">
                <app-header>
                            
                </app-header>

                <app-reviews>

                </app-reviews>
        </div>
    </div>
</template>
<script>
import AppHeader from '@/components/Header.vue'
import AppReviews from '@/components/Reviews.vue'




    export default {
        components: {
            AppHeader,
            AppReviews,
        },
        data: () => ({

        }),
        methods: {

        }
    }
</script>
<style lang="scss">

</style>