## Note: garmin need secret_string(and in Actions) get `python run_page/garmin_sync.py ${secret_string}` if cn `python run_page/garmin_sync.py ${secret_string} --is-cn`


[简体中文](README-CN.md) | English

This project is based on [running_page](https://github.com/yihong0618/running_page) and adds support for multi sports types. Follow the steps in the origin repo to deploy.

## New Features

1. support multi sports types, like Ride/Hike/Swim/Rowing
1. support [RoadTrip(GoogleMaps)](#roadtripgooglemaps), show Road Trip on maps

## Customize

### Change Sports Color

- Modify Ride Color: `RIDE_COLOR` in `src/utils/const.js`

### Add Sports Type

- Modify `TYPE_DICT` & `MAPPING_TYPE` in `scripts/config.py`
- Add Type Name and add it into `RUN_TITLES` in `src/utils/const.js`
- Modify `colorFromType` & `titleForRun` in `src/utils/util.js`
- refer to [commit](https://github.com/ben-29/workouts_page/commit/f3a35884d626009d33e05adc76bbc8372498f317)

---

### RoadTrip(GoogleMaps)

<details>
<summary>Import KML from Google Maps</summary>

1. Create a map in [Google Maps](https://www.google.com/maps/d/) (keep the route in one Layer)
2. Export Layer to KML file
3. Rename the file to `import.kml` and place it into `scripts`
4. Modify `scripts/kml2polyline.py`, fill in the trip info



5. Execute in Console

```python
python3(python) scripts\kml2polyline.py
```

</details>

# Special thanks

- @[yihong0618](https://github.com/yihong0618) for Awesome [running_page](https://github.com/yihong0618/running_page), Great Thanks
