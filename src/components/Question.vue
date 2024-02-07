<template>
    <div class="question">
        <div class="header">
            <span>{{ question.question }}</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="12" :class="{ open: showAnswer }"
                @click.stop="toggleShowAnswer">
                <path fill="none" stroke="#5267DF" stroke-width="3" d="M1 1l8 8 8-8" />
            </svg>
        </div>
        <div class="body" v-if="showAnswer">
            <p>{{ question.answer }}</p>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            showAnswer:this.question.open,
        }
    },
    props:['question'],
    methods: {
        toggleShowAnswer() {
            this.showAnswer=!this.showAnswer
        }
    }
}
</script>
<style lang="scss" scoped>
.question {
    border-bottom: 2px solid #ccc;
    padding: 2rem 0;
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        span {
            color: var(--Very-Dark-Blue);
            font-weight: 500;
        }
        svg {
            cursor: pointer;
            transition: all 0.5s ease-in-out;
            &.open {
                transform: rotate(180deg);

                path {
                    stroke: var(--Soft-Red);
                }
            }
        }
    }
    .body {
        margin-top: 2rem;
        p {
            line-height: 1.5;
            color: var(--Grayish-Blue);
        }
    }
}
</style>