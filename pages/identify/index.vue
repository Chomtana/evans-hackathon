
  
<template>

    <v-container Justify="center">
            <v-card
                color="#FF0000"
            >
            <vue-web-cam
                ref="webcam"
                :device-id="deviceId"
                width="100%"
                @started="onStarted"
                @stopped="onStopped"
                @error="onError"
                @cameras="onCameras"
                @camera-change="onCameraChange"
            />
            <v-card-title>Seat Code</v-card-title>
    
        <v-card-subtitle class="pb-0">EVANS51219</v-card-subtitle>
    
        <v-card-text class="text--primary">
            <div> </div>
            <div>License : FF01ET</div>
            <div>Path : Rama4 - Chula</div>
            <div>Seat : 30</div>
        </v-card-text>
        
        <v-card-actions>
            <v-btn
            color="orange"
            text
            >
            Scan
            </v-btn>
    
        </v-card-actions>
        
        </v-card>

    </v-container>
</template>

<script>
export default {
    name: "App",
    components: {
    },
    data() {
        return {
            img: null,
            camera: null,
            deviceId: null,
            devices: []
        };
    },
    computed: {
        device: function() {
            return this.devices.find(n => n.deviceId === this.deviceId);
        }
    },
    watch: {
        camera: function(id) {
            this.deviceId = id;
        },
        devices: function() {
            // Once we have a list select the first one
            const [first, ...tail] = this.devices;
            if (first) {
                this.camera = first.deviceId;
                this.deviceId = first.deviceId;
            }
        }
    },
    methods: {
        onCapture() {
            this.img = this.$refs.webcam.capture();
        },
        onStarted(stream) {
            console.log("On Started Event", stream);
        },
        onStopped(stream) {
            console.log("On Stopped Event", stream);
        },
        onStop() {
            this.$refs.webcam.stop();
        },
        onStart() {
            this.$refs.webcam.start();
        },
        onError(error) {
            console.log("On Error Event", error);
        },
        onCameras(cameras) {
            this.devices = cameras;
            console.log("On Cameras Event", cameras);
        },
        onCameraChange(deviceId) {
            this.deviceId = deviceId;
            this.camera = deviceId;
            console.log("On Camera Change Event", deviceId);
        }
    }
};
</script>
