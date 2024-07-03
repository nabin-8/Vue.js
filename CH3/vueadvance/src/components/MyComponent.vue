<script setup>
// const vFormatDiv={
//   mounted:(el, binding)=>{
//     // console.log(el)
//     // el.style.fontSize=binding.value+'px'
//     // console.log(binding)
//     // el.style.color='red'
//     // // el.style.fontStyle='4rem'
//     // console.log(binding.arg)
//
//   //   changing color
//     switch (binding.arg){
//       case 'orange':
//         el.style.color='orange'
//         break;
//       case 'pink':
//         el.style.color='pink'
//         break;
//       case 'purple':
//         el.style.color='purple'
//         break;
//
//       default:
//         el.style.color='black'
//     }
//   }
// }

const vFormateDiv=(el)=>el.style.fontSize='55rem'
</script>

<template>
<!--  <div v-format-div="100">Using custom v binding</div>-->
<!--  passing arguments-->
  <div v-formate-div>Using custom v binding</div>
</template>
