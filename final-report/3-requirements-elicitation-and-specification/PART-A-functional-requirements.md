Non-functional and prcoess requirements (possibly not included in final report):

- Arduino SHALL be connected via ethernet, to a central control system on an isolated local sub-LAN.

- Control system SHALL only allow communications to a vetted system that provides an interface to the end user.
- Control system SHALL use MQTT to communicate with Arduino.
- Control system SHALL handle all database work, and only allow a whitelist of commands from any user interface system.
- Control system and web interface SHALL use strong authentication and encryption of communication channels.

- Web interface SHOULD be held on a separate system than the central control system.
- Web interface SHALL use JSP's Expression Language (EL) to display any items where no updates to state are required.
- Web interface SHALL use JSP tags whenever a servlet needs to display information to a webpage.
- Manually-written servlet classes for the web interface SHALL only be used as coordinating objects.
- Web interface SHALL only use the service API provided by the control system.


Functional requirements:

- Arduino SHALL regularily mist roots, with the schedule set by the control system.
- Arduino SHALL turn on/off lights when commanded to do so by the control system.
- Arduino SHALL mix nutrient solution with water prior to fogging.
- Arduino SHALL routinely flush out built-up salts on the foggers with fresh water.
- Arduino SHALL keep the humidity of the top chamber to a level set by the control system.
- Arduino SHALL keep the temperatures of both bottom and top chambers to levels set by the control system. 
- Arduino SHALL send notifications regarding unplanned events to the control system for display to the user and possible autonomous decision-making.
- Arduino SHALL be able to automatically perform initial setup with the control system.
- Arduino SHALL cut off power to the intense growing lights upon the door opening and switch to viewing lights (assuming the lights should be on at that time.)

- Control system SHALL maintain history of the current growth cycle.
- Control system SHALL send directives to change Arduino's state when needed.
- Control system SHALL support multiple growing systems.
- Control system SHALL offer encrypted database backups.

- Web interface SHALL be able to display all non-secret information (private keys) held on the control system and perform all activities allowed to an end-user. This includes but is not limited to setting misting and lighting schedules, target temperature/humidity values, and nutrient ratios.
