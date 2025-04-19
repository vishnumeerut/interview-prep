# Explain the `<audio>` and `<video>` Elements

The `<audio>` and `<video>` elements in HTML5 allow for embedding media files like sound and video directly into web pages without the need for third-party plugins like Flash. These elements offer simple ways to add multimedia content, which can be controlled through HTML attributes and JavaScript.

### `<audio>` Element:
The `<audio>` element is used to embed sound content, such as music or audio files, in a web page.

#### Syntax:
```html
<audio controls>
    <source src="audio-file.mp3" type="audio/mp3">
    Your browser does not support the audio element.
</audio>

```
### `<video>` Element:
The `<video>` element is used to embed video content in a web page. It allows users to watch video directly from the browser.

#### Syntax:
```html
<video controls width="640" height="360">
    <source src="video.mp4" type="video/mp4">
    <source src="video.ogg" type="video/ogg">
    Your browser does not support the video element.
</video>


```
