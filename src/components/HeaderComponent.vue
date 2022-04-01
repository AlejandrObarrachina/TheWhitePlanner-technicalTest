<template>
    <header>
        <div class="header-container">
            <div class="header-txt-container">
                <div class="title">
                    <a href="#" class="logo-wrapp">
                        <span>
                            <img
                                src="@/assets/images/logo.svg"
                                alt=""
                                class="logo"
                            />
                        </span>
                    </a>
                </div>
                <div class="links">
                    <a href="#" id="weddingplanners-btn" class="page-link"
                        >Wedding Planners</a
                    >
                    <a id="novios-btn" href="#" class="page-link">Novios</a>
                    <a id="log-in-btn" href="#" class="log-in-btn"
                        >Inicia sesión</a
                    >
                </div>
            </div>
            <input type="checkbox" id="hamburger-input" class="burger-shower" />
            <label id="hamburger-menu" for="hamburger-input">
                <nav id="sidebar-menu">
                    <span class="close-icon">
                        <img src="@/assets/images/close.png" alt="" srcset="" />
                    </span>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Store</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </nav>
            </label>

            <div class="overlay"></div>
        </div>
    </header>
</template>

<script>
export default {
    name: "ButtonComponent",
    data() {
        return {
            counter: "Contar",
            count: 0,
            erase: "Borrar",
        };
    },
    methods: {
        incrementCount() {
            this.count++;
        },
        resetCount() {
            this.count = 0;
        },
    },
};
</script>

<style scoped>
header {
    height: 25vh;
}
.header-container {
    display: block;
}
.logo-wrapp {
    display: inline;
}
.header-txt-container {
    display: flex;
    justify-content: space-between;
    padding-top: 1%;
    padding-left: 1%;
    padding-right: 1%;
    margin-left: 5px;
    margin-right: 5px;
}

.header-txt-container .links {
    align-self: center;
    width: 30%;
    display: flex;
    justify-content: flex-end;
}
.header-txt-container .links a {
    align-items: center;
    display: inline-block;
    white-space: nowrap;
    text-decoration: none;
    color: #000;

    margin-right: 15px;
}
.header-txt-container #weddingplanners-btn {
    text-decoration: underline;
    text-underline-offset: 7px;

    margin-right: 10px;
}
.links #novios-btn {
    margin-right: 70px !important;
}
.links .log-in {
    margin-left: 5px !important;
}

#log-in-btn {
    border: 2px solid #97aae3;
    border-radius: 30px;
    padding-left: 1rem;
    padding-right: 1rem;
    padding-top: 0.3rem;
    padding-bottom: 0.3rem;
    color: #97aae3;
}

#log-in-btn:hover {
    background-color: #6080e2;
    color: white;
    transition: all 0.3s ease-in-out;
    border-color: #6080e2;
}
#main-menu {
    display: block;
    height: 100px;
    width: 100%;
    background: #000;
    margin: 0px;
    z-index: 9;
}

#main-menu ul {
    max-width: 800px;
    width: 100%;
    height: 100%;
    margin: 0px auto;
    padding: 0px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    z-index: 9;
}

#main-menu li {
    list-style-type: none;
    font-size: 2rem;
}

#main-menu a {
    color: #000;
    font-size: 1.5rem;
    text-decoration: none;
}

#main-menu a:hover {
    text-decoration: underline;
}

#hamburger-input {
    display: none;
}

#hamburger-menu {
    position: fixed;
    top: 20px;
    right: 20px;
    width: 30px;
    height: 30px;
    display: none;
    border: none;
    padding: 0px;
    margin: 0px;

    background: linear-gradient(
        to bottom,
        black,
        black 10%,
        white 10%,
        white 33%,
        black 33%,
        black 43%,
        white 43%,
        white 66%,
        black 66%,
        black 76%,
        white 76%,
        white 100%
    );
    background-color: transparent !important;
}

#hamburger-menu #sidebar-menu {
    visibility: hidden;
    position: fixed;
    top: 0;
    right: -250px;
    width: 200px;
    height: 100%;
    background-color: #d7e3f9;
    transition: 0.3s;
    padding: 0px 10px;
    box-sizing: border-box;
    padding-top: 5%;
    padding-right: 5%;
}

#hamburger-menu h3 {
    color: #000;
    font-size: 2.2rem;
    background-color: transparent;
}

#hamburger-menu ul {
    padding-left: 0px;
    background-color: transparent;
}

#hamburger-menu li {
    list-style-type: none;
    line-height: 2.5rem;
    background-color: transparent;
    font-size: 16px;
}

#hamburger-menu a {
    color: #000;
    font-size: 1.3rem;
    text-decoration: none;
    background-color: transparent;
    font-size: 16px;
    font-weight: 500;
    font-style: normal;
}

#hamburger-menu a:hover {
    text-decoration: underline;
}

#hamburger-input:checked + #hamburger-menu #sidebar-menu {
    visibility: visible;
    right: 0;
    text-align-last: right;
}
#hamburger-input:checked ~ .overlay {
    visibility: visible;
    opacity: 0;
}
.close-icon {
    margin-top: 20%;
    background-color: transparent !important;
}
.close-icon img {
    background-color: transparent;
}

/* ---------------------RESPONSIVE MEDIA------------------------ */

@media screen and (max-width: 750px) {
    #main-menu {
        display: none;
    }
    #hamburger-menu {
        display: inline;
    }
    #log-in-btn {
        display: none;
    }
    .header-txt-container .links a {
        line-height: 1.3rem !important;
        margin-left: 2rem;
    }
    .header-txt-container {
        flex-direction: column;
    }
    .title {
        display: flex;
        justify-content: center;
    }
    .links {
        position: absolute;
        right: 5px;
        width: 100% !important;
        justify-content: flex-end;
    }
    .logo-wrapp {
        position: absolute;
        top: 56px;
    }
}

@media screen and (max-width: 320px) {
    .header-txt-container .links a {
        white-space: normal;
        text-align: center;
        line-height: 1.5rem;
    }
    .header-txt-container {
        padding-bottom: 2rem;
    }
    .logo-wrapp img {
        transform: scale(0.8);
    }
    .logo-wrapp {
        margin-top: 30px;
    }
}
</style>
