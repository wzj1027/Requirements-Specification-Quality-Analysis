## 4. Functional Requirements

This section provides a description of the functional requirements. There is a DH
Use Case Model in the Appendix, which provides an overview of the system
functionality and shows the relationships between the DigitalHome System
entities.

### 4.1 General Requirements

1. The DigitalHome System shall allow a web-ready computer, cell phone
or PDA to control a home's temperature, humidity, lights, security, and
the state of small appliances.
2. The communication center of the DH system shall be a DH home web
server, through which a user shall be able to monitor and control home
devices and systems.
3. Each DigitalHome shall contain a master control device (the DH
Gateway Device) that connects to the home’s broadband Internet
connection, and uses wireless communication to send and receive
communication between the DigitalHome system and the home
devices and systems.
4. The DigitalHome shall be equipped with various environmental
controllers and sensors (temperature controller-sensors: thermostats,
humidity controller-sensors: humidistats, contact sensors, security
sound and light alarms, and power switches).
5. Using wireless communication, sensor values can be read and saved
in the home database.
6. Controller values can be sent to controllers to change the DH
environment.

### 4.2 Thermostat Requirements

1. The DigitalHome programmable thermostat shall allow a user to
monitor and control a home’s temperature from any location, using a
web ready computer, cell phone, or PDA.
    1. A DH user shall be able to read the temperature at a thermostat
    position.
    2. A DH user shall be able to set the thermostat temperatures to
    between 60 ° F and 80 ° F, inclusive, at one degree increments.
2. Up to eight thermostats shall be placed in rooms throughout the home.
    1. The thermostats may be controlled individually or collectively, so
    that temperature can be controlled at different levels in different
    home spaces.
    2. A single thermostat shall be placed in an enclosed space (e.g.,
    a room in the house) for which the air temperature is to be
    controlled.
    3. For each thermostat, up to twenty-four one hour settings per
    day for every day of the week can be scheduled.
    4. If a thermostat device allows a user to make a manual
    temperature setting, the setting shall remain in effect until the
    end of the planned or default time period, at which time the
    planned or default setting will be used for the next time period.
3. A thermostat unit shall communicate, through wireless signals, with the
master control unit.
4. The system shall support Fahrenheit and Celsius temperature values.
5. The system shall be compatible with a centralized HVAC (Heating,
Ventilation and Air Conditioning) systems: gas, oil, electricity, solar, or
a combination of two or more. The system shall adhere to the
standards, policies and procedures of the American Society of Heating,
Refrigerating and Air-Conditioning Engineers [ASHRAE 2010].

### 4.3 Humidistat Requirements

1. The DigitalHome programmable humidistat shall allow a user to
    monitor and control a home’s humidity from any location, using a web
    ready computer, cell phone, or PDA.
    1. A DH user shall be able to read the humidity at a humidistat
    position.
    2. A DH user shall be able to set the humidity level for a
    humidistat, from 30% to 60%, inclusive a 1% increments.
2. Up to eight humidistats shall be placed in rooms throughout the home.
    1. A single humidistat shall be placed in an enclosed space (e.g., a
    room in the house) for which the humidity is to be controlled.
    2. If a humdistat device allows a user to make a manual
    temperature setting, the setting shall remain in effect until the
    end of the planned or default time period, at which time the
    planned or default setting will be used for the next time period.
    3. For each humidistat, up to twenty-four one hour settings per day
    for every day of the week can be scheduled.
3. A DigitalHome system shall use wireless signals to communicate,
through the master control unit, with the humidistats.

### 4.4 Security System Requirements

1. The DigitalHome security system consists of contact sensors and a set
security alarms.
    1. A DigitalHome system shall be able to manage up to fifty door
    and window contact sensors.
    2. A DigitalHome system shall be able to activate both light and
    sound alarms: one sound alarm and one light alarm subsystem,
    with multiple lights.
2. When a security breach occurs and a contact sensor is set OPEN, the
alarm system shall be activated.

### 4.5 Appliance Management Requirements

1. The DigitalHome programmable Appliance Manager shall provide for
management of a home’s small appliances, including lighting units, by
allowing a user to turn them on or off as desired.
2. The Appliance Manager shall be able to manage up to one hundred
115 volt, 10 amp power switches.
3. The system shall be able to provide information about the state of a
power switch (OFF or ON), indicating the whether an appliance
connected to the power switch is OFF or ON.
4. The system shall be able to change the state of a power switch (OFF
to ON, or ON to OFF), in turn changing the state of an appliance
connected to the power switch.
5. If a user changes the state of power switch device manually, the
device shall remain in that state until the end of the planned or default
time period, at which time the planned or default setting will be used for
the next time period.

### 4.6 DH Planning and Reporting Requirements

1. DigitalHome Planner shall provide a user with the capability to direct
the system to set various preset home parameters (temperature,
humidity, security contacts, and on/off appliance/light status) for certain
time periods.
2. DigitalHome provides a monthly planner.
    1. For a given month and year, a user shall be able to create or
    modify a month plan that specifies for each day, for up to four
    daily time periods, the environmental parameter settings
    (temperature, humidity, contact sensors and power switches).
    2. A user shall be able to override planned parameter values,
    through the DH website, or if available, through manual
    switches on household devices
3. For a given month and year, in the past two years, DigitalHome shall
be able to provide a report on the management and control of the
home.
    1. The month report shall contain daily average, maximum (with
    time) and minimum (with time) values of temperature and
    humidity for each thermostat and humidistat, respectively.
    2. The month report shall provide the day and time for which any
    security breaches occurred, that is, when the security alarms
    were activated.
    3. The month report shall provide a section that indicates the
    periods of time when the DH System was not in operation..