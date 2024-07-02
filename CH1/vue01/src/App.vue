<script setup>
// import { ref } from 'vue'
// const firstname = ref('Nabin')
// const lastname = ref('Acharya')
// const myFavNumber = ref(7)

// let count = ref(0)

// // component form handler
// const formHandler = (username, email, password) => {
//   console.log('username', username)
//   console.log('email', email)
//   console.log('password', password)
// }

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
// import ComponentEvent from './components/ComponentEvent.vue'
// import slotComponent from './components/slotComponent.vue'
// import FallBackContentSlot from './components/FallBackContentSlot.vue'
import NamedSlot from './components/NamedSlot.vue'
import DefaultSlote from './components/DefaultSlote.vue'
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
<!-- <h1>Count: {{ count }}</h1>
<ComponentEvent @incrementCounter="count++" @userInfo="formHandler" /> -->
<!-- <slotComponent>
  <h1>Content 1</h1>
  <h1>Content 2</h1>
</slotComponent> -->
<!-- <FallBackContentSlot> </FallBackContentSlot>
<FallBackContentSlot>
  <p>
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sequi, accusantium vel nesciunt
    eligendi delectus, quasi minima temporibus omnis iusto voluptatibus in dolor debitis quod
    error a esse consequuntur? Odio, inventore!
  </p>
</FallBackContentSlot> -->
<template>
  <NamedSlot>
    <!-- V-slot:one -->
    <template v-slot:one>
      <h1>This content will go to slot "one"</h1>
    </template>

    <!-- #two -->
    <template #two>
      <h1>This content will go to slot "two"</h1>
    </template>
  </NamedSlot>

  <!-- default slote -->
  <DefaultSlote>
    <template #default>
      <h1>This is random slot</h1>
    </template>
  </DefaultSlote>
</template>
