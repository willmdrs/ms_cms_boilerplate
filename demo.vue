<template>
  <div :class="(_ms.configuracoes.cores.escuro.secundaria ? 'text-white' : 'text-black')">
    <div class="row bg-indigo-9 q-py-md">
      <div class="col-md-4 offset-md-4">
        <slot name="site.logotipo" classes="full-width"></slot>
      </div>
      <div class="col-md-12">
        <slot name="menu" orientacao="horizontal" tipo="botoes" cor="white" nome="Principal"></slot>
      </div>
    </div>
    <div class="q-pa-md">
      <div class="rounded-borders bg-grey-9 q-pa-md">
        <slot name="pagina.titulo"></slot>
        <slot name="pagina.conteudo"></slot>
      </div>
    </div>
  </div>
</template>
<style lang="stylus">
  body
    background #212121
  h1
    font-weight 600
</style>
<script>
module.exports = {
  /* NÃO ALTERE ABAIXO */
  props: {
    _ms: {
      type: Object,
      required: true
    }
    // eslint-disable-next-line comma-dangle
  }
  /* NÃO ALTERE ACIMA */
}
</script>
