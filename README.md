## home-assistant-intents-pl
Common workspace for polish group contributing into home assistant intents

### List of all device_class:
https://www.home-assistant.io/docs/configuration/customizing-devices/#device-class

### List of domains (30 in total):
  - alarm_control_panel
  - automation
  - binary_sensor
  - button
  - calendar
  - camera
  - climate
  - cover
  - device_tracker
  - group
  - input_boolean
  - light
  - lock
  - media_player
  - number
  - person
  - proximity
  - remote
  - scene
  - schedule
  - script
  - select
  - sensor
  - sun
  - switch
  - timer
  - update
  - vacuum
  - weather
  - zone
  
  Script to fetch domains from ha cli:
  ```
{%- for d in states | groupby('domain') %}
  {% if loop.first %}{{loop.length}} Domains:
  {% endif %}- {{ d[0] }}: {{d[0]|count}}
{%- endfor %}
```
