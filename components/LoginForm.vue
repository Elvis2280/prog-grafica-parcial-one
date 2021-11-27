<template>
   <FormulateForm 
   name="crearCuenta"
   @input="crearCuenta"
   @submit="submit">
        <div class="flex flex-col">
            <!-- <input class="border-2 text-primary-3 focus:text-primary-1 rounded border-secondary-3 focus:border-secondary-2 transition duration-300 h-9 outline-none px-2" type="email"> -->
       <FormulateInput

      name="userEmail"
      type="email"
      label="Usuario"
      input-class="border-2 text-primary-3 focus:text-primary-1 rounded border-secondary-3 focus:border-secondary-2 transition duration-300 h-9 outline-none px-2 w-full"
         />

        </div>
        <div class="flex flex-col mt-3">
             <FormulateInput
             name="userPassword"
      type="password"
      label="Contraseña"
      input-class="border-2 text-primary-3 focus:text-primary-1 rounded border-secondary-3 focus:border-secondary-2 transition duration-300 h-9 outline-none px-2 w-full"
    />
        </div>

       <div class="mt-3">
            <button  type="submit" class=" bg-secondary-2 px-3 py-2 w-full rounded hover:bg-secondary-1 hover:text-white-ui  transition duration-300">Ingresar a Cuenta</button>
        <button class="mt-3 text-primary-3 text-center w-full">¿Olvidaste tu Contraseña?</button>
       </div>
   </FormulateForm>
</template>

<script>
import { getAuth, signInWithEmailAndPassword } from "firebase/auth";

    
 




export default {
    methods:{
        crearCuenta(){
        this.$formulate.handle({
        inputErrors: { userEmail: 'Ingrese un email valido'},
        
      }, 'crearCuenta')
        },
        submit(data){
        const auth = getAuth();
        signInWithEmailAndPassword(auth, data.userEmail, data.userPassword)
        .then((userCredential) => {
         // Signed in
            const user = userCredential.user;
            console.log(user)
            this.$router.push({path: '/HomePage'});
    // ...
  })
  .catch((error) => {
    console.log(error.message)
  });
        
        }
    }
    
}
</script>