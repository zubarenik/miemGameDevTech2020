<template>
    <div class="sponsors" id="Sponsors">
        <div style="position: absolute; left: 50%; top: 50%;">
            <Trigger @triggerShow="$emit('show')"/>
        </div>
        <b-container>
            <b-row>
                <b-col class="sponsors-left" md=6 sm=12 order=2 order-md=1>
                    <img src="~assets/sponsors.png" class="sponsor-image-left"/>
                    <RegButton idGradient="3" idFilter1="30" idFilter2="300"/>
                </b-col>
                <b-col class="sponsors-right" md=6 sm=12 order=1 order-md=2>                  
                    <h1 class="sponsors-title">Партнеры и призы</h1>
                    <p style="padding: 0 0 50px 0">
                        Получи шанс выиграть фирменный мерч и образовательные курсы от наших партнеров.
                        <p></p>
                        Партнеры мероприятия:
                        <img src="~assets/sponsors.png" class="sponsor-image-right"/>
                        <p></p>
                        · MY.GAMES<br/>· GeekBrains<br/>· АНО «ИЦТО»
                    </p>
                    <LogoSponsor/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<style>
.sponsors {
    width: 100vw;
    padding: 60px 30px 60px 30px;
    position: relative;
    background: url('~assets/background.png') center center/100% 100%;
}
.sponsors-left {
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: space-between;
    flex-wrap: wrap;
    padding: 15px 0 0 0;
}
.sponsors-title {
    padding: 0 0 30px 0;
    font-family: 'Montserrat-Bold';
}
.sponsors-right {
    font-family: 'Montserrat';
    color: #fff;
}
.sponsor-image-left {
    position: relative;
    top: 50%;
    transform: translate(0, -50%);
    width: fit-content;
}
.sponsor-image-right {
    width: 40%;
    opacity: 0.48;
    float: right;
}
@media only screen and (max-width: 770px) {
    .sponsors-right {
        font-size: 18px;
    }
    .sponsors-title {
        font-size: 26px;
    }
    .sponsor-image-left {
        display: none;
    }
}
@media only screen and (min-device-width: 770px) {
    .sponsors-right {
        font-size: 24px;
    }
    .sponsor-image-right {
        display: none;
    }
}
</style>