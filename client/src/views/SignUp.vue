<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout column align-center>
      <v-form v-model="valid">
          <v-text-field
            v-model="user.username"
            :rules="notEmptyRules"
            label="Username"
            required
          ></v-text-field>
          <v-text-field
            v-model="user.displayName"
            :rules="notEmptyRules"
            label="Display Name"
            required
          ></v-text-field>
          <v-text-field
            v-model="user.password"
            :rules="notEmptyRules"
            label="password"
            type="password"
            required
          ></v-text-field>
          <v-text-field
            v-model="user.confirmPassword"
            :rules="notEmptyRules"
            label="Confirm Password"
            type="password"
            required
          ></v-text-field>
          <v-text-field
            v-model="user.imageURL"
            :rules="notEmptyRules"
            label="Image Url"
            required
          ></v-text-field>
      </v-form>
      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>


<script>
export default{
  name: 'signup',
  data: () => ({
    user: {
      username: '',
      password: '',
      confirmPassword: '',
      displayName: '',
      imageURL: '',
    },
  }),
};
</script>
