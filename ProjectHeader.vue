<template>
  <header>
    <div class="bg-[#efc432] p-4">
      <p>
        <b>¡The Nut House llegó a Amazon!</b> Pide tu<b>producto</b>preferido.
      </p>
    </div>
    <div class="flex justify-center border-b-2 p-7">
      <img src="@/assets/logo.jpg" alt="" />
    </div>
    <div class="flex justify-around p-5 flex-row">
      <router-link to="/the-nut-house">The Nut House</router-link>
      <router-link to="/fun-fruit">Fun Fruit</router-link>
      <router-link to="/productos-a-granelalt">Productos a granelalt</router-link>
      <router-link to="/acercade-fun">Acercade Fun Fruit</router-link>
      <router-link to="/fundacion-vue">Fundación</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "ProjectHeader",
}
</script>

<style></style>