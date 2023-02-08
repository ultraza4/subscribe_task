<template>
    <div class="popup-wrapper">
        <div class="popup">
            <div class="right-bg-wrapper">
                <div class="right-bg-frame">
                    <div class="bg-img"></div>
                </div>
                <div class="bg-purple1"></div>
                <div class="bg-purple2"></div>
            </div>
            <div class="title">
                10%
                <span>off</span>
            </div>
            <header>
                <div class="header-subtitle">your first order</div>
                <div class="rectangle"></div>
                <div class="description">
                    Subscrive to recieve 10% off promocode plus exclusive offers and deals
                </div>
            </header>
            <div class="form">
                <div class="input-wrapper">
                    <span class="form-title">Email-adress</span>
                    <input class="input" type="text">
                </div>
                <button class="form-btn">
                    <span>Subscribe!</span>
                </button>
                <div class="checkbox-wrapper">
                    <input type="checkbox">
                    <span>I'm agree with privacy policy</span>
                </div>
            </div>
            <!-- <div class="bg-picture"></div> -->
            <!-- <button @click="$emit('setShow')">close</button> -->
        </div>
    </div>
</template>

<script>
export default {
    emits: ["setShow"]

}

</script>

<style lang="scss">
$grey1: #2F3639;
$grey3: #595E61;
$grey4: #828688;
$grey6: #D5D7D7;
$purple1: #C24DFE;

.popup-wrapper {
    width: 100vw;
    height: 100vh;
    background-color: rgb(160, 160, 160, .5);
    display: flex;
    align-items: center;
    position: absolute;
    top: 0;
    left: 0;

    .popup {
        width: 864px;
        height: 501px;
        margin: auto;
        background-color: #F5F5F5;
        display: flex;
        flex-direction: column;
        padding: 0px 32px;
        overflow: hidden;
        position: relative;
        box-shadow: 0px 8px 20px rgba(68, 75, 77, 0.15);
        border-radius: 8px;

        .title {
            display: flex;
            align-items: baseline;
            position: absolute;
            width: 416px;
            height: 104px;
            left: 32px;
            top: 40px;
            font-style: normal;
            font-weight: 700;
            font-size: 104px;
            line-height: 100%;
            color: $grey1;

            span {
                font-size: large;
            }
        }

        header {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            padding: 0px;
            gap: 26px;
            position: absolute;
            width: 339px;
            height: 112px;
            left: 32px;
            top: 160px;

            .header-subtitle {
                width: 416px;
                height: 24px;
                font-style: normal;
                font-weight: 700;
                font-size: 24px;
                line-height: 100%;
                color: $grey4;
                flex: none;
                order: 0;
                flex-grow: 0;
            }

            .rectangle {
                width: 67px;
                height: 2px;
                background: $purple1;
                border-radius: 10px;
                flex: none;
                order: 1;
                flex-grow: 0;
            }

            .description {
                width: 373px;
                height: 34px;
                font-style: normal;
                font-weight: 400;
                font-size: 14px;
                line-height: 120%;
                display: flex;
                align-items: center;
                color: $grey3;
                flex: none;
                order: 2;
                flex-grow: 0;
            }
        }

        .form {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            padding: 0px;
            gap: 16px;
            position: absolute;
            width: 302px;
            height: 150px;
            left: 32px;
            top: 312px;

            .input-wrapper {
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                padding: 0px;
                gap: 8px;
                width: 302px;
                height: 62px;
                flex: none;
                order: 0;
                flex-grow: 0;

                .form-title {
                    width: 71px;
                    height: 14px;
                    font-style: normal;
                    font-weight: 700;
                    font-size: 12px;
                    line-height: 14px;
                    color: $grey4;
                    flex: none;
                    order: 0;
                    flex-grow: 0;
                }

                .input {
                    width: 302px;
                    height: 40px;
                    background: #FFFFFF;
                    border: 1px solid $grey6;
                    border-radius: 6px;
                    flex: none;
                    order: 0;
                    flex-grow: 0;
                }
            }

            .form-btn {
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                padding: 13px 0px;
                gap: 10px;
                width: 106px;
                height: 40px;
                background: $purple1;
                border-radius: 35px;
                flex: none;
                order: 1;
                flex-grow: 0;
                border: none;
                cursor: pointer;
                span {
                    width: 58px;
                    height: 14px;
                    font-style: normal;
                    font-weight: 700;
                    font-size: 12px;
                    line-height: 14px;
                    display: flex;
                    align-items: center;
                    text-align: center;
                    color: #FFFFFF;
                    flex: none;
                    order: 0;
                    flex-grow: 0;
                }
            }

            .checkbox-wrapper {
                display: flex;
                flex-direction: row;
                align-items: flex-start;
                padding: 0px;
                gap: 8px;
                width: 201px;
                height: 16px;
                flex: none;
                order: 2;
                flex-grow: 0;

                input[type="checkbox"] {
                    appearance: none;
                    background-color: #fff;
                    display: grid;
                    place-content: center;
                    width: 16px;
                    height: 16px;
                    border: 2px solid $purple1;
                    border-radius: 4px;

                    flex: none;
                    order: 0;
                    flex-grow: 0;

                    &:before {
                        content: "";
                        width: 8px;
                        height: 8px;
                        background-color: $purple1;
                        transform: scale(0);
                        transition: 120ms transform ease-in-out;
                        box-shadow: inset 1em 1em var(--form-control-color);
                    }

                    &:checked {
                        &:before {
                            transform: scale(1);
                        }
                    }
                }

                span {
                    width: 177px;
                    height: 16px;
                    font-family: 'Roboto';
                    font-style: normal;
                    font-weight: 500;
                    font-size: 14px;
                    line-height: 16px;
                    display: flex;
                    align-items: center;
                    color: $grey3;
                    flex: none;
                    order: 1;
                    flex-grow: 0;
                }
            }
        }
        .right-bg-wrapper {
            position: absolute;
            width: 581px;
            height: 502px;
            left: 283px;
            top: 0px;
        
            .right-bg-frame {
                position: absolute;
                width: 403px;
                height: 764px;
                left: 161px;
                top: -159px;
                transform: rotate(-30deg);
                overflow: hidden;
                z-index: 1000;
                .bg-img {
        
                    position: absolute;
                    width: 581px;
                    height: 502px;
                    left: -164px;
                    top: 119px;
                    overflow: hidden;
                    background: url('../assets/image38.png');
                    transform: rotate(30deg);
                    z-index: 1000;
                }
            }
        
            .bg-purple1 {
                position: absolute;
                width: 224px;
                height: 887.96px;
                left: 155px;
                top: -150.02px;
                background: $purple1;
                transform: rotate(-15deg);
                z-index: 100;
            }
        
            .bg-purple2 {
                position: absolute;
                width: 224px;
                height: 887.96px;
                left: 330px;
                top: -228.02px;
                background: $purple1;
                transform: rotate(-15deg);
                z-index: 100;
            }
        
        }
    }
}


</style>