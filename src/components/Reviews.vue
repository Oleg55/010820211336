<template>
    <section class="reviews">
        <div class="container">
            <div class="reviews__information-block">
                <div class="reviews__filter">
                    <div class="reviews__filter-item reviews__last reviews__last--active">
                        Последние отзывы
                    </div>
                    <div class="reviews__filter-item reviews__all">
                        Все отзывы
                    </div>
                </div>
                <div class="reviews__total">
                    <div class="reviews__total-likes">
                        <img class="likes__img" src="@/assets/images/like.svg" alt="">
                        <div class="likes__count">131</div>
                    </div>
                    <div class="reviews__total-reviews">
                        <img class="reviews__img" src="@/assets/images/comment.svg" alt="">
                        <div class="total-reviews__count">14</div>
                    </div>
                </div>
            </div>
            <div class="reviews__items-block">
                <transition-group name="list">
                    <div class="review-item" v-for="wallPost in wallPosts" :key="wallPost.id">
                        <div class="review__top">
                            <div class="review__name">
                                {{wallPost.name}}
                            </div>
                            <div class="review__date">{{wallPost.date}}</div>
                        </div>
                        <div class="review__main">
                            <p class="review__main-text">
                                {{ wallPost.text }}
                            </p>
                        </div>
                    </div>
                </transition-group>
                <div class="review-item">
                    <div class="review__top">
                        <div class="review__name">Самуил</div>
                        <div class="review__date">13 октября 2011</div>
                    </div>
                    <div class="review__main">
                        <p class="review__main-text">Привет, Верунь! ниче себе ты крутая. фотка класс!!!!</p>
                    </div>
                </div>
                <div class="review-item">
                    <div class="review__top">
                        <div class="review__name">Лилия Семёновна</div>
                        <div class="review__date">14 октября 2011</div>
                    </div>
                    <div class="review__main">
                        <p class="review__main-text">Вероника, здравствуйте! Есть такой вопрос: Особый вид куниц жизненно стабилизирует кинетический момент, это и есть всемирно известный центр огранки алмазов и торговли бриллиантами?</p>
                    </div>
                </div>
                <div class="review-item">
                    <div class="review__top">
                        <div class="review__name">Лилия Семёновна</div>
                        <div class="review__date">14 октября 2011</div>
                    </div>
                    <div class="review__main">
                        <p class="review__main-text">Вероника, здравствуйте! Есть такой вопрос: Особый вид куниц жизненно стабилизирует кинетический момент?</p>
                    </div>
                </div>
            </div>
            <form class="reviews__write" @submit.prevent="addWallPost" @keyup.ctrl.enter.exact="addWallPost">
                <textarea class="reviews__write-textarea" v-model="wallPost.text"></textarea>
                <button class="reviews__write-button" type="submit">
                    Написать консультанту
                </button>
            </form>
        </div>
    </section>
</template>
<script>
    export default {
        
        data: () => ({
            wallRows: 1,
            wallCount: 0,
            wallPosts: [],
            wallPost: {
                text: '',
                name: 'Гость',
                date: '',
            },
            options: { 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            }
        }),
        methods: {
            addWallPost() {
                if(this.wallPost.text.trim()) {
                    this.wallCount++
                    this.wallPosts.unshift({
                        id: this.wallCount,
                        text: this.wallPost.text,
                        name: this.wallPost.name,
                        date: this.wallPost.date = new Date().toLocaleDateString("ru-RU", this.options).replace(/\s*г\./, "")
                    })
                    text: this.wallPost.text = ''
                    date: this.wallPost.date = ''
                }
            },
        }
    }
</script>
<style lang="scss">

    .list-item {
        display: inline-block;
        margin-right: 10px;
    }
    .list-enter-active,
    .list-leave-active {
        transition: all 1s ease;
    }
    .list-enter-from,
    .list-leave-to {
        opacity: 0;
        transform: translateY(30px);
    }

</style>