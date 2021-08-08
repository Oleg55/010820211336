<template>
    <header class="header">
        <div class="container">
            <div class="header__block">
                <div class="logo">
                    <a class="logo__link" href="#">
                        <img class="logo__img" src="@/assets/images/avatar.svg" alt="" width="124" height="124">
                    </a>
                </div>
                <div class="information">
                    <div class="information__name">
                        Вероника Ростова
                    </div>
                    <div class="information__position">
                        Менеджер по продажам
                    </div>
                    <div class="information__status">
                       <p>Подберу для вас самые лучшие предложения.
                        Мои услуги абсолютно бесплатны</p>
                    </div>
                    <div class="services">
                        <div class="services__block">
                            <div class="services__title">Услуг</div>
                            <div class="services__content">
                                <div class="services__content-line">
                                    <div class="services__content-item">
                                        <div class="services__progress-line">
                                            <div class="progress-line__text">
                                                <div class="progress-line__color-line progress-line__text--done" style="width: 93%;"></div>
                                                <div class="progress-line__text-item">Ручное бронирование</div>
                                            </div>
                                            <div class="progress-line__count">
                                                11
                                            </div>
                                        </div>
                                    </div>
                                    <div class="services__content-item">
                                        <div class="services__progress-line">
                                            <div class="progress-line__text">
                                                <div class="progress-line__color-line progress-line__text--progress" style="width: 23%;"></div>
                                                <div class="progress-line__text-item">Пакетные туры</div>
                                            </div>
                                            <div class="progress-line__count">
                                                3
                                            </div>
                                        </div>
                                    </div>
                                    <div class="services__content-item">
                                        <div class="services__progress-line">
                                            <div class="progress-line__text">
                                                <div class="progress-line__color-line progress-line__text--progress" style="width: 15%;"></div>
                                                <div class="progress-line__text-item">Отели</div>
                                            </div>
                                            <div class="progress-line__count">
                                                1
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="services__total">
                                <div class="total__text">
                                    Всего
                                </div>
                                <div class="total__count">
                                    15
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<script>
    export default {
        methods: {

        }
    }
</script>