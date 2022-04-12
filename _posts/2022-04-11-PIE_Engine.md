## PIE-Engine

This script is to using PIE-Engine do something. And this kind of things always have the same process. Maybe this is the so called 'algorithm'.
Which just means 'the way to do something'.

### STEP1 roi

Almost everytime when we want to a research aboutremote sensing, we always find the research region at first.

This time we choose the Huainan area.
var roi = pie.Geometry.Polygon([[[116.50,32.78],[116.75,32.78],[116.75,32.94],[116.50,32.94],[116.50,32.78]]], null);

And we want to show this roi.
Map.addLayer(roi)

At the same time, it's important to center the object.
Map.centerObject(roi, 12);

### STEP2 datacollection

The second step is the core of the process because this is related to the datacollection. We should always remember that 
datacollection is the core of nearly every process. No matter what kind of research we want to do. Most of the time the data
collection is the image, just like Landsat, Sentinel or Gaofen. Sometime it's Featurecollection, when we want to research the 
vector.

This time we choose the Gaofen. And the process about datacollection always have the following steps.

#### 2.1 choose and import the collection

Find the collection we want to use and import them.
We use Gaofen-1 as a example.
var gf1 = pie.ImageCollection("GF1/L1A/BCD_FUSION").

#### 2.2 filter the collection

We always filter many things, because we don't need every images.
filterBounds and filterDate are most useful.
var gf1 = pie.ImageCollection("GF1/L1A/BCD_FUSION")
            .filterBounds(roi)
            .filterDate('2020-02-20','2020-10-01')
            .first();

#### 2.3 show them

Then we just show it
Map.addLayer(gf01.select(["B3", "B2", "B1"]), {min: 500, max: 2000}, "gf1");
