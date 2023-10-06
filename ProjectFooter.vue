<template>
  <footer>
    <div class="flex justify-around bg-[#1c3d79] mt-20 p-6">
      <div class="block">
        <h1 class="text-white mt-8">FUNFRUIT EN TU BANDEJA DE ENTRADA</h1>
        <p class="text-white mt-8">
          Regístrate para recibir ofertas y nuevo contenido de<b>FUNFRUIT.</b>
        </p>
        <input
          class="bg-[#1c3d79] border mt-4 py-6 rounded-lg w-full"
          type="email"
          placeholder="Ingresa tu email"
          name=""
        />
        <div class="flex text-white justify-around mt-8 gap-4">
          <a href="">
            <p>Aviso de privacidad</p>
          </a>
          <a href="">
            <p>Términos y condiciones</p>
          </a>
          <a href="">
            <p>©FUNFRUIT 2020</p>
          </a>
        </div>
      </div>
      <div class="block text-white">
        <a href="">
          <p class="mt-8">Contactanos</p>
        </a>
        <a href="">
          <p class="mt-8">Unete a nuestro equipo</p>
        </a>
        <a href="">
          <p class="mt-8">Blog</p>
        </a>
        <div class="flex justify-around mt-8">
          <a href=""><img src="@/assets/facebook.svg" alt="" /></a>
          <a href=""><img src="@/assets/instagram.svg" alt="" /></a>
          <a href=""><img src="@/assets/twitter.svg" alt="" /></a>
        </div>
        <div class="mt-8 text-[#fff]">
          <p>Powered by conceptHaus</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "ProjectFooter",
};
</script>

<style></style>
