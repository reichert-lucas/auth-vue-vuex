<template>
    <nav class="navbar navbar-expand-lg navbar-bytebank mb-4">
      <a class="navbar-brand" href="#">ByteBank</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        
        <barra-navegacao-logado-menu v-if="usuarioEstaLogado"/>
        <barra-navegacao-deslogado-menu v-else/>
		
      </div>
    </nav>
</template>
<script>
import BarraNavegacaoLogadoMenu from './BarraNavegacaoLogadoMenu'
import BarraNavegacaoDeslogadoMenu from './BarraNavegacaoDeslogadoMenu'
import { mapGetters } from 'vuex'

export default {
    computed: { 
      ...mapGetters(['usuarioEstaLogado'])
    },
    components: {
        'barra-navegacao-logado-menu': BarraNavegacaoLogadoMenu,
        'barra-navegacao-deslogado-menu': BarraNavegacaoDeslogadoMenu,
    }
}
</script>
<style>
    
</style>