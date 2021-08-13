---
title: Installation
type: introduction
layout: docs
parent_section: introduction
order: 2
---

이 설치 섹션에서는 몇가지 `A-Frame` 을 시작할 수 있는 방법을 소개하고 있습니다. 대부분의 방법들은 A-Frame 이 근본적으로 HTML과 Javascript 이기 때문에 설치 이후 별도의 설치가 필요하지는 않습니다.

<!--toc-->

## Code Editors in the Browser

브라우저에서 가장 빠르게 실행해보는 방법입니다.

### Remix on Glitch

![Glitch](https://cloud.githubusercontent.com/assets/674727/24480466/54b17d22-1499-11e7-8a18-d4f76b49ad07.jpg)

[glitch]: https://glitch.com/~aframe

[Glitch][glitch] 는 웹 사이트를 호스팅, 인스턴스 배포를 지원하는 온라인 코드 에디터를 제공합니다. 에디터는 다수의 파일과 디렉터리 뿐만 아니라 프론트엔드와 백엔드의 코드를 지원합니다.
`Glitch` 는 기존에 존재하는 프로젝트를 리믹스하고, 리믹스가 된 프로젝트를 자신이 소유할 수 있도록 지원하며, 모두가 볼 수 있도록 변경사항을 즉각적으로 호스팅하고, 배포합니다.

[Hit **Remix** on this A-Frame project][glitch], mess with the HTML in
`index.html`, and see your site published live on each change! The base A-Frame
Glitch, for example, is published at `aframe.glitch.me`, but we will provide your
own custom URL name.

[Hit **Remix** on this A-Frame project][glitch] 예를 들어, A-Frame이 기본으로 작성된 `Glitch` 는 `aframe.glitch.me` 로 배포되지만 우리는 우리 자신의 커스텀 URL 도메인 이름으로 제공할 것 입니다. 

Below are a few other A-Frame Glitches for starters: <br>
아래는 몇가지 A-Frame Glitches 를 다루는 `Starter` 링크 입니다.

- [aframe-aincraft](https://glitch.com/~aframe-aincraft) - Minecraft demo.
- [aframe-gallery](https://glitch.com/~aframe-gallery) - 360&deg; image gallery.
- [aframe-registry](https://glitch.com/~aframe-registry) - Showcase of various components.
- [aframe-vaporwave](https://glitch.com/~aframe-vaporwave) - Retro-futuristic scene.
- [networked-aframe](https://glitch.com/~networked-aframe) - Multiuser.

### Other Code Editors

아래는 몇가지 다른 브라우저상의 코드에디터에서 실행되는 `A-Frame Starter Kit` 입니다. 둘다 remix 와 forking 기능을 지원합니다.
- [CodePen &mdash; A-Frame](https://codepen.io/mozvr/pen/BjygdO)

## Local Development (로컬 개발환경)

### Local Server 를 사용해요.

아래 옵션은 로컬 서버를 사용하여 프로젝트를 개발해야 파일이 제대로 제공됩니다. 로컬 서버의 옵션은 다음과 같습니다.

- HTML 파일이 존재하는 같은 디렉토리 안의 터미널에서 `npm i -g five-server@latest && five-server --port=8000` 를 실행합니다.
- HTML 파일이 존재하는 같은 디렉토리에서 [Mongoose](https://www.cesanta.com/products/binary) application 을 열고 다운로드 합니다.
- HTML 파일과 같은 디렉토리 구조 안의 터미널에서 `python -m SimpleHTTPServer` (or `python -m http.server` for Python 3)를 실행하세요.

우리가 서버를 실행할 때, 우리는 종종 브라우저 안에서 local URL과 서버가 동작하는 local server 포트를 사용하여 프로젝트를 오픈하죠(예를 들면, http://localhost:8000/) <br>
프로젝트를 지원하지 않는 도메인인 `file://` 프로토콜을 사용하여 오픈하려고 하지마세요. 절대적이고 상대적인 URL들은 동작하지 않을 것 입니다.

### `Github` 에서 보일러 플레이트를 설치해요

[ghpages]: https://pages.github.com/

보일러 플레이트는 다음을 포함하고 있습니다.

- A simple HTML file that links to the [current version of A-Frame](#builds-prod)
- [current version of A-Frame](#builds-prod) 로 연결되는 간단한 HTML 파일 
- An optional local development server
- 모두와 공유하기 위해 [GitHub Pages][ghpages]를 통한 간단한 개발 워크플로우 

우리는 두가지 방법 중 하나를 이용해서 보일러 플레이트를 설치할 수 있습니다.

<a class="btn btn-download" href="https://github.com/aframevr/aframe-boilerplate/">깃허브에서 포크하기</a>
<br>(Note this is marked as 'discontinued', the Aframe version packaged with this is 0.5)

<a class="btn btn-download" href="https://github.com/aframevr/aframe-boilerplate/archive/master.zip" download="aframe-boilerplate.zip">.ZIP을 다운로드하기<span></span></a>

### Include the JS Build

HTML 파일에 A-Frame을 포함하기 위해 CDN 빌드를 가리키는 '[script]' 태그를 삭제합니다.


```html
<head>
  <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
</head>
```

만약 우리가 서비스를 제공하고자 한다면 JS build 를 통해 다운로드 할 수 있습니다.

<a id="builds-prod" class="btn btn-download" href="https://aframe.io/releases/1.2.0/aframe.min.js" download>Production Version <span>1.2.0</span></a> <em class="install-note">Minified</em>
<a id="builds-dev" class="btn btn-download" href="https://aframe.io/releases/1.2.0/aframe.js" download>Development Version <span>1.2.0</span></a> <em class="install-note">Uncompressed with Source Maps</em>

### `npm` 으로 설치하기
우리는 npm 명령어를 통해 A-Frame 을 설치할 수 있습니다.

```bash
$ npm install aframe
```

설치한 다음, 우리 애플리케이션 안에 A-Frame 을 Webpack 또는 Browserify 를 이용해서 번들링 할 수 있습니다. 

```js
require('aframe');
```

[angle]: https://www.npmjs.com/package/angle

만약 여러분이 npm 을 사용한다면, 여러분은 A-Frame을 위한 [`angle`][angle] CLI 를 사용할 수 있습니다. 여기서 `angle` 의 역할은 단일 커맨드로 scene 과 template 를 시작할 수 있도록 지원합니다.


```sh
npm install -g angle && angle initscene
```

## Cordova Development

`A-Frame`은 `Cordova` 애플리케이션과 호환되고 있습니다. 현재 `A-Frame` 및 `A-Frame`의 종속성을 가진 모듈(또는 라이브러리)들이 CDN 소스로부터 asset들을 로드하기 때문에 네트워크 엑세스가 별도로 필요합니다.

[Cordova A-Frame Showcase App (demo)](https://github.com/benallfree/cordova-aframe-showcase)

### 설치

[cordova-plugin-xhr-local-file](https://github.com/benallfree/cordova-plugin-xhr-local-file) 플러그인을 설치해주세요. 이 플러그인은 Cordova가 `file://` 로부터 실행된다는 것을 의미하며, 그리고 local로  `file://` assets(JSON font, 3D model 등)에 XHR 요청을 보낼 때 이 플러그인이 없이는 요청이 실패하게 될 겁니다.

```bash
cordova plugin add cordova-plugin-xhr-local-file
```

In your `index.html`, adjust as follows:

```html
<head>
  <meta
        http-equiv="Content-Security-Policy"
        content="
          default-src 
            'self' 
            data: 
            gap: 
            https://ssl.gstatic.com 
            'unsafe-eval' 
            https://cdn.aframe.io         <-- required
            https://dpdb.webvr.rocks      <-- required
            https://fonts.googleapis.com  <-- required
            https://cdn.jsdelivr.net      <-- your choice, see below
            ; 
          style-src 
            'self' 
            'unsafe-inline'
            ; 
          media-src *; 
          img-src 
            'self' 
            data:                         <-- required
            content:                      <-- required
            blob:                         <-- required
            ;
        "
      />
  ...
  <script src="https://cdn.jsdelivr.net/npm/aframe@1.2.0/dist/aframe-master.min.js"></script>
  <script id='my-scene' type="text/html">
    ...your scene goes here...
  </script>
  <script>
    document.addEventListener('deviceready', function() {
      // After the 'deviceready' event, Cordova is ready for you to render your A-Frame scene.
      document.getElementById('scene-root').innerHTML = document.getElementById('my-scene').innerHTML
    })
  </script>
</head>
<body>
  <div id='scene-root'></div>
  ...
</body>
```

### Discussion


#### deviceready 이벤트

브라우저 환경과 Cordova 환경의 가장 큰 차이점은 여러분의 Scene이 렌더링 되기전에 Cordova 환경이 `deviceready` 이벤트의 수신을 기다리고 있다는 것입니다.

위의 샘플이 순수한 DOM+JS 접근을 보여주기도 하지만, 리액트와 같은 프레임워크를 사용할 수도 있습니다.

```javascript
document.addEventListener('deviceready', () => {
  ReactDOM.render(<Root />, document.getElementById('root'))
})
```

#### Layout

여러분이 지정한 디바이스에 따라, A-Frame 의 기본적인 CSS 스타일때문에 특정 버튼들 또는 컨트롤러들이 위치를 벗어나거나 또는 폰 스크린에 너무 가깝게 배치되는 등, 위치가 어긋날 수 있습니다. 
이를 개선하기 위해, 여러분 자신만의 디바이스에 자신만의 CSS 스타일을 오버라이드하여 위치에 맞게 조정해서 서비스를 제공해보세요.

