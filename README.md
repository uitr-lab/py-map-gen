# py-map-gen

Easy to use map generator, generates a self contained html file that displays a hex-map, square-map, or custom (shp file) polygon histogram map

1. Get an access-token from mapbox.
2. Update config in VIS.ipynb
3. Generate output map 

```python

config={
    "input": "./example/Book3.xlsx",
    "map": {
        
        # go to https://www.mapbox.com/ sign up and find your access token
        "access-token": "XXXXXXXXX",
        "options-json":{
            "style": "dark", # [light, dark, street]
            "grid":"hex", # [hex, square] default: hex, 
            "source-color": "#d00b8abd",  # [00-ff], #{a}{r}{g}{b}
            "dest-color": "#b0c334eb",
            "hex-grid-zoom":8, # only if using hexmap
            "square-size":1000, # meters, only if using square cells
            "min-height":50,
            "height-scale":30,
            "arc-width":1,
            "data-sample":1,
            "arc-opacity":0.6, # if 0, then arcs are ommited
            "arc-sample":0.2,
            "grid-opacity":0,
        }
    }
}
```

![Hex Grid: 8z with arcs](https://github.com/user-attachments/assets/34c0e6fa-286b-4ea0-ad36-d06365693f53)

```python
config={
    "input": "./example/Input_Arc.csv",
    "map": {
        
        # go to https://www.mapbox.com/ sign up and find your access token
        "access-token": "XXXXXXXXX",
        "options-json":{
            "style": "light", # [light, dark, street]
            "grid":"square", # [hex, square] default: hex, 
            "source-color": "#d00b8abd",  # [00-ff], #{a}{r}{g}{b}
            "dest-color": "#b0c334eb",
            "hex-grid-zoom":8, # only if using hexmap
            "square-size":400, # meters, only if using square cells
            "min-height":50,
            "height-scale":1,
            "arc-width":1,
            "data-sample":1,
            "arc-opacity":0.2, # if 0, then arcs are ommited
            "arc-sample":0.02,
            "grid-opacity":0.2,
        }
    }
}
```

<img width="1370" alt="Square Grid: 400m with arcs" src="https://github.com/user-attachments/assets/a120b88f-4b76-4c2b-aeae-c3732a331779" />
