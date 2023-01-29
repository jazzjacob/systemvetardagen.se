<template>
    <section>
        <div class="info">
            <div class="info-first">
                <h3 style=" color:var(--clr-pink-600); text-align: center;">{{ $t('before_the_fair') }}</h3>
                <p><ul>
                    <li>{{ $t('before_the_fair_description1') }}</li>
                    <li>{{ $t('before_the_fair_description2') }}</li>
                    <li>{{ $t('before_the_fair_description3') }}</li>
                    <li>{{ $t('before_the_fair_description4') }}</li>
                </ul></p>
                <p>{{ $t('before_the_fair_description5') }}</p>
            </div>
            <div class="info-second">
                <h3 style="color:var(--clr-blue-600); text-align: center;">{{ $t('during_the_fair') }}</h3>
                <p><ul>
                    <li>{{ $t('during_the_fair_description1') }}</li>
                    <li>{{ $t('during_the_fair_description2') }}</li>
                    <li>{{ $t('during_the_fair_description3') }}</li>
                </ul></p>
            </div>
        </div>

        <div class="faq">
            <h2 style="color:var(--clr-blue-600); display: flex; justify-content: center;">{{ $t('frequently_asked_questions') }}</h2>
            <div class="faq-question">
                <h3 style="max-width: 28ch; color: var(--clr-pink-600);">{{ $t('question1') }}</h3>
                <p>
                    {{ $t('answer1') }}
                </p>
            </div>
            <div class="faq-question">
                <h3 style="max-width: 28ch; color: var(--clr-pink-600);">{{ $t('question2') }}</h3>
                <p>
                    {{ $t('answer2') }}
                </p>
            </div>
            <div class="faq-question">
                <h3 style="max-width: 28ch; color: var(--clr-pink-600);">{{ $t('question3') }}</h3>
                <p>
                    {{ $t('answer3') }}
                </p>
            </div>
        </div>

        <Blob type="4-p" height="30rem" class="blob-l" />
        <!-- <Blob type="10-p" height="35rem" class="blob-p" /> -->
        <Blob type="8-p" height="35rem" class="blob-r" />


	</section>



</template>

<script>
    import Button from '@/components/Button.vue'
    import Blob from "@/components/Blob.vue";

    export default {
        name: 'heroSection'
    }
    components: {
        Button, Blob
    }

</script>
<style>
    .faq {
        z-index: 100;
    }

    .blob-l {
        left: 0;
        top: 180rem;
        transform: translateX(-40%);
    }
    .blob-p {
        background-image: "@/assets/img/nod_11.jpg";
        left: 10rem;
        top: 170rem;

    }
    .blob-p >img {
        background-image: "@/assets/img/nod_11.jpg";
    }
    .blob-r {
       right:0;
        transform: translateX(40%) translateY(50%);
    }
    .info{
        display:flex;
        flex-direction: column;
        position: relative;
        text-align: left;
        background:  linear-gradient(0deg, rgba(255, 255, 255, 0.4), rgba(255, 255, 255, 0.4));
        background-position: center;
        background-size: cover;
        height: 100vh;
        background-repeat: no-repeat;
        margin-bottom: 0rem;
        margin-top: 0rem;
        padding-bottom:2%;
        z-index: 101;
    }
    .info-first{
        margin-left: 0rem;
    }
    .info-second{
        margin-left: 0rem;
    }

</style>