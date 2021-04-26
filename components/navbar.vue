<template>
    <b-navbar toggleable="sm" sticky>
        <b-navbar-toggle target="navbar-toggle-collapse" class="button" style="margin: 15px">
            <template #default="{ expanded }">
                <b-icon v-if="expanded"><IconClose/></b-icon>
                <b-icon v-else><IconOpen/></b-icon>
            </template>
        </b-navbar-toggle>

        <b-collapse id="navbar-toggle-collapse" is-nav>
            <b-navbar-nav class="navbar-center" justified>
                <b-nav-item class="nav-item-center" @mouseover="isHovering = true" @mouseout="isHovering = false" :class="{active: curr_item==='/' && !isHovering}" href="/#">Главная</b-nav-item>
                <b-nav-item class="nav-item-center" @mouseover="isHovering = true" @mouseout="isHovering = false" :class="{active: curr_item==='Experts' && !isHovering}" href="#Experts">Эксперты</b-nav-item>
                <b-nav-item class="nav-item-center" @mouseover="isHovering = true" @mouseout="isHovering = false" :class="{active: curr_item==='Date' && !isHovering}" href="#Date">Даты</b-nav-item>
                <b-nav-item class="nav-item-center" @mouseover="isHovering = true" @mouseout="isHovering = false" :class="{active: curr_item==='Sponsors' && !isHovering}" href="#Sponsors">Партнеры</b-nav-item>
                
                <RegButton class="fix-button" idGradient="1" idFilter1="10" idFilter2="100"/>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>
</template>

<style>
.navbar {
    background: #fff;
    padding: 0;    
}
.navbar-center {
    background: #fff;
    margin: 0 auto;
}
.nav-item-center {
    font-family: "Montserrat";
    font-size: 18px;
    cursor: pointer;
}
.nav-item-center a{
    height: 100%;
    display: flex;
    align-items: center;
    padding: 20px 30px 15px 30px;
    padding-right: 30px !important;
    padding-left: 30px !important;
}
.navbar-center li:hover, .navbar-center li.active  { 
    background-color: #F5F5F5;
}

.button, .button:hover, .button:focus{
    border: none;
    outline: none;
    text-decoration: none;
}
.fix-button {
    margin: 10px 0 10px 0px;       
    padding: 10px 0 10px 0;
}
@media only screen and (min-device-width: 720px) {
    .fix-button {
        margin: 10px 0 10px 30px;
    }
}   
</style>

<script>
export default {
    name: 'header',
    props: ['curr_item'],
    data() {
        return {
            isHovering: false
        }
    }
}
</script>
