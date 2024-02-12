<template>
    <button>{{text}}</button>
</template>
<script setup>
   const props= defineProps({
     props:{
        text:{
            default:'No value available'
        }
     }  
   })
</script>
<!-- <script>
  export default{
    props:{
        text:{
            default:'No value available'
        }
    }   
  }

</script>    -->