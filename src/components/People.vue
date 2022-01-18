<template>
    <section>
        <div class="person">
            <img src="../assets/img/h1-team-1a-700x700.jpg" alt="Peter Anderson Image">
            <div class="overlay">
                <img src="../assets/img/poits_background.jpg" alt="Overlay">
                <div class="text">
                    <h3>PETER ANDERSON</h3>
                    <span>Head Chef</span>
                    <div class="socials">
                        <a href="#"><i class="fab fa-instagram-square"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
            </div>
        </div>
        <div class="person">
            <img src="../assets/img/h1-team-2a.jpg" alt="Sharon Hayes Image">
            <div class="overlay">
                <img src="../assets/img/poits_background.jpg" alt="Overlay">
                <div class="text">
                    <h3>SHARON HAYES</h3>
                    <span>Executice Chef</span>
                    <div class="socials">
                        <a href="#"><i class="fab fa-instagram-square"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
            </div>
        </div>
        <div class="person">
            <img src="../assets/img/h1-team-4a.jpg" alt="Frank Bailey Image">
            <div class="overlay">
                <img src="../assets/img/poits_background.jpg" alt="Overlay">
                <div class="text">
                    <h3>FRANK BAILEY</h3>
                    <span>Kitchen Porter</span>
                    <div class="socials">
                        <a href="#"><i class="fab fa-instagram-square"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
            </div>
        </div>
        <div class="person">
            <img src="../assets/img/h1-team-3a.jpg" alt="">
            <div class="overlay">
                <img src="../assets/img/poits_background.jpg" alt="Overlay">
                <div class="text">
                    <h3>CAROL SIMPSON</h3>
                    <span>Sous Chef</span>
                    <div class="socials">
                        <a href="#"><i class="fab fa-instagram-square"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
            </div>
        </div>
        <a href="#" class="pizza_svg pizza_svg_grey"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '../style/Variables.scss';

section{
    display: flex;
    margin: 8px 0;
    position: relative;
    .person{
        width: calc(100% / 4);
        position: relative;

        .overlay{
            position: absolute;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
            height: 100%;
            width: 100%;
            opacity: 0;
            transition: .5s ease;

            .text {
                position: absolute;
                top: 0;
                bottom: 0;
                left: 0;
                right: 0;
                height: 100%;
                width: 100%;
                opacity: 0;
                transition: .5s ease;
                background-color: $brand_primary_color;
                transform: scale(0.85);
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                color: white;

                h3{
                    font-size: 25px;
                    font-weight: 500;
                }

                span{
                    font-weight: 400;
                    margin-top: 5px;
                }

                .socials {
                    margin: 20px 0;

                    a{
                        margin: 0 10px;
                    }
                }
            }
        }

        &:hover .overlay{
            opacity: 1;
        }

        &:hover .overlay .text{
            opacity: 1;
        }
    }
    .pizza_svg{
        bottom: 50px;
    }
}
</style>