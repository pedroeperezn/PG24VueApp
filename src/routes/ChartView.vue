<!--
VFS VUE Single File Component
Copyright (c) 2018-2023. Scott Henshaw All Rights Reserved.
-->

<!--
Vue App -> 2023 PG24Pedro pg24pedro@vfs.com
-->

<script>

    import Controller from '@/plugins/controller'

    class ChartViewController extends Controller {

        constructor( name, subComponentList = []) {
            super( name, subComponentList );
            this.vm = {
                name: 'Chart View'
            }

            this.props = {
                name: String,
            }
        }
    }
    
    export default new ChartViewController('Chart')

</script>
<template>

    <section class="flexbox columns about">
        <h1 class="flexitem left title">Chart View</h1>
        <div class="flexitem dialog">
            <div class="flexitem dialog">

                <div class="flexbox">
                    <p>Hello Chart View</p>
                </div>

                <div class="flexitem">
                    
                </div>
            </div>
        </div>


    </section>

</template>
<style scoped>
</style>

