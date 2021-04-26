<template>
        <b-container class="date" id="Date">
            <div style="position: absolute; left: 50%; top: 50%;">
                <Trigger @triggerShow="$emit('show')"/>
            </div>
            <img src="~assets/date.png" class="date-image-left"/>
            <b-row>
                <b-col md=6 sm=12>
                    <h1 class="date-title">Сроки проведения хакатона</h1>
                    <div class="date-text">
                        <p class="date-subtitle">Лига <span class="underline-text">«GameDev Master»</span></p>
                        <p>
                            1 этап<br/> 
                            28 ноября - 5 декабря<br/><br/>
                            2 этап<br/>
                            7 декабря - 9 декабря
                        </p>
                        <hr/>
                        <p class="date-subtitle">Лига <span class="underline-text">«GameDev Junior»</span></p>
                        <p>
                            7 - 8 декабря<br/>
                            10:00-18:00
                        </p>
                        <hr/>
                        <p class="date-subtitle" style="color: #614efc">Итоги и награждение команд</p>
                        <p>10 декабря</p>
                    </div>
                </b-col>
                <b-col class="date-right" md=6 sm=12>
                    <img src="~assets/date.png" class="date-image-right"/>   
                </b-col>
            </b-row>
        </b-container> 
    
</template>

<style>
.date {
    padding: 60px 30px 60px 30px;
    position: relative;
}
.date-text {
    font-family: 'Montserrat';
}
.date-text hr {
   width: 60%;
   position: relative;
   left: 100%;
   transform: translate(-100%);
}
.date-text p{
    text-align: right;
}
.date-title {
    color: #614efc;
    font-family: 'Montserrat-Bold';
}
.date-subtitle {
    font-family: 'Montserrat-Bold';
    padding: 0 0 30px 0;
}
.underline-text {
    font-family: 'Montserrat-Bold-Italic';
}
.date-image-right {
    position: relative;
    top: 50%;
    transform: translate(0, -50%);
    width: 100%;
}
.date-image-left {
    position: absolute;
    width: 100%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.16;
}
@media only screen and (max-width: 770px) {
    .date-text {
        padding: 50px 60px 0 0;
        font-size: 18px;
        background: url('~assets/date-title.png') no-repeat center top/109% 100%;
    }
    .date-title {
        font-size: 26px;
    }
    .date-image-right {
        display: none;
    }
}
@media only screen and (min-device-width: 770px) {
    .date-image-left {
        display: none;
    }
    .date-text {
        padding: 50px 70px 0 0;
        font-size: 20px;
        background: url('~assets/date-title.png') no-repeat center top/109% 105%;
    }
}
</style>