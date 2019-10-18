`IoT.Hass.Farm` ![Travis branch](https://api.travis-ci.org/josemotta/IoT.Hass.Farm.svg?branch=master)

# IoT.Farm Regional Center

**An IoT Farm for supervisory, control & data acquisition systems.**

## Water Process

The picture describes a typical process, detailed at [IoT.Hass.Farm](https://github.com/josemotta/IoT.Hass.Farm), that pumps water from well and fills a big water storage placed on a high tower. The plumbing connects to water points located on the near buildings, equipped with secondary water tanks that are filled by gravity and should also be monitored.

![water-process-2](https://user-images.githubusercontent.com/86032/67102821-84654e00-f19a-11e9-92ec-f38b84c0cd15.png)

A couple pumps work together to fill the water storage on the top of high tower:

- The first stage is twenty five meters below surface in the well, powered by a thin-vertical-pump, located inside the plumbs. It pushes water to a small intermediary tank, located at surface level.
- A second fast-pump is responsible for moving the water from the intermediary tank to the big water storage placed on the high tower.
- The fast-pump starts when the intermediary tank is full and stops when it is empty. The command logic for this synchronization is already set and is not being considered here now.

The objective of this projecty is to gather info from big water tank to:

![castle-45-live super panel 2019-9-2 Influx-linha-dagua](https://user-images.githubusercontent.com/86032/67041426-06eb0080-f0fc-11e9-99d9-d4ad083cbfcb.png)

- **measure water flow:** get real-time tank level using the [ToF (time of flight) sensor](https://github.com/josemotta/IoT.Hass.Farm/tree/master/_tank);
- **extract seasonal data during the year:** how much time does it take to fill the [intermediary tank](https://github.com/josemotta/IoT.Hass.Farm/tree/master/_pump)?
- **forecast water availability from nature:** are we consuming too much?
- **detect anomalies on water availability:** is it possible to anticipate a water shortage?

