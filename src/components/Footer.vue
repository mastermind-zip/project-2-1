<template>
<footer class="footer">
    <div class="container">
        <div class="footer-up">
            <div class="footer-about">
                <p class="footer-title">Product</p>
                <p class="footer-text">Minimalistic products for a modern lifestyle, combining form and function in a sleek, user-friendly interface. </p>
            </div>
            <div class="footer-nav">
                <p class="footer-title">Support</p>
                <nav class="footer-nav">
                    <ul class="nav-list">
                        <li><router-link class="list-link">Contact</router-link></li>
                        <li><router-link class="list-link">FAQ</router-link></li>
                        <li><router-link class="list-link">Feedback</router-link></li>
                        <li><router-link class="list-link">Help</router-link></li>
                    </ul>
                </nav>
            </div>
            <div class="contacts">
                <p class="footer-title">Contact Us</p>
                <div class="nav-list">
                    <a href="" class="list-link">support@product.com</a>
                    <a href="" class="list-link">123-456-789</a>
                </div>
                <ul class="social-media">
                    <li>
                        <router-link><ion-icon name="logo-instagram" class="socials-icon"></ion-icon></router-link>
                    </li>
                    <li>
                        <router-link><ion-icon name="logo-facebook" class="socials-icon"></ion-icon></router-link>
                    </li>
                    <li>
                        <router-link><ion-icon name="logo-twitter" class="socials-icon"></ion-icon></router-link>
                    </li>
                </ul>
            </div>
        </div>
        <div class="footer-down">
            <p class="copyright">© 2024 Product, dedicated to customer satisfaction! </p>
            <p class="copyright">Terms & Conditions , Privacy Policy</p>
        </div>
    </div>
</footer>
</template>

<script>
export default {
    setup () {
        

        return {}
    }
}
</script>

<style  scoped>
.footer {
    padding: 9.6rem 0;
}

.footer-up {
    display: grid;
    grid-template-columns: 0.9fr 0.55fr 0.55fr;
    column-gap: 2.4rem;
    border-bottom: 1px solid #000;
    padding-bottom: 9.6rem;
}

.footer-title {
    font-size: 2.4rem;
    font-weight: 700;
    margin-bottom: 3.2rem;
}

.footer-text {
    width: 60%;
    font-size: 1.6rem;
    font-weight: 300;
    line-height: 1.7;
}

.nav-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 2.4rem;
}

.list-link:link, 
.list-link:visited {
    display: inline;
    font-size: 1.6rem;
    color: #111;
    text-decoration: none;
}



.social-media {
    margin-top: 2.4rem;
    list-style: none;
    display: flex;
    gap: 0.6rem;
}

.socials-icon {
    width: 2.2rem;
    height: 2.2rem;
    color: #111;
}

.footer-down {
    margin-top: 2.4rem;
    display: flex;
    justify-content: space-between;
}

.copyright {
    font-size: 1.6rem;
    font-weight: 400;
}




/* MEDIA QUERIES */

@media (max-width: 56em) {
    .footer-up {
        grid-template-columns: repeat(3, 0.5fr);
        padding-bottom: 6.4rem;
    }
    .footer-text {
        width: 80%;
    }
}

@media (max-width: 48em) {
    .footer-down {
        flex-direction: column;
        gap: 2.4rem;
    }
    .footer-text {
        font-size: 1.4rem;
    }
    .list-link:link,
    .list-link:visited {
        font-size: 1.4rem;
    }
}

@media (max-width: 36em) {
    .footer-up {
        grid-template-columns: repeat(2, 0.5fr);
        row-gap: 3rem;
        justify-content: center;
    }
    .footer-about {
        grid-column: 1 / -1;
        text-align: center;
    }
    .footer-text {
        width: 100%;
        padding: 0 2.4rem;
    }
}
@media (max-width: 30em ) {
    .footer-up {
        column-gap: 3.2rem;
    }
    .footer-title {
        font-size: 2rem;
    }
    .footer-text {
        padding: 0;
    }
}

</style>