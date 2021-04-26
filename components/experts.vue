<template>
    <div class="experts" id="Experts">
        <div style="position: absolute; left: 50%; top: 50%;">
            <Trigger @triggerShow="$emit('show')"/>
        </div>
        <img src="~assets/expert.png" class="tank-image"/>
        <b-container class="fix-padding">
            <b-row class="experts-title-center"><h1 class="experts-title">Эксперты</h1></b-row> 
            <b-row>
                <b-col sm=12 md=6>
                    <Card 
                        name="Александр ЗАЛЕССКИЙ" 
                        text="преподаватель факультета «Геймдизайн» образовательного портала «GeekBrains»"
                        image="Залесский"/>
                </b-col>
                <b-col sm=12 md=6>
                    <Card 
                        name="Роман МУРАТОВ" 
                        text="преподаватель факультета «Разработка игр» образовательного портала «GeekBrains»"
                        image="Муратов"/>
                </b-col>
            </b-row>
            <b-row>
                <b-col sm=12 md=6>
                    <Card 
                        name="Роман ГОРОШКИН" 
                        text="Менеджер по развитию бизнеса MGVC"
                        image="Горошкин"/>
                </b-col>
                <b-col sm=12 md=6>
                    <Card 
                        name="Владимир АЛЯМКИН" 
                        text="Tech Lead, Pushkin Studio (MY.GAMES)"
                        image="Алямкин"/>
                </b-col>
            </b-row>
            <b-row>
                <b-col sm=12 md=6>
                    <Card 
                        name="Евгений ВЫБОРНЫЙ" 
                        text="Академический руководитель образовательной программы «Математические методы моделирования и компьютерные технологии», МИЭМ НИУ ВШЭ"
                        image="Выборный"/>
                </b-col>
                <b-col sm=12 md=6>
                    <Card 
                        name="Илья СЕМИЧАСНОВ" 
                        text="эксперт АНО «ИЦТО»"
                        image="Семичаснов"/>
                </b-col>
            </b-row>
        </b-container>
    </div>  
</template>

<style>
.experts {
    width: 100vw;
    padding: 60px 30px 60px 30px;
    position: relative;
    background: url('~assets/background.png') center center/100% 100%;
}
.experts-title {
    font-family: 'Montserrat-Bold';
    color: #fff;
}
.tank-image{
    width: 25%;
    position: absolute;
    top: 25%;
}
@media only screen and (max-width: 770px) {
    .tank-image {
        width: 100%;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        opacity: 0.16;
    }
    .experts-title {
        font-size: 26px;
    }
    .experts-title-center {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }
}
@media only screen and (min-device-width: 770px) {
    .experts {
        background: url('~assets/background.png') center/100% 100%;
    }
    .fix-padding {
        padding: 0 0 0 40px;
    }
}
</style>