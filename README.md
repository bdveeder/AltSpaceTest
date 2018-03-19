<!DOCTYPE html>
<html><body>
<script src="https://aframe.io/releases/0.3.0/aframe.min.js"></script>
<script src="https://cdn.rawgit.com/AltspaceVR/AltspaceSDK/v2.0.2/dist/altspace.min.js"></script>

<!-- set up the scene -->
<a-scene altspace='vertical-align: bottom;'>

    <!-- preload all our textures -->
    <a-assets>
        <img id='moon' src='assets/moon.jpg'/>
        <img id='stars' src='assets/stars.png'/>
    </a-assets>

    <!-- add the moon to the scene -->
    <a-sphere position='0 1.5 0' material='src: #moon;'>
        <!-- add an animation to make it rotate -->
        <a-animation to='0 360 0' easing='linear' dur='20000' repeat='indefinite'/>
    </a-sphere>

    <!-- add the backdrop of stars -->
    <a-sky src='#stars' radius='2500'></a-sky>

    <!-- add a view camera (2d only) -->
    <a-entity position='0 0 2'>
        <a-camera></a-camera>
    </a-entity>

</a-scene>

</body></html>
