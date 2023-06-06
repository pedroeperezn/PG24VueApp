<!--
Vue App -> 2023 PG24Pedro pg24pedro@vfs.com
-->
<script>

    import Controller from '@/plugins/controller'
    import BarChart from '@/components/BarChart.vue'

    class TestViewController extends Controller {

        constructor( name, subComponentList = []) {
            super( name, subComponentList );
            this.vm = {
                name: 'Test View'
            }

            this.props = {
                name: String,
            }
        }
    }
    
    export default new TestViewController('Test')

    

</script>
<template>

    <section class="flexbox columns about">
        <h1 class="flexitem left title">Test View</h1>
        <div class="flexitem dialog">
            <div class="flexitem dialog">

                <div class="flexbox">
                    <p>Hello Test View</p>
                </div>

                <div class="flexitem">
                    
                </div>
            </div>
        </div>
    </section>

    <BarChart />

</template>
<style scoped>
</style>

