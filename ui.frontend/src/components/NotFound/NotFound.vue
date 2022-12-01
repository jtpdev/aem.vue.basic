<template>
    <div class="d404">
        <div class="d404-header">{{ header }}</div>
        <div class="d404-wrapper">
            <div class="d404-wrapper-container d404-wrapper-container-img">
                <img :src="img" :alt="altImg">
            </div>
            <div class="d404-wrapper-container">
                <div class="d404-wrapper-container-header">
                    {{ title }}
                </div>
                <div class="d404-wrapper-container-content">
                    {{ content }}
                </div>
                <div class="d404-wrapper-container-footer">
                    <button>
                        {{ btn }}
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'NotFound',
  props: {
    img: {
      type: String,
      default: require('@assets/espantalho.png')
    },
    altImg: {
      type: String
    },
    header: {
      type: String
    },
    title: {
      type: String
    },
    content: {
      type: String
    },
    btn: {
      type: String
    }
  }

}
</script>
<style lang="scss">
body {
    margin: 0;
    padding: 0;
    height: 100vh;
    box-sizing: border-box;
}

.d404 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100vw;
    background: #FFFFFF;
    color: #333333;
    font-family: 'Space Mono';
    font-style: normal;
    padding: 12px;
    text-align: start;

    &-header {
        width: 100%;
        font-family: 'Inconsolata';
        font-style: normal;
        font-weight: 700;
        font-size: 24px;
        line-height: 25px;
        letter-spacing: -0.08em;
        text-transform: uppercase;
    }

    &-wrapper {
        width: 100%;
        height: 720px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        justify-content: center;
        align-items: center;

        &-container {
            width: 40%;
            height: 100%;
            letter-spacing: -0.035em;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            justify-content: space-around;
            flex: 1;

            &-img {
                display: flex;
                justify-content: center;
                align-items: center;

                img {
                    display: block;
                    height: auto;
                    max-width: 80%;
                }
            }

            &-header,
            &-content,
            &-footer {
                width: 100%;
            }

            &-header {
                max-width: 35vw;
                font-weight: 700;
                font-size: 64px;
                line-height: 95px;
            }

            &-content {
                max-width: 23vw;
                font-weight: 400;
                font-size: 24px;
                line-height: 36px;
                color: #4F4F4F;
            }

            &-footer {
                width: 100%;

                button {
                    background: #333333;
                    text-transform: uppercase;
                    font-weight: 700;
                    font-size: 14px;
                    line-height: 21px;
                    padding: 24px 43px;
                    border-radius: 0;
                    color: #FFFFFF;

                    &:hover {
                        background: #3f3f3f;
                    }

                    &:active {
                        background: #272727;
                    }
                }
            }
        }
    }

}

@media only screen and (max-width: 640px) {
    .d404-wrapper {
        flex-direction: column;

        &-container {
            width: 100%;

            &-header {
                max-width: 100vw;
                font-weight: 700;
                font-size: 48px;
                line-height: 71px;
            }

            &-content {
                max-width: 100vw;
                font-weight: 400;
                font-size: 18px;
                line-height: 27px;
            }

        }
    }
}
</style>
