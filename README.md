<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>WebAR Con Cua</title>

  <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
  <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
</head>

<body style="margin:0; overflow:hidden;">

  <a-scene
    embedded
    vr-mode-ui="enabled: false"
    renderer="logarithmicDepthBuffer: true;"
    arjs="sourceType: webcam; debugUIEnabled: false;"
  >

    <a-assets>
      <a-asset-item
        id="crab-obj"
        src="./10012_crab_v2_iterations-1.obj">
      </a-asset-item>

      <a-asset-item
        id="crab-mtl"
        src="./10012_crab_v2_iterations-1.mtl">
      </a-asset-item>
    </a-assets>

    <!-- Marker Hiro -->
    <a-marker preset="hiro">

      <a-obj-model
        src="#crab-obj"
        mtl="#crab-mtl"
        position="0 0 0"
        rotation="-90 0 0"
        scale="0.03 0.03 0.03">
      </a-obj-model>

    </a-marker>

    <!-- Camera -->
    <a-entity camera></a-entity>

  </a-scene>

</body>
</html>
