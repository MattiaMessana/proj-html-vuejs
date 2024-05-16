<script>
import { defineComponent } from "vue";
import { GoogleMap, Marker } from "vue3-google-map";

export default defineComponent({
    components: {
        GoogleMap,
        Marker,
    },
    setup() {
        const center = {
            lat: 43.7695604, lng: 11.2558136
        };
        return {
            center
        }
    }
})
</script>

<template>
    <div class="container-maps">
        <GoogleMap class="maps" api-key="AIzaSyBqvZfzDW7YlZHtfaR-5l1v8f0YkMzswQM" :zoom="5" :center="center">
            <Marker :options="{ position: center }" />
        </GoogleMap>
    </div>
</template>

<style scoped lang="scss">
.container-maps {
    display: flex;
    justify-content: center;
    padding-top: 50px;

    .maps {
        height: 400px;
        width: 90%;
    }
}
</style>