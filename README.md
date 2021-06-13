# aksVideoPlayer.js
Video Player

**[View the Demo on CodePen &rarr;](https://codepen.io/collection/DPvrMq)**

## Getting Started

Compiled and production-ready code can be found in the `dist` directory.

### 1. Include aksVideoPlayer.min.js on your site.

**Direct Download**

You can [download the files directly from GitHub](https://github.com/Ahmetaksungur/aksvideoplayer/archive/main.zip).

```html
<link type="text/css" rel="stylesheet" href="dist/aksVideoPlayer.min.css">
```

```html
<script src="dist/aksVideoPlayer.min.js"></script>
```

**CDN**

```html
<link type="text/css" rel="stylesheet" href="https://unpkg.com/aksvideoplayer@1.0.0/dist/aksVideoPlayer.min.css">
```

```html
<script src="https://unpkg.com/aksvideoplayer@1.0.0/dist/aksVideoPlayer.min.js"></script>
```
---

```html
<link type="text/css" rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aksvideoplayer@1.0.0/dist/aksVideoPlayer.min.css">
```

```html
<script src="https://cdn.jsdelivr.net/npm/aksvideoplayer@1.0.0/dist/aksVideoPlayer.min.js"></script>
```

**jQuery**

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
```
---

**NPM**

```bash
npm i aksvideoplayer
```


## Document aksVideoPlayer.js

```html
<div id="video"></div>
```

```js
$("#video").aksVideoPlayer({
  file: [
    {
      file: "videos/video-1080.mp4",
      label: "1080p"
    },
    {
      file: "videos/video-720.mp4",
      label: "720p"
    },
    {
      file: "videos/video-540.mp4",
      label: "540p"
    },
    {
      file: "videos/video-360.mp4",
      label: "360p"
    },
    {
      file: "videos/video-240.mp4",
      label: "240p"
    }
  ],
  width: 640,
  height: 360,
  poster: "videos/poster.webp",
});
```
[Sample](https://codepen.io/ahmetaksungur/pen/Jjbddem).

### Captions

```js
  captions: [
    {
      file: "videos/subtitle.en.vtt",
      label: "English",
      kind: "captions",
      srclang: "en"
    },
    {
      file: "videos/subtitle.fr.vtt",
      label: "Français",
      kind: "captions",
      srclang: "fr"
    },
    {
      file: "videos/subtitle.tr.vtt",
      label: "Türkçe",
      kind: "captions",
      srclang: "tr"
    },
    {
      file: "videos/subtitle.de.vtt",
      label: "Deutsche",
      kind: "captions",
      srclang: "de"
    }
  ],
```
[Sample](https://codepen.io/ahmetaksungur/pen/jOVPbOw).

### Advertising

**Google Ima 3**

```html
<script src="https://imasdk.googleapis.com/js/sdkloader/ima3.js"></script>
```

```js
  ads: [
    {
    type: "google",
    url: 'https://pubads.g.doubleclick.net/gampad/ads?sz=640x480&' +
    'iu=/124319096/external/single_ad_samples&ciu_szs=300x250&impl=s&gdfp_req=1&'+
    'env=vp&output=vast&unviewed_position_start=1&cust_params=' +
    'deployment%3Ddevsite%26sample_ct%3Dskippablelinear&correlator='
    },
    {
      type: "image",
      src: "videos/ads.png",
      width: 320,
      height: 50,
      link: "http://adsurl.com/",
      time: "00:20"
    },
    {
      type: "video",
      src: "videos/videoads.mp4",
      link: "http://adsurl.com/",
      time: "00:35",
      adstimer: "6"
    },
    {
      type: "video",
      src: "videos/videoads.mp4",
      link: "http://adsurl.com/",
      time: "01:35",
      adstimer: "6"
    },
    {
      type: "html",
      html : '<div class="class-name"><img src="" style=""/>Ads Code</div>',
      time: "00:10"
    }
  ],
```
[Sample](https://codepen.io/ahmetaksungur/pen/xxRGwGm).

### Context Menu

```js
  contextMenu: [
    {
      type: "urlCopy",
      label: "Copy Video Url",
      url: "http://url.com/"
    },
    {
      type: "socialmedia",
      label: "Share on Social Media",
      socials: [
        {
          label: "Facebook",
          url: "",
          colorBg: "#0066ff",
          color: "white",
          icon:
            '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 10 20"><defs/><path d="M8.174 3.32H10V.14A23.66 23.66 0 007.34 0C4.709 0 2.906 1.656 2.906 4.7v2.8H0v3.555h2.905V20h3.56v-8.945h2.789L9.697 7.5H6.466V5.05c0-1.027.276-1.73 1.708-1.73z" fill-rule="evenodd"/></svg>'
        },
        {
          label: "Twitter",
          url: "",
          colorBg: "#0089ff",
          color: "white",
          icon:
            '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 16"><defs/><path d="M17.944 3.987c.013.175.013.35.013.526C17.957 9.85 13.833 16 6.294 16c-2.322 0-4.48-.662-6.294-1.813.33.038.647.05.99.05 1.916 0 3.68-.637 5.089-1.725-1.802-.037-3.313-1.2-3.833-2.8.254.038.508.063.774.063.368 0 .736-.05 1.079-.137-1.878-.376-3.287-2-3.287-3.963v-.05c.546.3 1.18.488 1.853.512A4.02 4.02 0 01.838 2.775c0-.75.203-1.438.558-2.038a11.71 11.71 0 008.452 4.225 4.493 4.493 0 01-.102-.924c0-2.226 1.828-4.038 4.1-4.038 1.18 0 2.245.487 2.994 1.275A8.145 8.145 0 0019.442.3a4.038 4.038 0 01-1.802 2.225A8.316 8.316 0 0020 1.9a8.74 8.74 0 01-2.056 2.087z" fill-rule="evenodd"/></svg>'
        }
      ]
    },
    {
      type: "iframe",
      label: "Copy Iframe Code",
      iframe: "&lt;iframe&gt;&lt;/iframe&gt;"
    }
  ],
```
[Sample](https://codepen.io/ahmetaksungur/details/OJbVyMR).

### Attributes

```js
          poster: "", // picture telling the video
          width: 640, // player width
          height: 360, // player height
          rewind: true, // video rewind button
          rewindValue: 10, // video rewind second
          forward: false, // video forward button
          forwardValue: 10, // video forward second
          preview: true, // previews of the video
          previewWidth: 140, // previews width
          previewHeight: 95, // previews height
          controller: true, // video controller on off
          autoplay: false, // video autoplay
          muted: true, // video muted
          volume: 1, // video volume start
          loop: false, // loop the video
          playbackRate: ["0.25", "0.5", "0.75", "1", "1.25", "1.5", "1.75", "2"], // playbackRate
          pictureinpicture: true, // to watch when scroll scrolls down
          // language
          playbackRateLabel: "Playing Speed",
          captionsLabel: "Subtitles",
          sourcesLabel: "Quality",
          playLabel: "Play",
          pauseLabel: "Pause",
          rewindLabel: "Rewind %s Seconds",
          forwardLabel: "Forward %s Seconds",
          settingsLabel: "Settings",
          fullScreenLabel: "Fullscreen",
          exitFullScreenLabel: "Exit Fullscreen",
          adsSkipLabel: "Skip Ad",
          closeLabel: "Close",
          pictureinpictureLabel: "Picture in Picture",
```


## License

The code is available under the [MIT License](https://github.com/Ahmetaksungur/aksvideoplayer/blob/main/LICENSE).
