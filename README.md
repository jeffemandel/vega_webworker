# vega_webworker
Demonstrates use of a web worker to generate events to control a Vega visualization

Vega has limited ability to update a signal based on a timer; these are limited to Number. A signal
can be updated by an event posted to a DOM element such as window:
````
"on": [
  {
    "events": "window:myupdate",
    "update": "event.detail"
  }
]
````
This example demonstrates use of a web worker to generate these events
