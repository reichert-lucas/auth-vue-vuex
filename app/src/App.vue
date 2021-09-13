<template>
	<div id="app">
		<barra-navegacao/>
		<router-view/>
	</div>
</template>
<script>
	import BarraNavegacao from '@/components/BarraNavegacao'
    export default {
        components: {
			'barra-navegacao': BarraNavegacao
		}

    }
</script>
<style>
.navbar {
  background: #2791ae;
}
.navbar-bytebank a {
  color: #fff;
}
.navbar-bytebank a:hover {
  color: #000;
}
</style>
