<template>
    <div class="hero">
        <div class="container">
            <div class="img-box">
                <div class="bg-div"></div>
                <figure>
                    <img src="../assets/images/illustration-hero.svg" alt="illustration-hero" />
                </figure>
            </div>
            <div class="text-box flex flex-column">
                <h1>A Simple Bookmark Manager</h1>
                <p>
                    A clean and simple interface to organize your favourite websites. Open
                    a new browser tab and see your sites load instantly. Try it for free.
                </p>
                <div class="buttons flex">
                    <button class="btn btn-primary">Get it on Chrome</button>
                    <button class="btn btn-light">Get it on Firefox</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {};
    },
};
</script>

<style lang="scss" scoped>
    .hero {
        margin: 3rem 0;
        @media(min-width:768px) {
            margin-bottom: 0;
        }
        .container {
            .img-box {
                position: relative;
                margin-bottom: 5rem;
                .bg-div {
                    width: 100%;
                    height: 80%;
                    border-radius: 0 0 0 4rem;
                    background-color: var(--Soft-Blue);
                    position: absolute;
                    z-index: -1;
                    top: 3rem;
                    right: -4rem;
                }
            }
            .text-box {
                text-align: center;
                h1 {
                    font-weight: 500;
                    line-height: 1.2;
                    color: var(--Very-Dark-Blue);
                    font-size: 1.8rem;
                }
                p {
                    line-height: 1.5;
                    margin: 2rem 0;
                    color: var(--Grayish-Blue);
                }
                .buttons {
                    gap: 1rem;
                    justify-content: center;
                }
            }
            @media (min-width:768px) {
                margin-top: 4rem;
                display: flex;
                flex-direction: row-reverse;
                align-items: flex-start;
                div {
                    flex: 1;
                }
                .img-box {
                    position: relative;
                    right: -3rem;
                    img {
                        transform: scale(1.2);
                    }
                    .bg-div {
                        border-radius:0 0 0 8rem;
                        right: -15rem;
                        top: 7rem;
                    }
                }
                .text-box {
                    width: 50%;
                    max-width: 450px;
                    justify-content: flex-start;
                    text-align: left;
                    margin-top: 3rem;
                    h1 {
                        font-size: 2.5rem;
                    }
                    .buttons {
                        justify-content: flex-start;
                    }
                }
            }
        }

    }

</style>
