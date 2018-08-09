<template>
  <div>

    <div class="form-group">
      <label>Name</label>
      <input
        type="text"
        class="form-control"
        v-model="localUser.firstName">
    </div>

    <div class="form-group">
      <label>Surname</label>
      <input
        type="text"
        class="form-control"
        v-model="localUser.lastName">
    </div>

    <div class="form-group">
      <label>Balance</label>
      <input
        type="text"
        class="form-control"
        v-model="localUser.balance">
    </div>

    <div class="form-group">
      <label>Phone</label>
      <input
        type="text"
        class="form-control"
        v-model="localUser.phone">
    </div>

    <div class="form-group">
      <label>Address</label>
      <input
        type="text"
        class="form-control"
        v-model="localUser.address">
    </div>

    <div class="form-group">
      <label>Company</label>
      <input
        type="text"
        class="form-control"
        v-model="localUser.company">
    </div>

  </div>
</template>

<script>
export default {
  name: 'UserForm',
  props: {
    // Объект с данными пользователя
    user: {
      type: Object,
      required: true
    }
  },
  data: () => ({
    // Локальный изменяемый объект пользователя
    localUser: null
  }),
  watch: {
    // При изменении локального состояния
    // отправляем объект наверх
    localUser: {
      deep: true,
      handler() {
        this.$emit('input', this.localUser)
      }
    }
  },
  created() {
    // Копируем пользователя в локальное состояние
    this.localUser = Object.assign({}, this.user)
  }
}
</script>