---
layout: pixijs-post
title: Starmap - Random Distribution
category: PixiJS
scripts:
- url: /assets/js/pixi.min.js
  is_local: true
footnotes:
- url: https://pixijs.com/
  note: PixiJS homepage
codeHighlightingEnabled: true
---
<script>
  let app = new PIXI.Application({ width: 640, height: 360 });
  const pixiContainer = document.getElementById('content');

  pixiContainer.appendChild(app.view);

  const starTexture = PIXI.Texture.from('/assets/img/star.png');
  const starAmount = 500;

  for (let i = 0; i < starAmount; i++)
  {
    const star = new PIXI.Sprite(starTexture);

    star.anchor.x = 0.5;
    star.anchor.y = 0.5;
    star.scale.x = 0.05;
    star.scale.y = 0.05;

    star.x = Math.random() * app.screen.width;
    star.y = Math.random() * app.screen.height;

    app.stage.addChild(star);
  }
</script>