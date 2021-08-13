---
title: Introduction
section_title: Introduction
type: introduction
layout: docs
order: 1
parent_section: docs
section_order: 1
installation: true
examples:
  - title: Hello, World!
    src: https://glitch.com/edit/#!/aframe?path=index.html
---

[three.js]: https://threejs.org

## Getting Started

[glitch]: http://glitch.com/~aframe

A-Frame은 어떠한 설치없이도 순수 HTML 파일로 개발할 수 있습니다. A-Frame 을 시도하기 위한 가장 좋은 방법은,
**[remix the starter example on Glitch][glitch]** 에서 찾을 수 있고, 온라인 코드 에디터로 즉각적으로 호스팅하고 무료로 배포할 수 있습니다.
대안책으로는, 기존에 사용하던 `.html` 파일의  `<head>` 태그 안에 `A-Frame` 을 포함하는 코드를 작성하는 것 입니다.

```html
<html>
  <head>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
    </a-scene>
  </body>
</html>
```

[Installation]: ./installation.md
[school]: https://aframe.io/school/

[Installation] 페이지에서는, A-Frame 을 시작하기 위한 조금 더 많은 getting started 옵션들을 제공합니다. `A-Frame`의 학습을 위해
[A-Frame School][school] 를 체크하고, 단계별로 레슨을 완료하면서 학습하기를 권장합니다.


## A-Frame이란 무엇일까요?

[github]: https://github.com/aframevr/
[community]: https://aframe.io/community/

![A-Frame](https://cloud.githubusercontent.com/assets/674727/25392020/6f011d10-298c-11e7-845e-c3c5baebd14d.jpg)

:A-Frame은 virtual reality(VR), 즉 가상 현실을 만들고 경험을 제공하기 위한 위한 웹 프레임워크에요. HTML 기반에서 동작하는 `A-Frame`은 입문하기 쉽도록 간단하게 만들어졌습니다.
하지만 3D scene 이나 그래프 또는 마크업 언어와는 다른 특징을 가지고 있습니다.
`A-Frame` 코어는 선언적인, 확장 가능한, 그리고 [three.js]로 구성가능한 구조를 지원하는 강력한 entity-component framework 입니다.

`A-Frame` 은 모질라 재단에서 구상되었으며, 현재 Supermedium 내의 A-Frame의 공동 제작자가 유지 관리하고 있으며, VR 콘텐츠를 개발하는 쉽고 강력한 방법으로 개발되어 왔습니다.
독립 오픈소스 프로젝트로서, A-Frame은 가장 큰 VR 커뮤니티 중 하나로 성장하게 되었습니다.

A-Frame은 대부분의 VR 헤드셋 -- Vive, Rift, Windows Mixed Reality, Daydream, GearVR, Cardboard, Oculus Go, 그리고 Argument Reality(AR)을 모두 지원하고 있습니다.
비록 A-Frame이 전반적인 스펙트럼을 지원하긴 하지만, 위치추적과 컨트롤러를 사용하여 만들어진 기본 360° 반경의 컨텐츠를 뛰어 넘어, 완전몰입형 interactive VR 경험을 정의하는데에 초점을 맞추고 있습니다.

<div class="docs-introduction-examples">
  <a href="https://supermedium.com/supercraft">
    <img alt="Supercraft" target="_blank" src="https://user-images.githubusercontent.com/674727/41085457-f5429566-69eb-11e8-92e5-3210e4c6c4a0.gif" height="190" width="32%">
  </a>
  <a href="https://aframe.io/a-painter/?url=https://ucarecdn.com/962b242b-87a9-422c-b730-febdc470f203/">
    <img alt="A-Painter" target="_blank" src="https://cloud.githubusercontent.com/assets/674727/24531388/acfc3dda-156d-11e7-8563-5bd75252f70f.gif" height="190" width="32%">
  </a>
  <a href="https://supermedium.com">
    <img alt="Supermedium" target="_blank" src="https://user-images.githubusercontent.com/674727/37294616-7212cd20-25d3-11e8-9e7f-c0c61074f1e0.png" height="190" width="32%">
  </a>
  <a href="https://aframe.io/a-blast/">
    <img alt="A-Blast" target="_blank" src="https://cloud.githubusercontent.com/assets/674727/24531440/0336e66e-156e-11e7-95c2-f2e6ebc0393d.gif" height="190" width="32%">
  </a>
  <a href="https://aframe.io/a-saturday-night/">
    <img alt="A-Saturday-Night" target="_blank" src="https://cloud.githubusercontent.com/assets/674727/24531477/44272daa-156e-11e7-8ef9-d750ed430f3a.gif" height="190" width="32%">
  </a>
  <a href="https://github.com/googlecreativelab/webvr-musicalforest">
    <img alt="Musical Forest by @googlecreativelab" target="_blank" src="https://cloud.githubusercontent.com/assets/674727/25109861/b8e9ec48-2394-11e7-8f2d-ea1cd9df69c8.gif" height="190" width="32%">
  </a>
</div>

## Features

:eyeglasses: **VR Made Simple**: Just drop in a `<script>` tag and `<a-scene>`.
A-Frame will handle 3D boilerplate, VR setup, and default controls. Nothing to
install, no build steps.

:heart: **Declarative HTML**: HTML is easy to read, understand, and
copy-and-paste. Being based on top of HTML, A-Frame is accessible to everyone:
web developers, VR enthusiasts, artists, designers, educators, makers, kids.

:electric_plug: **Entity-Component Architecture**: A-Frame is a powerful
[three.js] framework, providing a declarative, composable, reusable
[entity-component structure][ecs]. HTML is just the tip of the iceberg;
developers have unlimited access to JavaScript, DOM APIs, three.js, WebVR, and
WebGL.

:globe_with_meridians: **Cross-Platform VR**: Build VR applications for Vive,
Rift, Windows Mixed Reality, Daydream, GearVR, and Cardboard with support for
all respective controllers. Don't have a headset or controllers? No problem!
A-Frame still works on standard desktop and smartphones.

[ecs]: ./entity-component-system.md

[A-Painter]: https://github.com/aframevr/a-painter
[Tilt Brush]: https://www.tiltbrush.com/

:zap: **Performance**: A-Frame is optimized from the ground up for WebVR. While
A-Frame uses the DOM, its elements don't touch the browser layout engine. 3D
object updates are all done in memory with little garbage and overhead. The most
interactive and large scale WebVR applications have been done in A-Frame
running smoothly at 90fps.

[inspector]: ./visual-inspector-and-dev-tools.md

:mag: **Visual Inspector**: A-Frame provides a handy built-in [visual 3D
inspector][inspector]. Open up *any* A-Frame scene, hit `<ctrl> + <alt> + i`,
and fly around to peek under the hood!

![Inspector](https://cloud.githubusercontent.com/assets/674727/25377018/27be9cce-295b-11e7-9098-3e85ac1fe172.gif)

[augmented reality]: https://github.com/jeromeetienne/AR.js#augmented-reality-for-the-web-in-less-than-10-lines-of-html
[environment]: https://github.com/supermedium/aframe-environment-component
[multiuser]: https://github.com/haydenjameslee/networked-aframe
[oceans]: https://github.com/donmccurdy/aframe-extras/tree/master/src/primitives
[particle systems]: https://github.com/IdeaSpaceVR/aframe-particle-system-component
[physics]: https://github.com/donmccurdy/aframe-physics-system
[state]: https://npmjs.com/package/aframe-state-component
[super hands]: https://github.com/wmurphyrd/aframe-super-hands-component
[teleportation]: https://github.com/fernandojsg/aframe-teleport-controls

:runner: **Components**: Hit the ground running with A-Frame's core components
such as geometries, materials, lights, animations, models, raycasters, shadows,
positional audio, text, and controls for most major headsets. Get even further
from the hundreds of community components including [environment], [state], [particle
systems], [physics], [multiuser], [oceans], [teleportation], [super hands], and
[augmented reality].

:earth_americas: **Proven and Scalable**: A-Frame has been used by companies
such as Google, Disney, Samsung, Toyota, Ford, Chevrolet, Amnesty
International, CERN, NPR, Al Jazeera, The Washington Post, NASA. Companies such
as Google, Microsoft, Oculus, and Samsung have made contributions to A-Frame.\

## Off You Go!

[Discord]: https://supermedium.com/discord
[slack]: https://aframe.io/slack-invite/

만약 여러분이 여기에 온게 처음이라면, `Aframe` 을 시작해볼 수 있는 몇가지 성공적인 플랜을 세워두었어요.

1. A-Frame과 커뮤니티 프로젝트를 볼 수 있도록 몇가지 팁과 업데이트 사안을 제공하는 [Subscribe to the Newsletter](https://aframe.io/subscribe/)  
 
2. A-Frame을 시작하기 위한 공식문서를 읽어보세요. <br>
[Glitch](https://glitch.com/~aframe) >> 코딩 플레이 그라운드로 사용되고 몇가지 좋은 예제들이 제공되고 있어요.

3. [Join us on Discord][Discord] 와 [Slack][slack] 그리고 만약 여러분이 궁금한게 있다면,
[search and ask on StackOverflow](http://stackoverflow.com/questions/ask/?tags=aframe) 에서 질문하면
누군가 여러분에게 도움을 줄 것입니다.

4. 무언가를 만들 때, 프로젝트를 온라인으로 공유하세요. 그러면 기능을 사용할 수 있도록 노력하겠습니다. <br>

그리고 자바스크립트와 three.js 에 대한 기초에 대해 알아보는게 많은 도움이 될 것 입니다. 즐거운 시간 되세요!
