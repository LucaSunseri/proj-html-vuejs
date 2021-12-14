<template>
    <div class="ls-footer">
        <div class="container">
            <div class="row">
                <div class="col-12 col-sm-6 col-lg-3 mb-2">
                    <img
                        src="../assets/img/logo-sidearea-1.png"
                        alt="Logo Maree"
                    />
                    <p>Let's Get Creative</p>
                </div>
                <div class="col-12 col-sm-6 col-lg-3 mb-2">
                    <p>maree.qode@gmail.com</p>
                    <p>+44645 321 789</p>
                </div>
                <div class="col-12 col-sm-6 col-lg-3 mb-2">
                    <p>Avenue d’Auderghem 10</p>
                    <p>1040 Brussels, Belgium</p>
                </div>
                <div class="col-12 col-sm-6 col-lg-3 mb-2">
                    <p>Stay in touch with us</p>
                    <a href="#"> <i class="fab fa-twitter"></i> </a>
                    <a href="#"> <i class="fab fa-pinterest-p"></i></a>
                    <a href="#"> <i class="fab fa-facebook-f"></i> </a>
                    <a href="#"> <i class="fab fa-linkedin-in"></i> </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
};
</script>

<style lang="scss" scoped>
.ls-footer {
    background-color: #c0e1cf;
    padding: 80px 0;
    font-weight: 300;
    p {
        margin: 8px 0;
    }
    a {
        color: black;
    }
    .fab {
        font-size: 18px;
        padding: 0 12px;
    }
}
</style>
