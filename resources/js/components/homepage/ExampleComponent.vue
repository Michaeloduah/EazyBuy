<template>

    <!-- Nabar Start -->
        <header>
            <div class="logo">
                <img src="../img/logo.png" alt="">
                <a href="#" class="header__logo">EazyBuy</a>
            </div>
            <nav :class="['nav', { 'show': isActive }]" ref="nav-menu">
                <ion-icon name="close-outline" @click="closeSidebar" class="header__close" ref="close-menu"></ion-icon>

                <ul class="nav__list">
                    <li class="nav__item"><a href="#" class="nav__link">Home</a></li>
                    <li class="nav__item"><a href="#" class="nav__link">Services</a></li>
                    <li class="nav__item"><a href="#" class="nav__link">Who We Are</a></li>
                    <li class="nav__item"><a href="#" class="nav__link">About Us</a></li>
                    <li class="nav__item"><a href="#" class="nav__link">Contact Us</a></li>
                </ul>
            </nav>

            <ion-icon name="menu-outline" @click="openSidebar" class="header__toogle" ref="toogle-menu"></ion-icon>
        </header>
    <!-- Navbar End -->

    <!-- Hero Section Start -->
        <div class="hero">
            <div class="container">
            <div class="info">
                <h1>Title</h1>
                <h2>Lorem ipsum dolor sit amet consectetur.</h2>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatem vero ratione vitae dicta explicabo
                perferendis amet quis provident molestiae magni!</p>
                <a class="click" href="https://www.learningrobo.com/">Click Me</a>
                <div class="credit">Made with <span style="color:tomato">❤</span> by <a  href="https://www.learningrobo.com/">Learning Robo</a></div>
            </div>
            </div>
        </div>
    <!-- Hero Section End -->
</template>

<script>
    export default {

        data() {
            return {
                isActive: false
            };
        },

        methods: {
            openSidebar () {
                this.isActive = true;
            },
            closeSidebar () {
                this.isActive = false;
            }
        }
    }
</script>

<style scoped>
    /* Navbar Start */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        a {
            text-decoration: none;
        }

        ul {
            list-style: none;
        }

        header {
            display: flex;
            background-color: blue;
            justify-content: space-around;
            padding: 1rem 0;
            align-items: center;
            color: #eeeeee;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            width: 50px;
            border-radius: 50%;
            margin-right: 10px;
        }

        .header__logo {
            color: #eeeeee;
            font-weight: 600;
        }

        .nav__list {
            display: flex;
            align-items: center;
        }

        .nav__item {
            margin: 0 8px;
        }

        .nav__link {
            padding: 10px;
            color: #eeeeee;
            font-size: 0.9rem;
            font-weight: 500;
            border-radius: 5px;
        }

        .nav__link:hover {
            background-color: #00adb5;
        }

        .header__close,
        .header__toogle {
            display: none;
            cursor: pointer;
        }

        @media screen and (max-width:768px) {
            header{
                height: 50px;
                justify-content: space-between;
                padding: 0 28px;
            }
            .logo a {
                font-size: 0.9rem;
            }
            .logo img {
                width: 50px;
            }
            .header__toogle {
                display: inline;
                color: #eeeeee;
                font-size: 24px; 
            }
            .header__close {
                position: absolute;
                right: 24px;
                display: block;
                font-size: 24px;
                border-radius: 50%;
            }
            .header__close:hover {
                background-color: #00adb5;
            }
            .nav {
                position: fixed;
                top: 0;
                right: -100%;
                background-color: blue;
                color: #eeeeee;
                width: 50%;
                height: 100vh;
                padding: 24px 0;
                z-index: 100;
                transition: 0.5s;
                border-radius: 0 0 0 50%;
            }
            .nav__list{
                display: flex;
                flex-direction: column;
            }
            .nav__item {
                margin: 2rem 0;
            }
            .show{
                right: 0;
            }
        }
    /* Navbar End */

    /* Hero Section Start */
        .hero{
            width: 100%;
            height: auto;
            background-image: linear-gradient(rgba(0,0,0, 0.7),rgba(255,0,0, 0.2)),url(https://cdn.pixabay.com/photo/2017/01/30/16/11/sunset-2021266__340.jpg);
            background-position: center;
            background-size: cover;
            position: relative;
            color: #fff;
        }
        .container {
            width: 90%;
            height: 100%;
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: left;
        }
        .info h1 {
            font-size: 3rem;
            margin-bottom: .5rem;
        }
        .info h2 {
            font-size: 1.5rem;
            margin-bottom: 2rem;
        }
        .info p {
            font-size: 1.2rem;
            max-width: 50%;
        }
        .info .click{
            text-decoration: none;
            display: inline-block;
            background-color: #fff;
            border-radius: 4px;
            font-size: 1rem;
            padding: 0.5em 2em;
            margin-top: 2rem;
            color: black;
        }
        @media only screen and (max-width: 768px) {
        html {
            font-size: 10px;
        }
        }
        .credit a{
            text-decoration: none;
            color: #fff;
            font-weight: 800;
        }
        .credit {
            margin-top: 10px;
            font-size: 1.2rem;
        }
    /* Hero section Ends */

</style>