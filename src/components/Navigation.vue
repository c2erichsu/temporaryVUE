<template>
  <b-navbar toggleable="lg" type="light" variant="light" fixed="top">

    <b-navbar-brand><router-link to="/" id="navbar">{{ siteName }}</router-link></b-navbar-brand>

      <b-navbar-nav>
        <b-nav-item><router-link to="/catalog">{{catalog}}</router-link></b-nav-item>
        <b-nav-item><router-link to="/about">{{about}}</router-link></b-nav-item>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="鍵入題目名稱"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">搜尋</b-button>
        </b-nav-form>

        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template #button-content>
            <em>{{user}}</em>
          </template>
          <b-dropdown-item>{{signOut}}</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>

    
  </b-navbar>
</template>

<script>

export default {
  name: 'Navigation',
  components: {
  },
  data(){
    return{
      siteName: '樂讀Yuedo',
      catalog: '學科',
      paper: '考古題',
      about: '關於',
      user: '設置',
      signOut: '登出',
    }
  }
}

</script>

<style scoped>



</style>
