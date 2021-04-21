# Video/Audio Content

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)

## `<video>` element

```html
<video src="rabbit320.webm" controls>
    <p>
        Your browser doesn't support HTML5 video. Here is a 
        <a href="rabbit320.webm">link to the video</a>
        instead.
    </p>
</video>
```

__Attributes:__

* `src`
  * This contains the path to the video
* `controls`
  * This enabled the native browser controls for the video.
  * If you want, you may also create a custom interface using JS instead.
* `width`, `height`
  * You can control the video size with these attributes or with CSS.
* `autoplay`
  * The video/audio plays right away. Not recommended since it can be annoying.
* `loop`
  * The video/audio plays again whenever it finished. Not recommended since it can be annoying.
* `muted`
  * The media plays with sound off by default
* `poster`
  * The image displayed before the video is played
* `preload`
  * Buffering large files
  * Values:
    * `"none"` - Don't buffer the file
    * `"auto"` - buffers the media file
    * `"metadata"` - buffers only the metadata

### `<video>` paragraph

This is __fallback content__ -- it'll be displayed if the browser doesn't
support html5 video.

### Use multiple formats to improve compatibility

Some older browsers won't support newer video format. You can use multiple formats
so more browsers can play video.

```html
<video controls>

    <source src="rabbit320.mp4" type="video/mp4">
    <source src="rabbit320.webm" type="video/webm">
    <p>
        Your browser doesn't support HTML5 video. Here is a 
        <a href="rabbit320.mp4">link to the video</a>
        instead.
    </p>
</video>
```

## `<audio>` element

The audio element works in the same way as the video element,
but it doesn't support `width/height` or the `poster` attributes.

## Video text tracks

Useful:

* For people with auditory impairments
* Noisy environments
* Audio would be a disraction/disruption
* People don't speak the language in the video

You can use [WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) to create transcripts.

Types of WebVTT cues:

<dl>

<dt><strong>subtitles</strong></dt>
<dd>Translations of foreign material</dd>

<dt><strong>captions</strong><dt>
<dd>Synchronized transcripts of dialog or descriptions of sounds</dd>

<dt><strong>timed descriptions</strong></dt>
<dd>Text to be spoken by the media player to describe visuals to visually
impaired users</dd>

</dl>

### Typical WebVTT file

```webvtt
WEBVTT

1
00:00:59:590 --> 00:01:10:000
This is a subtitle

  ...
```

Instructions:

1. Save as a `.vtt` file
2. Link to the file with the `<track>` element inside `<audio>` or `<video>` after all source elements.
3. Use the `kind` attribute to specify the cue (`subtitles`, `captions`, `descriptions`)
4. Use the `srclang` attribute to specify the language the subtitles are in
5. Use the `label` to help readers identify the language

```html
<video controls>
    <source src="example.mp4" type="video/mp4">
    <source src="example.webm" type="video/webm">
    <track kind="subtitles" src="subtitles_es.vtt" srclang="es" label="Spanish">
</video>
```
