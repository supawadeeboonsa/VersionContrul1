<template>
<<<<<<< HEAD

=======
<<<<<<< HEAD
>>>>>>> thai-lang
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    >
  </q-page>
</template>

<script setup>
//
<<<<<<< HEAD



=======
=======
>>>>>>> thai-lang
  <div class="q-pa-md" style="max-width: 400px">

    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
    >
      <q-input
        filled
        v-model="name"
<<<<<<< HEAD
<<<<<<< HEAD
        label="Your name fgdfsgfdgsfdgsdg *"
        hint="baiporrrrrrr379"
=======
        label="Your name dsfgsdgsdfgsfd *"
        hint="Name and surname"
>>>>>>> thai-lang

        label="ชื่อ-สกุล สุภาวดี บูญสา 379*"
        hint="ชื่อและนามสกุล supawadee boonsa 379"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type somethingawdawd']"
=======
        label="ชื่อ-สกุล379 *"
        hint="ชื่อและนามสกุล379"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'กรุณาพิมพ์ชื่อ']"
>>>>>>> thai-lang
      />

      <q-input
        filled
        type="number"
        v-model="age"
<<<<<<< HEAD

        label="อายุ: *"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'กรุณากรอกอายุของคุณนะคะwadwadwada',
          val => val > 0 && val < 100 || 'กรุณากรอกอายุที่ถูกต้องนะจ๊ะ'

        label="อายุ *"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'Please type your age',
          val => val > 0 && val < 100 || 'Please type a real age'
=======
        label="อายุ *"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'กรุณาใส่อายุ',
          val => val > 0 && val < 100 || 'กรุณาใส่อายุจริง'
>>>>>>> thai-lang
        ]"
      />

      <q-toggle v-model="accept" label="I accept the license and terms" />

      <div>
<<<<<<< HEAD

        <q-btn label="Submit" type="submit" color="primary"/>
        <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />

=======
>>>>>>> thai-lang
        <q-btn label="ยืนยัน" type="submit" color="primary"/>
        <q-btn label="เริ่มใหม่" type="reset" color="primary" flat class="q-ml-sm" />
      </div>
    </q-form>

  </div>
</template>

<script>
import { useQuasar } from 'quasar'
import { ref } from 'vue'

export default {
  setup () {
    const $q = useQuasar()

    const name = ref(null)
    const age = ref(null)
    const accept = ref(false)

    return {
      name,
      age,
      accept,

      onSubmit () {
        if (accept.value !== true) {
          $q.notify({
            color: 'red-5',
            textColor: 'white',
            icon: 'warning',
            message: 'You need to accept the license and terms first'
          })
        }
        else {
          $q.notify({
            color: 'green-4',
            textColor: 'white',
            icon: 'cloud_done',
            message: 'Submitted'
          })
        }
      },

      onReset () {
        name.value = null
        age.value = null
        accept.value = false
      }
    }
  }
}
<<<<<<< HEAD

=======
>>>>>>> thai-lang
>>>>>>> thai-lang
</script>
