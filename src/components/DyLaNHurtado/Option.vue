
<template>
	<div class="w-full h-full flex items-center justify-center">
		<input type="checkbox" :id="'checkbox'+icon"  class="hidden peer">
        <label :for="'checkbox'+icon" class=" p-5 w-full flex items-center justify-center text-gray-500 bg-white rounded-lg border-2 border-gray-200 cursor-pointer dark:hover:text-gray-300 dark:border-gray-700 peer-checked:border-cyan-500 hover:text-gray-600 dark:peer-checked:text-gray-300 peer-checked:text-gray-600 hover:bg-gray-50 dark:text-gray-200 dark:bg-gray-600 dark:hover:bg-gray-500">                           
            <div class="flex justify-center items-center flex-col w-full">
               <UpperIcon v-if="icon==1"/>
               <LowerIcon v-else-if="icon==2"/>
               <NumbersIcon v-else-if="icon==3"/>
               <SymbolsIcon v-else/>
                <div class="w-full text-sm mt-2">{{sum}}</div>
            </div>
        </label>
	</div>
		
</template>
<script>
import SymbolsIcon from './icons/symbols-icon.vue';
import UpperIcon from './icons/uppercase-icon.vue';
import LowerIcon from './icons/lowercase-icon.vue';
import NumbersIcon from './icons/numbers-icon.vue';
export default{
		name:'Option',
		props:{
			icon:String,
			sum:String
		},
		components:{
			SymbolsIcon,UpperIcon,LowerIcon,NumbersIcon
		}
	}
</script>
