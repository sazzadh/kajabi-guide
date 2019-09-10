## Background Video


```liquid
{% raw %}
{% assign s-ID            = section.id %}
{% assign s-BgVideo       = current_site.find_video[section.settings.bg_video] %}
{% assign s-BgVideoID     = s-BgVideo.wistia_id %}
{% assign s-BgImage       = section.settings.bg_video_cover | image_picker_url %}
{% endraw %}
```

```html
<div id="wistia_{{ s-BgVideoID }}" class="wistia_embed backgroundVideo" data-src="{{ s-BgVideoID }}" data-img="{{ s-BgImage }}"></div>
```

```json
{
	"type": "video",
	"id": "bg_video",
	"label": "Background Video",
	"info": ""
},
{
	"type": "image_picker",
	"id": "bg_video_cover",
	"label": "Background Video Cover Image",
	"info": "Suggested dimensions: 1856 × 1044"
}
```


### Instruction
To enable the mobile background video please remove the folling code from the `scripts.js` file

```javascript
if( /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent) ) {
	$(this).hide();
	$(this).closest('.hero-background').css('background-image', 'url(' + bgImg + ')');;
}
```

Put the background video inside a dive which has `position: relative;` css style
Plus you can use a small image (16x9 px size) as place holder of the video is there are no aditionl content of the main dive.