<!--
Vue App -> 2023 PG24Pedro pg24pedro@vfs.com
-->
<script>

    import Controller from '@/plugins/controller'

    class RecordEditViewController extends Controller {

        constructor( name, subComponentList = []) {
            super( name, subComponentList );
            this.vm = {
                name: 'Record Edit'
            }

            this.props = {
                name: String,
            }
        }
    }
    
    export default new RecordEditViewController('Record Edit')

</script>
<template>

    <section class="flexbox columns about">
        <h1 class="flexitem left title">Test View</h1>
        <div class="flexitem dialog">
            <div class="flexitem dialog">

                <div class="flexbox">
                    <p>Hello Record edit View</p>
                </div>

                <div class="flexitem">
                    
                </div>
            </div>
        </div>


    </section>

</template>
<style scoped>
</style>

