## Countdown
### Countdown Timer section example

```liquid
{% assign c-NumberColor = section.settings.number_color | default: "" %}
{% assign c-Style       = '' %}
{% assign c-End         = section.settings.countdown_end_time %}
{% assign c-Timezone    = section.settings.countdown_timezone %}
{% assign c-Days        = section.settings.days_text %}
{% assign c-Hours       = section.settings.hours_text %}
{% assign c-Minutes     = section.settings.minutes_text %}
{% assign c-Seconds     = section.settings.seconds_text %}

 <div class="countdown countdown--{{ c-Style }} countdown--sunset" id="countdown-timer" kjb-settings-id="{{ kjb-End }}" data-end-time="{{ c-End }}" data-timezone="{{ c-Timezone }}">
	<div class="row">
		<div class="col-sm-10">
			<div class="row">
				<div class="col-xs-3 countdown__item">
					<h2 id="days" class="countdown__amount days">00</h2>
					<h6 class="countdown__title" kjb-settings-id="{{ kjb-Days }}">{{ c-Days }}</h6>
				</div>
				<div class="col-xs-3 countdown__item">
					<h2 id="hours" class="countdown__amount hours">00</h2>
					<h6 class="countdown__title" kjb-settings-id="{{ kjb-Hours }}">{{ c-Hours }}</h6>
				</div>
				<div class="col-xs-3 countdown__item">
					<h2 id="minutes" class="countdown__amount minutes">00</h2>
					<h6 class="countdown__title" kjb-settings-id="{{ kjb-Minutes }}">{{ c-Minutes }}</h6>
				</div>
				<div class="col-xs-3 countdown__item">
					<h2 id="seconds" class="countdown__amount seconds">00</h2>
					<h6 class="countdown__title" kjb-settings-id="{{ kjb-Seconds }}">{{ c-Seconds }}</h6>
				</div>
			</div>
		</div>
	</div>
</div>


    {% schema %}
{
  "name": "(18) CTA Countdown",
  "elements": [
    {
      "type": "header",
      "content": "Countdown",
      "style": "subheading"
    },
    {
        "type": "text",
        "id": "countdown_end_time",
        "label": "End Time",
        "default": "2017-10-14 12:00:00",
        "info": "You MUST use the following format: YYYY-MM-DD HH:MM:SS (24-Hour Clock)"
      },
      {
        "type": "text",
        "id": "countdown_timezone",
        "label": "Timezone",
        "default": "America/Los_Angeles",
        "info": "Choose your timezone from the map [here](momentjs_timezone)."
      },
      {
        "type": "header",
        "style": "subheading",
        "content": "Language"
      },
      {
        "type": "text",
        "id": "days_text",
        "label": "Days",
        "default": "DAYS"
      },
      {
        "type": "text",
        "id": "hours_text",
        "label": "Hours",
        "default": "HOURS"
      },
      {
        "type": "text",
        "id": "minutes_text",
        "label": "Minutes",
        "default": "MINS"
      },
      {
        "type": "text",
        "id": "seconds_text",
        "label": "Seconds",
        "default": "SECS"
      }
      
  ],
  "presets": [
    {
      "name": "(18) CTA Countdown",
      "category": "Content",
      "blocks": [],
      "settings": {
      }
    }
  ]

}
    {% endschema %}
```