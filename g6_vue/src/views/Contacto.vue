<template>
    <div class="contenedorTotal">
        <header class="contenedorHeader">
            <img class="contenedorHeader__imgLogo" src="../images/Logo.png" alt="">
            <div class="contenedorHeader__banner">
                <div class="contenedorHeader__filtro">
                    
                    <nav class="contenedorHeader__navegacion">
                        <router-link to="/">Inicio</router-link>
                        <router-link to="/login">Login</router-link>
                    </nav>
        
                    <h1>Universidad de las Tecnologias TIC</h1>
                </div>
    
            </div>
        </header>

        <h2 id="divTitulo"> Formulario de Contacto</h2>
        <form class="formulario__contenedor" action="#" target="" method="get" name="formDatosPersonales">
            <div class="formulario">       
                <label for="nombre">Nombre</label>
                <input type="text" name="nombre" id="nombre" placeholder="Escribe tu nombre" v-model="nombre" />

                <label for="apellidos">Apellidos</label>
                <input type="text" name="apellidos" id="apellidos" placeholder="1r Apellido" v-model="apellidos" />

                <label for="email" >Email</label>
                <input type="email" name="email" id="email" placeholder="email" required v-model="email"/>

                <label for="mensaje">Comentarios</label>
                <textarea name="mensaje" for="mensaje" placeholder="describe brevemente en menos de 300 carácteres" maxlength="300" v-model="comentarios"></textarea>
            </div>
            <div>
                    <!-- <input type="submit" name="enviar" value="enviar datos" /> -->
                    <button @click.prevent="enviarDatos" >Enviar</button>
            </div>
        </form>

        <footer>
            <!-- <img src="images\Banner.png" alt="Pie de pagina"> -->
            <div class="contenedorFooter">
                <div class="contenedorFooter__banner">
                    <nav class="navegacion-footer">
                        <router-link to="/">Inicio</router-link>
                        <router-link to="/login">Login</router-link>
                    </nav>
                </div>
            </div>
        </footer>
    </div>
</template>

<script>
import ContactoService from "@/services/contacto.js";
export default {
    data() {
        return {
            nombre:'',
            apellidos:'',
            email:'',
            comentarios:'',
            infoContacto:{"nombre":'',
                            "apellido":'',
                            "email":'',
                            "comentario":''}
        }
    },
    methods:{
        enviarDatos(){
            if (this.nombre === '""' || this.apellidos === '' || this.email === '') {
                alert('Porfavor asegurese de entrar todos los datos')
            } else {
                this.infoContacto.nombre=this.nombre;
                this.infoContacto.apellido=this.apellidos;
                this.infoContacto.email=this.email;
                this.infoContacto.comentario=this.comentarios;

                ContactoService.guardar(this.infoContacto).then((respuesta)=>{
                    if(respuesta){
                        alert('Sus datos han sido guardados en la base de datos');
                        this.nombre='';
                        this.apellidos='';
                        this.email=''
                        this.comentarios=''
                    }
                })
                //console.log(this.infoContacto);


                
            }
            
        }
    }
}
</script>


<style scoped>

.contenedorTotal {
    width: 1140px;
    margin:0 auto;
}

/** Header **/
.contenedorHeader {
	
	background-image: url(../images/banner.jpeg);
	height: 280px;
	background-size: cover;
	background-repeat: no-repeat;
	background-position: center center;
	display: grid;
	grid-template-columns: 280px 860px;
}

.contenedorHeader__imgLogo {
	height: 280px;
	width: 280px;
}

.contenedorHeader__banner {

	position: relative;
}
.contenedorHeader__filtro {
	position: absolute;
	background-color: rgba(0, 0, 0, 0.7);
	width: 100%;
	height: 100%;
}
.contenedorHeader__banner h1 {
	text-align: center;
	margin-top: 120px;
	color: white;
	
}
.contenedorHeader__navegacion {
	display: flex;
	gap: 2rem;
	justify-content: right;
	margin-top: 50px;
	margin-right: 50px;
	
	
}
.contenedorHeader__navegacion a {
	
	color: white;
	text-decoration: none;
}


        * {
            box-sizing: border-box;
        }

        .formulario__contenedor {
            width: 300px;
            margin: 0 auto;
            display: grid;

        }
        
        .formulario {
            width: 300px;
            padding: 16px;
            border-radius: 10px;
            margin: auto;
            background-color:#E5E0DC;
        }
        
        form label {
            width: 72px;
            font-weight: bold;
            display: inline-block;
        }
        
        form input[type="text"],
        form input[type="email"] {
            width: 180px;
            padding: 3px 10px;
            border: 1px solid #f6f6f6;
            border-radius: 3px;
            background-color: #f6f6f6;
            margin: 8px 0;
            display: inline-block;
        }
        
        form input[type="submit"] {
            
            padding: 8px 16px;
            margin-top: 32px;
            border: none;
            border-radius: 5px;
            display: block;
            color: #206A64;
            text-transform: uppercase;
            background-color: #E5E0DC;

        }
        
        form input[type="submit"]:hover {
            cursor: pointer;
        }
        
        textarea {
            width: 100%;
            height: 100px;
            border: 1px solid #f6f6f6;
            border-radius: 3px;
            background-color: #f6f6f6;
            margin: 8px 0;
            /*resize: vertical | horizontal | none | both*/
            resize: none;
            display: block;
        }
        
        #divTitulo {
            height: 25px;
            width: max-content;
            margin: 0 auto;
            color: rgb(7, 7, 7);
            text-align: center;
            font-weight: bold;
            /* background-color: rgb(247, 245, 246); */
            font-size: x-large;
            margin-top: 30px;
            margin-bottom: 20px;
        }
        div button {
            margin-top: 1rem;
        }


    /** Footer **/
    .contenedorFooter {
    margin-top: 20px;
    background-image: url(../images/banner.jpeg);
    height: 100px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    position: relative;

    }

    .contenedorFooter__banner {
    position: absolute;
    background-color: rgba(0, 0, 0, 0.7);
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content:right;

    }
    .navegacion-footer {
    display: flex;
    gap: 2rem;
    padding-right: 2rem;
    }
    .navegacion-footer a {

    color: white;
    text-decoration: none;
    }
</style>

