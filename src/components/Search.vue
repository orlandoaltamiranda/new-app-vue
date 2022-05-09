<template>
  <div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="button-addon2">
  <button class="btn btn-outline-secondary" type="button" id="button-addon2" @click="searchMovie()">Button</button>
</div>
</template>

<script>
export default {
  name: 'Search',

methods: {
  searchMovie(){
    console.log('Hola')
  }
},
}


</script>

<style>

</style>


    // contenido.innerHTML = ""
    // const busquedaUsuario = document.getElementById("basic-addon2").value;

    //     console.log(personajes);
    //     if ((!/^[a-zA-Z]*$/g.test(busquedaUsuario))) {
    //         alert("Solo admite letras")
    //         contenido.innerHTML = '<h1 class="text-center">No hay resultados</h1>'
    //     }else {
    //         const nombrePersonaje = busquedaUsuario.toLowerCase();

    //         const resultados = personajes.filter(personaje => {
    //             const resultado = personaje.title.toLowerCase();
    //             return resultado == "" ?  lista(productos) : resultado.includes(nombrePersonaje);
    //         })
    //         mostrar(resultados)
    //     }