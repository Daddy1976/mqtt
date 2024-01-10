This is my use for Victron Energy and controlling the solar system with HomeAssistant

To use, copy all items to the created MQTT directory in HomeAssistant (File Editor) and insert all items with the yaml extension into the subdirectory.

Before using in each file, you need to search and change YourVictronID to "Your Victron ID" every single name

you also need to check the path in state_topic and command_topic

example:

state_topic: 'N/my_victron_id/vebus/276/Mode'

use mqtt explorer to check to the relevance of the path for functionality

it may be necessary to:
state_topic: 'N/your_victron_id/vebus/279/Mode'

note the different number behind the vebus. it may be different for you because victron assigns the port addressing itself.
This also applies to Pylontech and MPPT and other devices

install and configure mqtt integration
https://www.home-assistant.io/integrations/mqtt

edit configuration.yaml in HA and add this text somewhere at the end of the file

mqtt: !include_dir_merge_list mqtt/

restart homeassistant

go to settings -> devices and services -> mqtt

you should see the devices there
