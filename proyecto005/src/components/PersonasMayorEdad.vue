<script>
    export default {
        data() {
            return {
                personas: [
                    {
                        nombre: 'Jose', 
                        edad: 12
                    },{
                        nombre: 'Ana', 
                        edad: 43
                    },{
                        nombre: 'Pedro', 
                        edad: 4
                    },{
                        nombre: 'María', 
                        edad: 12
                    }
                ]
            }
        }
    }
</script>

<template>
    <ul>
        <template v-for="persona in personas">
            <li>
                {{ persona.nombre }}
                <span v-if="persona.edad>=18">(Mayor)</span>
                <span v-else>(Menor)</span>
            </li>
        </template>
    </ul>
</template>