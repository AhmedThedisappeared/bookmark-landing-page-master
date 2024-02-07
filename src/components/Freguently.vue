<template>
    <div class="faq">
        <div class="container-sm">
            <div class="text">
                <h2>Frequently Asked Questions</h2>
                <p>
                    Here are some of our FAQs. If you have any other questions you&apos;d
                    like answered please feel free to email us.
                </p>
            </div>
            <div class="faq-container">
                <Question 
                v-for="(question,index) in questionlist"
                :key="index"
                :question="question"
                />
            </div>
            <button class="btn btn-primary">More Info</button>
        </div>
    </div>
</template>

<script>
import Question from './Question.vue';
export default {
    data() {
        return {
            questionlist: [
                {
                    question: "What is Bookmark?",
                    answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt justo eget ultricies fringilla. Phasellus blandit ipsum quis quam ornare mattis.",
                    open: false
                },
                {
                    question: "How can I request a new browser?",
                    answer: "Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula.Suspendisse imperdiet. Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa,ultricies non ligula. Suspendisse imperdie tVivamus luctus eros aliquet convallis ultricies.Mauris augue massa, ultricies non ligula. Suspendisse imperdiet.",
                    open: false
                },
                {
                    question: "Is there a mobile app?",
                    answer: "Sed consectetur quam id neque fermentum accumsan. Praesent luctus vestibulum dolor, ut condimentum urna vulputate eget. Cras in ligula quis est pharetra mattis sit amet pharetra purus. Sed sollicitudin ex et ultricies bibendum.",
                    open: false
                },
                {
                    question: "What about other Chromium browsers?",
                    answer: "Integer condimentum ipsum id imperdiet finibus. Vivamus in placerat mi, at euismod dui. Aliquam vitae neque eget nisl gravida pellentesque non ut velit.",
                    open: false
                }
            ],
        }
    },
    components: {
        Question
    }
}
</script>

<style lang="scss" scoped>
.faq {
    margin: 4rem 0;
    > div {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .text {
        text-align: center;
        max-width: 450px;

        h2 {
            color: var(--Very-Dark-Blue);
            font-weight: 500;
            font-size: 26px;
        }

        p {
            line-height: 1.5;
            color: var(--Grayish-Blue);
            margin-top: 1rem;
        }
    }

    .faq-container {
        margin: 3rem 0;
        width: 100%;
    }
}
</style>
