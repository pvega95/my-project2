<template>
<v-container >

<v-layout justify-center>
  <v-flex xs5>
    <div>
      <img src="../images/ScotiabankLogo.png">
    </div>  
  </v-flex>
</v-layout>
<v-layout justify-center>
<v-flex xs5>
<v-form v-model="valid" lazy-validation>
    <v-text-field
      v-model="name"
      :rules="nameRules"
      :counter="10"
      label="Name"
      required
    ></v-text-field>
    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
    ></v-text-field>
  </v-form>
</v-flex>
</v-layout>
 
  <v-btn color="green" type="submit">Sign Up</v-btn>
  
</v-container>
 
</template>

<script>
  export default {
    data: () => ({
      valid: false,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => v.length <= 10 || 'Name must be less than 10 characters'
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid'
      ]
    })
  }
</script>
