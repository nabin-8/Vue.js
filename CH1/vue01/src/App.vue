<script setup>
import { ref } from 'vue'
// const firstname = ref('Nabin')
// const lastname = ref('Acharya')
// const myFavNumber = ref(7)

let count = ref(0)

// component form handler
const formHandler = (username, email, password) => {
  console.log('username', username)
  console.log('email', email)
  console.log('password', password)
}

// import HelloWorld from './components/HelloWorld.vue'
// import GlobalStyle from './components/GlobalStyle.vue'
// import LocalStyle from './components/LocalStyle.vue'
// import CombinedStyle from './components/CombinedStyle.vue'
// import ModuleStyle from './components/ModuleStyle.vue'
// import MyEvents from './components/MyEvents.vue'
// import MyReactiveComponent from './components/MyReactiveComponent.vue'
// import MyRefComponent from './components/MyRefComponent.vue'
// import ComputedProperties from './components/ComputedProperties.vue'
// import ConditionalRendering from './components/ConditionalRendering.vue'
// import ListRendering from './components/ListRendering.vue'
// import vforTwoWayDataBynding from './components/vforTwoWayDataBynding.vue'
// import StaticProps from './components/StaticProps.vue'
// import DynamicProps from './components/DynamicProps.vue'
// import PropValidation from './components/PropValidation.vue'
// import ComplexProps from './components/ComplexProps.vue'
// import CustomValidator from './components/CustomValidator.vue'
import ComponentEvent from './components/ComponentEvent.vue'
</script>

<!-- <GlobalStyle />
<LocalStyle />
<CombinedStyle />
<ModuleStyle /> -->
<!-- <MyEvents /> -->
<!-- <MyReactiveComponent /> -->
<!-- <MyRefComponent /> -->
<!-- <ComputedProperties /> -->
<!-- <ConditionalRendering /> -->
<!-- <ListRendering /> -->
<!-- <vforTwoWayDataBynding /> -->
<!-- <StaticProps name="Nabin" /> -->
<!-- <DynamicProps :firstname="firstname" :lastname="lastname" :myFavNumber="myFavNumber" /> -->
<!-- <PropValidation :age="20" /> -->
<!-- <ComplexProps
  :friends="['alex', 'john', 'nabin', 'huxn']"
  :userInfo="{ name: 'alex', age: 26, location: ['Earth', 'KTM'] }"
/> -->
<!-- <CustomValidator name="random" :age="22" password="impoissblepassword" /> -->
<template>
  <h1>Count: {{ count }}</h1>
  <ComponentEvent @incrementCounter="count++" @userInfo="formHandler" />
</template>
