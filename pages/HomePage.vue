<template>
    <div class="min-h-screen bg-black-ui text-white-ui box pb-6 gap-y-6">
        <Header class="col-start-1 col-end-12 " />
        <div class="max-w-6xl mx-auto px-4 col-start-1 col-end-12 w-full flex justify-between gap-x-6 relative">
            <AsideHomeMenu />
            <div class="flex flex-col justify-between mr-auto">
                <div>
                    <h1 class="text-5xl">Agenda del Día</h1>
                    <h2 class="text-xl">{{today}}</h2>
                </div>
                <div class="flex gap-x-4 mbCustom">
                   <StatusCard title="Pendientes" detail="120" />
                   <StatusCard title="En Curso" detail="72" />
                   <StatusCard title="Cerrados" detail="204" />
                  
                </div>
            </div>
            <div>
              <no-ssr>
                  <date-picker class="text-primary-1" :inline="true" />
              </no-ssr>


            </div>
            <button class="absolute right-0 bottomCustom bg-secondary-2 rounded-full w-12 h-12 font-light text-xl  "><p class="flex justify-center items-center w-full h-full">+</p></button>
        </div>
    </div>
</template>


<style>
.box{
    display: grid;
    grid-template-columns: repeat(11, minmax(0, 1fr));
    grid-template-rows: max-content 1fr;
}

.mbCustom{
    margin-bottom: 20%;
}
.bottomCustom{
    bottom: 10%;
}
</style>

<script>
import moment from "moment"
const date = moment().locale("es").format("dddd DD MMMM [de] YYYY");



export default {
    data() {
        return {

            today: date
        }
        
    },
}
</script>