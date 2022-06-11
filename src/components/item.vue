<template>
  <div class="card">
      <h1>

        <a :href="item.href"
        >  
          <img :src="item.img" alt="Icono de servicio" />

          <span>   {{item.titulo}} </span>

        </a>
        
          
      </h1>
  </div>
</template>

<script>
export default {
props: ['item']
}
</script>



<style scoped>
div{
  margin: 20px 50px 20px 50px;
  display: block;
  width: 100px;

}
img{
  width: 70px;

}
span{
  font-weight: 900;
}
 .card{
   display: flex;
   justify-content: center;
   flex-direction: column;
   min-width: 120px;
   min-height: 150px;
   border: 1px solid grey;
   border-radius: 5%;
   box-shadow: 0 0 2em grey;
   opacity: .9;
   transition: box-shadow .5s;

 }

 .card:hover{
   opacity: 1;

   box-shadow: 0 0 4em grey;
 }

</style>>

