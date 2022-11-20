<template>
    <div class="btn-out">
        <a href="" class="btn"> {{ btn-msg }} </a>
    </div>
</template>

<script>
export default {
  props: {
    btn-link: { 
      type: String,
      default: "",
      required: true
    },
    btn-msg: { 
      type: String,
      default: "Button",
      required: true
    },
  },
  name: 'IndexPage'
}
</script>

<style>
    .btn {
        background-color: var(--clr-blue);
        font-weight: 700;

        color: var(--clr-white);
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