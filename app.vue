new Vue({
	el: '#app',
	data: {
		titulo : 'My Shopping List',
		frutas : [
		{nombre: 'Manzana',cantidad: 5},	
		{nombre: 'Pera',cantidad: 0},	
		{nombre: 'Durazno',cantidad: 9}
		],
		nuevafruta : '',
		total : 0 
	},
    methods:{
      agregarfruta (){
        this.frutas.push({
          nombre: this.nuevafruta, cantidad :1
        });
        this.nuevafruta='';
      },
      borrarfruta: function(index){
         this.frutas.splice(index, 1)
      },
    }
  
})