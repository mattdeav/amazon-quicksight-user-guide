# Geospatial Limits & Troubleshooting<a name="geospatial-limits-and-troubleshooting"></a>

There are some limitations to working with geospatial data\. Be aware of the following and make sure that your data follows the guidelines listed, so that it works properly in geospatial visuals:

+ The map chart identifies State, City, County, and Zipcode as GeoEntity types\. After it does so, it converts each to a latitude and longitude pair to display on the map\. This automatic conversion is currently supported for US data only\. In other regions, automatic conversion is not supported\. However, you can still use the map chart with latitude and longitude pairs for locations outside the US\. 

+ Geospatial data can't be ambiguous\. For example, suppose that the data contains a city named Springfield, but no state is specified\. Because multiple states have a city named Springfield, it isn't possible to geocode the location to a specific point on a map\. To avoid this problem, you can add enough geographical data to make it clear exactly what point should be shown on a map chart\.

+ Some places aren't yet supported, and trying to use these places can cause errors\. If your geography follows all the guidelines listed here, and still generates errors, contact the Amazon QuickSight team from within the Amazon QuickSight console\. 

+ The country that you choose on the **Create hierarchy** screen becomes the default for that data set\. To change it, edit or create a hierarchy, and choose a different country\. 

+ Latitude values must fall within the range \-90 to 90\. Longitude values must fall within the range \-180 to 180\. Amazon QuickSight skips anything outside these ranges\. Out\-of\-range points can't be mapped on a map chart\. 

+ Latitude and longitude values must be numeric\. For example, the map point indicated by **28\.5383355 \-81\.3792365** is compatible with Amazon QuickSight\. But **28° 32' 18\.0096'' N 81° 22' 45\.2424'' W** is not\. You can use a calculated field with a formula to create a numeric latitude and longitude out of character strings\. The following examples show different ways that you can create calculated field formulas in Amazon QuickSight, to parse GPS latitude and longitude into numeric latitude and longitude\. 

The following sample converts latitude and longitude to numeric format from separate fields\. For example, if you parse **51° 30' 26\.4636'' N 0° 7' 39\.9288'' W** using space as a delimiter, you can use something like the following sample to convert the resulting fields to numeric latitude and longitude\. \(In this example, the seconds are followed by two single quotes; if your data has a double quote instead, then you can use `strlen(LatSec)-1) )` instead of `strlen(LatSec)-2) )`\.

```
/*Latitude*/
        ifelse( 
        LatDir = "N", 
        parseInt(split(LatDeg, "°", 1)) + 
            (parseDecimal(split(LatMin, "'", 1) ) /60) +
            (parseDecimal((substring(LatSec, 1, strlen(LatSec)-2) ) ) /3600), 
        (parseInt(split(LatDeg, "°", 1)) + 
            (parseDecimal(split(LatMin, "'", 1) ) /60) +
            (parseDecimal((substring(LatSec, 1, strlen(LatSec)-2) ) ) /3600)) * -1
        )
        
/*Longitude*/
        ifelse( 
        LongDir = "E", 
        parseInt(split(LongDeg, "°", 1)) + 
            (parseDecimal(split(LongMin, "'", 1) ) /60) +
            (parseDecimal((substring(LongSec, 1, strlen(LongSec)-2) ) ) /3600), 
        (parseInt(split(LongDeg, "°", 1)) + 
            (parseDecimal(split(LongMin, "'", 1) ) /60) +
            (parseDecimal((substring(LongSec, 1, strlen(LongSec)-2) ) ) /3600)) * -1
        )
```

If your data doesn't include the symbols for degree, minute and second, the formula looks like the following\.

```
/*Latitude*/
    ifelse( 
        LatDir = "N", 
        (LatDeg + (LatMin / 60) + (LatSec / 3600)), 
        (LatDeg + (LatMin / 60) + (LatSec / 3600)) * -1
    )
    
/*Longitude*/
    ifelse( 
        LongDir = "E", 
        (LongDeg + (LongMin / 60) + (LongSec / 3600)), 
        (LongDeg + (LongMin / 60) + (LongSec / 3600)) * -1
    )
```

The following sample converts **53°21'N 06°15'W** to numeric format\. However, without the seconds, this value doesn't map as accurately\.

```
/*Latitude*/
ifelse( 
    right(Latitude, 1) = "N", 
    (parseInt(split(Latitude, '°', 1)) +
        parseDecimal(substring(Latitude, (locate(Latitude, '°',3)+1),  2) ) / 60) , 
    (parseInt(split(Latitude, '°', 1)) +
        parseDecimal(substring(Latitude, (locate(Latitude, '°',3)+1),  2) ) / 60) * -1
)

/*Longitude*/
ifelse( 
    right(Longitude, 1) = "E", 
    (parseInt(split(Longitude, '°', 1)) +
        parseDecimal(substring(Longitude, (locate(Longitude, '°',3)+1),  2) ) / 60) , 
    (parseInt(split(Longitude, '°', 1)) +
        parseDecimal(substring(Longitude, (locate(Longitude, '°',3)+1),  2) ) / 60) * -1
)
```

The formats of GPS latitude and longitude can vary, so customize your formulas to match your data\. For more information, see the following links:

+ [Degrees Minutes Seconds to Decimal Degrees](https://www.latlong.net/degrees-minutes-seconds-to-decimal-degrees) on LatLong\.net

+ [Converting Degrees/Minutes/Seconds to Decimals using SQL](https://stackoverflow.com/questions/12186110/converts-degrees-minutes-seconds-to-decimals-using-sql) on Stack Overflow

+ [Geographic Coordinate Conversion](https://en.wikipedia.org/wiki/Geographic_coordinate_conversion) on Wikipedia