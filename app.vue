<template>
  <div class="flex flex-row justify-between gap-10 px-20 mt-10">
    <div class="border w-1/2 rounded-lg p-5">
      <form action="">
        <div>
          <input type="text" v-model="firstName" placeholder="first name">
        </div>
        <div class="mt-3">
          <input type="text"  v-model="lastName" placeholder="last name">
        </div>
        <div class="mt-3">
          <input type="text" v-model="occupation" placeholder="occupation">
        </div>
        <div class="mt-3">
          <input type="text" v-model="gitRepo" placeholder="git repo">
        </div>
        <div class="mt-3">
          <input type="text" v-model="about" placeholder="about">
        </div>
      </form>
    </div> 
    <div class="border w-1/2 rounded-lg p-5">
      <div>
        Name: {{  firstName }} {{ lastName }}
      </div>
      <div>
        Occupation: {{ occupation }}
      </div>
      <div>
        Git: {{ gitRepo }}
      </div>
      <div>
        About: {{ about }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "Jamiu",
      lastName: "",
      occupation: "",
      gitRepo: "",
      about: "",
    }
  }
}
</script>

<style>
input {
  @apply border rounded-full
}
</style>