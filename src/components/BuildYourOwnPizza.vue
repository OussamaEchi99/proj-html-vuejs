<template>
    <section>
        <div class="col_left">
            <div class="image top one">
                
            </div>
            <div class="image center two">

            </div>
            <div class="image bottom three">

            </div>
        </div>
        <div class="col_center">
            <div class="image top one">
                
            </div>
            <div class="image center two">

            </div>
            <div class="image bottom three">

            </div>
        </div>
        <div class="col_right">
            <div class="image top one">
                
            </div>
            <div class="image center two">

            </div>
            <div class="image bottom three">

            </div>
        </div>
        <div class="text">
            <h2>GO AHEAD AND BUILD YOUR OWN PIZZA, WE WON'T JUDGE!</h2>
        </div>
        <a href="#" class="pizza_svg pizza_svg_grey"><img src="../assets/img/svg-4.svg" alt="Pizza Image"></a>
    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
section{
    display: flex;
    position: relative;
    .col_left, .col_right{
        width: calc(20% / 2);
        height: 800px;
        background-color: crimson;
    }

    .col_left{
        .one{
           background-position: right bottom;
       }

       .two{
           background-position: right top;
       }

       .three{
        background-position: 100% 75%;
       }
    }

    .col_center{
        width: 80%;
        height: 800px;
        background-color: black;

       .one{
           background-position: bottom;
       }

       .two{
           background-position: top;
       }

       .three{
        background-position: 85% 75%;
       }
    }

    .col_right{
        .one{
           background-position: left bottom;
       }

       .two{
           background-position: left top;
       }

       .three{
        background-position: 0% 75%;
       }
    }

    .image{
        background-image: url('../assets/img/h3-background-img.jpg');

        &.top, &.bottom{
            height: 200px;
        }

        &.center{
            height: 400px;
        }
    }

    .text{
        position: absolute;
        top: 50%;
        left: 30%;
        transform: translate(-50%,-50%);
        color: white;
        width: 24%;
        margin: auto;
        font-size: 55px;
        line-height: 90px;
    }

    .pizza_svg_grey{
        top: 65%;
    }
    
}
</style>