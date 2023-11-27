<script>
export default{
    data(){
        return{
            usernameContact:'',
            passwordContact:'',
            massageContact:''
        }
    },
    methods:{
        submit:function(){
            if(this.usernameContact===""|| this.passwordContact===''|| this.massageContact===""){
                alert('tolong masukkan input!!')
            }
            else{
                alert('berhasil!')
            }
        },
        cancel:function(){
            this.usernameContact=''
            this.passwordContact=''
            this.massageContact=''
            window.location.reload()
        }
    }
}
</script>

<template>
    <aside id="contact" class="w-full h-screen flex flex-col gap-2 justify-center items-center bg-black text-white px-20">
        <h3 class="text-3xl font-black capitalize">contact us</h3>
        <div class="contact w-3/4 p-2 flex flex-col">
            <div class="col mb-5">
                <label for="username" class="text-xl font-light mb-2">username</label>
                <input type="text" class="w-full px-3 py-2 bg-white" placeholder="username" v-model="usernameContact">
            </div>
            <div class="col mb-5">
                <label for="password" class="text-xl font-light mb-2">password</label>
                <input type="password" class="w-full px-3 py-2 " placeholder="password" v-model="passwordContact">
            </div>
            <div class="col mb-5">
                <label for="massage" class="text-xl font-light mb-2">massage</label>
               <textarea name="" id="" cols="30" rows="10" class="w-full h-3/4 px-2" placeholder="massage" v-model="massageContact"></textarea>
            </div>
            <div class="btn w-full flex justify-around items-center">
                <button @click="submit" class="bg-red-600 text-white p-2 rounded-lg" >submit</button>
                <button @clikc="cancel" class="bg-red-600 text-white p-2 rounded-lg" >cancel</button>
            </div>
        </div>
    </aside>
</template>