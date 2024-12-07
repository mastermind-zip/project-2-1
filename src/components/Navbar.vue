<template>
<header class="header">
    <div class="header-logo">
        <h3 class="product-brand">Product</h3>
    </div>
    <nav class="main-nav-bar" :class="{ 'nav-open': isOpen}">
        <ul class="main-nav-list">
            <li>
                <router-link class="nav-links">Home</router-link>
            </li>
            <li>
                <router-link class="nav-links">Products</router-link>
            </li>
            <li>
                <router-link class="nav-links">About</router-link>
            </li>
            <li>
                <router-link class="nav-links">Contact</router-link>
            </li>
        </ul>
    </nav>
    <div class="nav-cta-btn">
        <p class="cta-textbox">Shop now</p>
    </div>
    <div class="nav-menu">
        <ion-icon name="menu-outline" class="nav-menu-icon" @click="toggleNav" v-if="!isOpen"></ion-icon>
        <ion-icon name="close-outline" class="nav-close-icon" @click="toggleNav" v-if="isOpen"></ion-icon>
    </div>
</header>
</template>

<script>
export default {
    data() {
        return {
            isOpen: false,
        };
    },
    methods: {
        toggleNav() {
            this.isOpen = !this.isOpen;
        }
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@200..800&display=swap');

.header {
    padding: 0 3.2rem;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #1C6758;
    height: 12.8rem;
    color: #fff;
    gap: 8rem;
}

.product-brand {
    font-size: 2.4rem;
    font-family: "Manrope", sans-serif;
    font-weight: 700;
}

.main-nav-list {
    display: flex;
    gap: 2.4rem;
    list-style: none;
}

.nav-links:link,
.nav-links:visited {
    font-size: 1.6rem;
    font-weight: 400;
    font-family: "Manrope", sans-serif;
    text-decoration: none;
    color: #fff;
}


.nav-cta-btn {
    background-color: #fff;
    color: #000;
    padding: 1.6rem 3.2rem;
    border-radius: 21px;
}


.cta-textbox {
    font-size: 1.6rem;
    font-weight: 600;
    font-family:  "Manrope", sans-serif;
}

.nav-menu {
    display: none;
}

.nav-menu-icon {
    width: 3.6rem;
    height: 3.6rem;
}
.nav-close-icon {
    color: #111;
    width: 3.6rem;
    height: 3.6rem;
    z-index: 9999;
}




/* MEDIA QUERIES */


@media (max-width: 48em) {
    .header {
        padding: 0 4.8rem;
        justify-content: space-between;
    }

    .main-nav-bar {
        position: absolute;
        background-color: #fff;
        top: 0%;
        right: 0%;
        height: 110vh;
        width: 50%;
        padding: 12.8rem 4.8rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        opacity: 0;
    }
    .main-nav-list {
        flex-direction: column;
        align-items: end;
    }

    .nav-links:link, 
    .nav-links:visited {
        color: #333;
        font-size: 3rem;
    }

    .nav-cta-btn {
        background-color: transparent;
        padding: 0;
    }

    .nav-menu {
        display: block;
    }
    .cta-textbox {
        display: none;
    }

    .main-nav-bar.nav-open {
        opacity: 1;
    }
    

}

@media (max-width: 42em) {
    .main-nav-bar {
        width: 75%;
    }
}

</style>