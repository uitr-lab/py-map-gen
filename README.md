# py-map-gen

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

![output](https://github.com/user-attachments/assets/34c0e6fa-286b-4ea0-ad36-d06365693f53)
