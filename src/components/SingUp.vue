<template>
    <div class="sing-up">
        <div class="container-sm">
            <span>35,000+ already joined</span>
            <h2>Stay up-to-date with what we&apos;re doing</h2>
            <form @submit.prevent="submitForm">
                <div class="input" :class="{error:error}">
                    <input type="text" placeholder="Enter your email address" v-model="emailValue">
                    <div class="error-img" v-if="error">
                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20"><g fill="none" fill-rule="evenodd"><circle cx="10" cy="10" r="10" fill="#FA5959"/><g fill="#FFF" transform="translate(9 5)"><rect width="2" height="7" rx="1"/><rect width="2" height="2" y="8" rx="1"/></g></g></svg>
                    </div>
                    <div class="error-msg" v-if="error">Whoops, make sure it's an email</div>
                </div>
                <button class="btn btn-danger">Contact Us</button>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            emailValue:'',
            error:false,
        }
    },
    methods: {
        submitForm() {
            const regExp = /^([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6})*$/;
            if(this.emailValue) {
                if(regExp.test(this.emailValue)) {
                    this.emailValue=''
                    this.error=false;
                }else {
                    this.error=true;
                }
            } else {
                this.error=true;
            }
        },
    }
}
</script>

<style lang="scss" scoped>
    .sing-up {
        margin-top: 4rem;
        background-color: var(--Soft-Blue);
        padding: 2rem 0;
        color: #fff;
        text-align: center;
        .container-sm {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        span {
            text-transform: uppercase;
            letter-spacing: 4px;
            word-spacing: 2px;
            font-size: 10px;
            color: #f0f0f0;
            font-weight: 500;
        }
        h2 {
            margin: 2rem 0;
            font-weight: 500;
        }
        form {
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 1rem;
            .input {
                position: relative;
                padding: 2px;
                border-radius: 6px;
                &.error {
                    background-color: var(--Soft-Red);
                }
                input {
                    width: 100%;
                    padding: 1rem 2rem;
                    border-radius: 5px;
                    border: none;
                    &:focus {
                        outline: none;
                    }
                    &::placeholder {
                        font-weight: 300;
                        color: var(--Grayish-Blue);
                    }
                }
                .error-img {
                    position: absolute;
                    right: 1rem;
                    top: 1rem;
                }
                .error-msg {
                    margin: 6px 10px;
                    text-align: left;
                    font-style: italic;
                    font-size: 12px;
                }
            }
            .btn {
                text-transform:capitalize;
            }
        }
        @media (min-width:992px) {
            h2 {
                font-size: 2rem;
                letter-spacing: 1px;
            }
            form {
                flex-direction: row;
                align-items: flex-start;
                .input {
                    flex: 1;
                }
            }
        }
    }
</style>