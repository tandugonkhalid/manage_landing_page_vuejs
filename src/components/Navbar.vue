<template>
    <div class="navbar" id="home">
        <div class="logo">
            <a href="#home"><img src="images/logo.svg" alt="Logo"></a>
        </div>
        <div class="navbar-links">
            <ul>
                <li class="nav-link">Pricing</li>
                <li class="nav-link">Product</li>
                <li class="nav-link">About Us</li>
                <li class="nav-link">Careers</li>
                <li class="nav-link">Community</li>
            </ul>
        </div>
        <div class="nav-btn">
            <button type="submit">Get Started</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "Navbar",
}
</script>

<style lang="scss" scoped>
@import "../css/__colors.scss";
@import "../css/__fonts.scss";

.navbar{
    padding: 3rem 8rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.navbar-links ul{
    display: flex;
}

.navbar-links li{
    text-decoration: none;
    padding: 1em;
    list-style-type: none;
    font-family: "Be Vietnam", sans-serif;
    color: map-get($colors , very-dark-blue );
    transition: .5s ease;
}

li:hover{
    cursor: pointer;
    color: map-get($colors , dark-grayish-blue );
}


</style>