<template>
    <b-container class="description">                
        <img src="~assets/description.png" class="desc-image-left"/>
        <b-row>        
            <b-col class="description-left" md=6 sm=12>            
                <h1 class="description-title">Хакатон по разработке игр в дистанционном формате</h1>
                <p>Это соревнование бросает вызов твоим навыкам разработки игр. Попробуй свои силы в роли программиста, геймдизайнера или художника.</p>
                <p>Для тебя мы подготовили две лиги: <span class="underline-text">«GameDev Master»</span> и <span class="underline-text">«GameDev Junior»</span>. Первая предназначена только для студентов НИУ ВШЭ любого кампуса, любого факультета. Вторая же подойдет для учащихся школ 9 – 11 классов.</p>
                <p>Выбери подходящую тебе лигу, собери команду и получи шанс выиграть призы от наших партеров. Если у тебя нет команды – не беда: наши организаторы подберут тебе подходящую команду, и вы вместе создадите качественный прототип игры в кратчайшие сроки. Участвуй и борись за победу в схватке игроразработчиков!</p>
            </b-col>
            <b-col class="description-right" md=6 sm=12>
                <img src="~assets/description.png" class="desc-image-right"/>
                <RegButton idGradient="2" idFilter1="20" idFilter2="200"/>
            </b-col>
        </b-row>
    </b-container>  
</template>

<style>
.description {
    padding: 60px 30px 60px 30px;
    position: relative;
}
.description-title {
    color: #614efc;
    font-family: 'Montserrat-Bold';
    padding: 0 0 30px 0;
}
.underline-text {
    color: #614EFC;
    font-family: 'Montserrat-Italic';
}
.description-left {
    font-family: 'Montserrat';
}
.description-right {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
.desc-image-right {
    position: relative;
    top: 50%;
    transform: translate(0, -50%);
    width: 100%;
}
.desc-image-left {
    position: absolute;
    width: 100%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.16;
}
@media only screen and (max-width: 770px) {
    .desc-image-right {
        display: none;
    }
    .description-title {
        font-size: 26px;
    }
}
@media only screen and (min-device-width: 770px) {
    .desc-image-left {
        display: none;
    }
    .description-left {
        font-size: 20px;
    }
}
</style>
