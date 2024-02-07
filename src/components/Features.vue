<template>
    <div class="features">
        <div class="container">
            <article>
                <h1>Features</h1>
                <p>
                    Our aim is to make it quick and easy for you to access your favourite websites.
                    Your bookmarks sync between your devices so you can access them on the go.
                </p>
            </article>
            <ul ref="tab">
                <li v-for="(tab ,index) in tabList" :key="index" @click="toggleTab($event,index)"> {{ tab.text }}</li>
            </ul>
            <component :is="activeComp"></component>
        </div>
    </div>
</template>

<script>
import FeatOne from './FeatOne.vue';
import FeatTwo from './FeatTwo.vue';
import FeatThree from './FeatThree.vue';
export default {
    data() {
        return {
            activeComp:'FeatOne',
            tabList: [
                {text:"Simple Bookmarking" ,component:"FeatOne"},
                {text:"Speedy Searching" ,component:"FeatTwo"},
                {text:"Easy Sharing" ,component:"FeatThree"},
            ]
        }
    },
    components: {
        FeatOne,
        FeatTwo,
        FeatThree
    },
    methods: {
        toggleTab(e,index) {
            const parent =Array.from(e.target.parentElement.children);
            parent.forEach(element => {
                element.classList.remove("active")
                parent[index].classList.add("active")
            });
            this.activeComp = this.tabList[index].component
        }
    },
    mounted() {
        this.$refs.tab.children[0].classList.add("active")
    }
}
</script> 

<style lang="scss" scoped>
    .features {
        margin: 7rem 0;
        article {
            text-align: center;
            max-width: 490px;
            margin: auto;
            h1 {
                color: var(--Very-Dark-Blue);
                font-weight: 500;
            }
            p {
                line-height: 1.5;
                color: var(--Grayish-Blue);
                margin-top: 1rem;
            }
        }
        ul {
            margin: 3rem auto;
            max-width: 800px;
            text-align: center;
            li {
                width: 100%;
                position: relative;
                padding: 1rem 0;
                font-size: 18px;
                font-weight: 400;
                color: var(--Grayish-Blue);
                transition: all 0.12s ease-in-out;
                cursor: pointer;
                &:hover {
                    color: var(--Soft-Red);
                }
                &::after {
                    content: "";
                    position: absolute;
                    width: 50%;
                    background-color: transparent;
                    height: 3px;
                    bottom: 0;
                    left: 50%;
                    transform: translateX(-50%);
                }
                &.active {
                    color: var(--Very-Dark-Blue);
                    &::after {
                        background-color: var(--Soft-Red);
                    }
                }
            }
            li:not(:nth-child(2)) {
                @media (max-width:767px) {
                    border-top: 2px solid #eee;
                    border-bottom: 2px solid #eee;
                }
            }
            @media (min-width:768px) {
                display: flex;
                border-bottom: 2px solid #eee;
                li {
                    flex: 1;
                    &::after {
                        width: 100%;
                    }
                }
            }
        }
    }
</style>