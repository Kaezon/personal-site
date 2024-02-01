---
layout: pixijs-post
scripts:
  - url: /assets/js/pixi.min.js
    is_local: true
---
<script>
  let app = new PIXI.Application({ width: 640, height: 360 });
  const pixiContainer = document.getElementById('content');
  pixiContainer.appendChild(app.view);

  const rectangle = new PIXI.Graphics();
  rectangle.beginFill(0xFF0000);
  rectangle.drawRect(0, 0, 200, 100);
  rectangle.endFill();

  app.stage.addChild(rectangle);
</script>