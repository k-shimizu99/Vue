<template>
  <div>{{id}} {{title}} {{image}}  {{description}}</div>
</template>

<script>
// import { numberLiteralTypeAnnotation } from '@babel/types';
// import { stringify } from 'querystring';

export default {
    props: {
        id: Number,
        title: String,
        image: String,
        description: String
    }

}
</script>

<style>

</style>