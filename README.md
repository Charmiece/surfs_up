# surfs_up
## Overview
The purpose of this project was to analyze the temperature trends in June and December for Oahu, Hawaii in order to determine year-round sustainability of a surf and ice cream shop business.

## Results
<img width="176" alt="Screen Shot 2022-04-16 at 3 07 53 AM" src="https://user-images.githubusercontent.com/93438483/163665494-98831b2b-ab8b-46dd-81ea-e6e4acb302ca.png"> <img width="166" alt="Screen Shot 2022-04-16 at 3 08 52 AM" src="https://user-images.githubusercontent.com/93438483/163665521-88936d36-20e0-4d07-b208-1c27475ecfc4.png">

* The range in June is 64 to 85 degrees. While the range in December is 56 to 83 degrees.
* The average in June is 75 degress and 71 in December.
* The spread in June is 21 degrees and 27 in December.

## Summary
Even with the difference in the range of temperatures, surf and ice cream shop would still be viable. I would perform precipitation queries because that effects the amount of people surfing and eating ice cream. One would be the total precipitation...
session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
The next would be the same but at active stations...
session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 6).all()
session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 12).all()
