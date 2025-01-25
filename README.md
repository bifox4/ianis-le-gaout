<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Réalité Augmentée Sans Marqueur</title>
  <!-- A-Frame pour RA -->
  <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
  <!-- AR.js -->
  <script src="https://cdn.jsdelivr.net/gh/jeromeetienne/ar.js/aframe/build/aframe-ar.min.js"></script>
  <style>
    body, html {
      margin: 0;
      overflow: hidden;
      height: 100%;
    }
  </style>
</head>
<body>
  <!-- Scène A-Frame avec AR.js -->
  <a-scene
    vr-mode-ui="enabled: false"
    embedded
    arjs="sourceType: webcam; debugUIEnabled: false;">
    
    <!-- Indicateur de surface (plan transparent pour la détection) -->
    <a-plane 
      position="0 0 0" 
      rotation="-90 0 0" 
      width="5" 
      height="5" 
      color="#000000" 
      opacity="0.5">
    </a-plane>

    <!-- Objet 3D (une boîte simple) -->
    <a-box 
      position="0 0.5 0" 
      rotation="0 45 0" 
      color="blue" 
      shadow></a-box>

    <!-- Lumières -->
    <a-light type="ambient" intensity="0.5"></a-light>
    <a-light type="point" intensity="1" position="2 4 4"></a-light>
  </a-scene>
</body>
</html>
