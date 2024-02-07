<template>
    <div class="extensions">
        <div class="container">
            <div class="text">
                <h2>Download the extension</h2>
                <p>
                    We&apos;ve got more browsers in the pipeline. Please do let us know if you&apos;ve
                    got a favourite you&apos;d like us to prioritize.
                </p>
            </div>
            <div class="extension-container">
                <div class="card flex flex-column">
                    <img src="../assets/images/logo-chrome.svg" alt="logo-chrome">
                    <h2>Add to Chrome</h2>
                    <p>Minimum version 62</p>
                    <button class="btn btn-primary btn-block">Add & Install Extension</button>
                </div>
                <div class="card flex flex-column">
                    <img src="../assets/images/logo-firefox.svg" alt="logo-chrome">
                    <h2>Add to Firefox</h2>
                    <p>Minimum version 55</p>
                    <button class="btn btn-primary btn-block">Add & Install Extension</button>
                </div>
                <div class="card flex flex-column">
                    <img src="../assets/images/logo-opera.svg" alt="logo-chrome">
                    <h2>Add to Opera</h2>
                    <p>Minimum version 46</p>
                    <button class="btn btn-primary btn-block">Add & Install Extension</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script></script>

<style lang="scss" scoped>
    .extensions {
        margin: 5rem 0;
        .text {
            text-align: center;
            max-width: 500px;
            margin: auto;
            h2 {
                color: var(--Very-Dark-Blue);
                font-weight: 500;
            }
            p {
                line-height: 1.5;
                color: var(--Grayish-Blue);
                margin: 1rem 0 2rem;
            }
        }
        .extension-container {
            margin-top: 3rem;
            display: grid;
            grid-template-columns: repeat(auto-fill ,minmax( 250px ,280px));
            justify-content: center;
            gap: 2rem;
            .card {
                padding: 1.5rem;
                border-radius: 1rem;
                background-image: url(../assets/images/bg-dots.svg);
                background-repeat: no-repeat;
                background-size: 100%;
                background-position: center 75%;
                align-items: center;
                box-shadow: 4px 4px 20px 0 #ddd;
                img {
                    width: 100px;
                    height: 100px;
                    margin: 2.5rem 0;
                }
                h2 {
                    color: var(--Very-Dark-Blue);
                    font-weight: 500;
                }
                p {
                    line-height: 1.5;
                    color: var(--Grayish-Blue);
                    margin: 1rem 0 2rem;
                }
                button {
                    margin-top: 3rem;
                }
            }
            @media (min-width:992px) {
                height: 500px;
                gap: 2rem;
                > div:first-of-type {
                    align-self: flex-start;
                }
                > div:nth-child(2) {
                    align-self: center;
                }
                > div:last-of-type {
                    align-self: flex-end;
                }
            }
        }
    }
</style>