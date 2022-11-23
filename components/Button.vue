<template>
    <div class="btn-out" :style="hoverCol" @mouseover="mouseOver()">
        <a :href="link" :style="colorVar" class="btn"> {{ title }} </a>
    </div>
</template>

<script>
import { variableDeclaration } from '@babel/types';
import { computed } from '@vue/reactivity';

    export default {
        props: ['title', 'link', 'tColor', 'bColor', 'htColor', 'hbColor'],
        computed: {
            colorVar () {
               
                return 'background-color: var(' + this.bColor + '); color: var(' + this.tColor + ')'
                    //'Background-color: var(' + this.htColor + ')',
                    //'Background-color: var(' + this.hbColor + ')', 
            },
            hoverCol () {
                return 'background-color:' + this.hovering ? this.hbColor: 'red'
            },
        },
        data () {
            return {
                hovering: false
            }
        },
        methods: {
            mouseOver () {
                this.hovering = !this.hovering
                console.log(String(this.hovering))
                
            }
        }
    }
</script>

<style>
    .btn {
        /* background-color: var(--clr-blue); */
        font-weight: 700;

        /* color: var(--clr-white); */
        border: none;

        text-align: center center;
        text-decoration: none;
        display: inline-block;
        font-size: 25px;
        margin-top: 2rem;
        padding:0.6em 2em;
        border-radius: 20px;

    }
    .btn-out {
        margin: 5px;
    }
</style>