<template lang="pug">
  v-app#app
    v-app-bar#nav(
      light
      app
      absolute
    )
      a
        v-img(:src="require('@/assets/Logo_black.png')" height="36" max-width="250" contain)

      v-spacer

      v-toolbar-items
        v-btn(icon)
          v-icon mdi-google
        v-btn(icon)
          v-icon mdi-facebook
        v-btn(icon)
          v-icon mdi-linkedin

    div.bg
      v-container.mt-8
        v-row.justify-center.mt-16
          v-col(cols="8")
            v-img.mx-auto(:src="require('@/assets/Logo_black.png')" width="80%")

        v-row.justify-center.mt-8
          v-col.text-center(cols="12")
            strong(style="font-size:1.6rem;") Experience a hassle free application process with InternNet

        v-row.justify-center
          v-col(cols="12" md="4")
            .wrapper
              v-row
                v-col(cols="12")
                  v-img.mx-auto.mt-10(:src="require('@/assets/search.svg')" height="160" width="160")
                v-col.text-center(cols="12")
                  strong(style="font-size:1.6rem;") Search
                v-col.text-center(cols="12")
                  div.px-8(style="font-size:1rem; color:#777;") Search through many internship platforms(indeed, jobstreet, linkedin) at once with InternNet.
          v-col(cols="12" md="4")
            .wrapper
              v-row
                v-col(cols="12")
                  v-img.mt-10.mx-auto(:src="require('@/assets/apply.svg')" height="160" width="160")
                v-col.text-center(cols="12")
                  strong(style="font-size:1.6rem;") Apply
                v-col.text-center(cols="12")
                  div.px-8(style="font-size:1rem; color:#777;") You can choose to either apply through platforms outside or directly with the company directly.
          v-col(cols="12" md="4")
            .wrapper
              v-row
                v-col(cols="12")
                  v-img.mt-10.mx-auto(:src="require('@/assets/plan.svg')" height="160" width="160")
                v-col.text-center(cols="12")
                  strong(style="font-size:1.6rem;") Manage
                v-col.text-center(cols="12")
                  div.px-8(style="font-size:1rem; color:#777;") Mange your many applications with easy to use interface and flexible way of storing information.
      
        v-row.mt-4.justify-center
          v-col(cols="8" style="display:flex;").text-center
            v-text-field.mr-4(hide-details label="email" v-model='email' outlined color="#E82735" style="width:50% !important; background-color:#fff;")
            v-btn(color="#1C5DAB" dark x-large) Early Access

        v-row.justify-center.mt-10
          v-col(cols="12")
            div Icons made by 
              a(href="https://www.flaticon.com/authors/freepik" title="Freepik") Freepik 
              | from 
              a(href="https://www.flaticon.com/" title="Flaticon") www.flaticon.com
</template>

<script>
export default {
  name: 'App',

  data: () => ({
    email: ''
  }),
};
</script>

<style>
.bg {
  /* background: url('~@/assets/pattern.svg') #f8f8f8; */
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #3c3b37;
  /* overflow-x: hidden; */
}

.wrapper:hover {
  box-shadow: 0 2px 40px #e0e5f0;
  transform: translateY(-3px);
  background-color: #fff;
  cursor: pointer;
}

.wrapper {
  transition: all .3s cubic-bezier(.77,0,.175,1);
  border: 1px solid #d9e1e6;
  background-color: #fff;
}

#nav {
  background-color: #fff;
}
</style>
