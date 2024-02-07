<template>
    <div class="feat">
        <div class="img-box">
            <div class="right-bg"></div>
            <figure>
                <img src="../assets/images/illustration-features-tab-3.svg" alt="">
            </figure>
        </div>
        <div class="text">
            <h2>
                Share your bookmarks
            </h2>
            <p>
                Easily share your bookmarks and collections with others. Create a shareable
                link that you can send at the click of a button.
            </p>
            <button class="btn btn-primary">More Info</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FeatThree',
}
</script> 

<style lang="scss" scoped>
.feat {
    display: flex;
    flex-direction: column;
    align-items: center;

    .img-box {
        position: relative;
        margin-bottom: 5rem;
        display: flex;
        justify-content: center;

        .right-bg {
            position: absolute;
            z-index: -1;
            width: 200%;
            height: 90%;
            top: 3rem;
            left: -122%;
            border-radius: 0 5rem 5rem 0;
            background-color: var(--Soft-Blue);
        }
    }

    .text {
        max-width: 400px;
        margin: auto;

        h2 {
            color: var(--Very-Dark-Blue);
            font-weight: 500;
        }

        p {
            line-height: 1.5;
            color: var(--Grayish-Blue);
            margin-top: 1rem;
        }
        .btn {
            margin-top: 2rem;
        }
        @media (max-width:991px) {
            text-align: center;
            .btn {
                display: none;
            }
        }
    }
    @media(min-width:992px) {
        display: flex;
        flex-direction: row;
        div {
            flex: 1;
        }
        .img-box {
            margin-bottom: 0;
            .right-bg {
                width: 110%;
                top: 4.5rem;
                left: -15rem;
                border-radius: 0 10rem 10rem 0;
            }
        }
    }
}
</style>