This is my use for Victron Energy and controlling the solar system with HomeAssistant

To use, copy all items to the created MQTT directory in HomeAssistant (File Editor) and insert all items with the yaml extension into the subdirectory.

install and configure mqtt integration
https://www.home-assistant.io/integrations/mqtt

edit configuration.yaml in HA and add this text somewhere at the end of the file
mqtt: !include_dir_merge_list mqtt/
restart homeassistant

go to settings -> devices and services -> mqtt

you should see the devices there
