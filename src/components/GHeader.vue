<template>
  <q-header class="header">
    <q-toolbar class="toolbar text-white">
      <div class="row header-content">
        <div>
          <q-btn
            class="home-button"
            icon="fa-solid fa-house"
            round
            @click="$router.push('/')"
          />
        </div>
        <q-input
          rounded
          outlined
          v-model="search"
          class="search-bar"
          :placeholder="$t('search')"
        >
          <template v-slot:prepend>
            <q-icon class="search-icon" name="fa-solid fa-magnifying-glass" />
          </template>
        </q-input>
        <div class="absolute-right" style="padding-top: 10px">
          <q-btn
            class="user-button"
            icon="fa-regular fa-user"
            rounded
            outline
            no-caps
            :label="$t('default_user_name')"
          />
        </div>
      </div>
    </q-toolbar>
  </q-header>
</template>
<script>
export default {
  name: "GHeader",
  data() {
    return {
      leftDrawerOpen: true,
      search: null,
    };
  },
  publicarMusica() {},
  publicarPodcast() {},
};
</script>
<style lang="scss" scoped>
.header {
  background: #1e1e1e;
  padding: 5px;
}
.toolbar {
  background: #1e1e1e;
  height: 50px;
}

.header-content {
  margin: 20px 0;
}

.home-button {
  background-color: #525252;
  margin: 0 50px 0 30px;
}

.menuDropDown {
  color: #1e1e1e;
  font-size: 20px;
}

.search-icon {
  color: #ffff;
  font-size: 20px;
}

.search-bar {
  width: 50%;
  max-width: 500px;
  min-width: 500px;
  margin-right: 40px;
}

.user-button {
  margin: 0 30px;
}

:deep(.user-button.q-btn .q-icon) {
  font-size: 16px;
  padding: 4px;
  border: 1px solid white;
  border-radius: 15px;
}

:deep(.q-field) {
  height: 40px !important;
}

:deep(.q-field__native) {
  color: #525252;
  height: 40px !important;
  font-size: 16px;
}

:deep(.q-field--outlined) {
  height: 40px !important;
}

:deep(.q-field__control) {
  height: 40px !important;
}

:deep(.q-field__marginal) {
  height: 40px !important;
}

:deep(.q-field__control:before) {
  border: #525252 1px solid;
  transition: none;
}

:deep(.q-field__control:after) {
  border-width: 1px !important;
  transition: none;
}

:deep(.q-field__inner) {
  height: 40px !important;
}

:deep(.q-field--dense) {
  height: 40px !important;
}
</style>
