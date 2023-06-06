<!--
VFS VUE Single File Component
Copyright (c) 2018-2023. Scott Henshaw All Rights Reserved.
-->
<script>

    import Controller from '@/plugins/controller'

    class AdminViewController extends Controller {

        constructor( name, subComponentList = []) {
            super( name, subComponentList );
            this.vm = {
                name: 'Admin View'
            }

            this.props = {
                name: String,
            }
        }
    }
    
    export default new AdminViewController('Admin')

const TRECEvent = 
{
    DEATH: 0, //Triggered in game when dead
    JUMP_SUCCESS: 1,
    RESPAWN: 2,
    WEAPON_pICKUP: 3
    
}

function EventsToString(theEventEnum)
{
    let name = ""
    switch(theEventEnum){
        case TRECEvent.DEATH:
            name="Death";
            break;
        default:
        break
    }
}

const TRECAction = {
    IDLE: 0,
    WALKING: 1,
    RUNNING: 2,
    SHOOTING: 3
}

const TRex = {
    sessionID: 0,   //gAME BUILD
    deltaTime: 20, //SECONDS SINCE LEVEL START
    position: { x: 0, y: 0, z: 0 }, //PLAYERS LOCATION AT TIME EVENT
    heading: { x: 0, y: 0, z: 0 }, //PLAYERS LOCATION AT TIME EVENT
    eventId: TRECAction.RESPAWN, //WHAT HAPPENED
    actionId: TRECAction.IDLE,
    

}

const recordList = [];
    for (let i = 0; i < 3; i++)
        recordList[i] = TRex;

const OneLine = ( aRec ) =>
{
    var theLine =  `@${aRec.deltaTime}`
    theLine += `Player @${aRec.position.x},@${aRec.position.z}`
    theLine += `${EventsToString(aRec.eventId)}`

    return theLine
}

</script>
<template>

    <section class="flexbox columns about">
        <h1 class="flexitem left title">Single Telemetry Record Admin</h1>
        <div class="flexitem dialog">
            <div class="flexitem dialog">

                <div class="flexbox">
                    <ul class="flexitem">
                        <li v-for="(rec,i) in recordList" :key="i">
                            <span>{{OneLine(rec)}}</span> 
                            <button>Edit</button>
                        </li>
                    </ul>
                </div>

                <div class="flexitem">
                    <form>
                        <label for="speed">Speed</label>
                        <input name="speed" type="number" />
                        <input name="speed" type="number" />
                        <label for="speed">Speed</label>
                    </form>
                </div>
            </div>
        </div>


    </section>

</template>
<style scoped>
</style>

