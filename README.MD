![image](https://github.com/magroski/miami-vice-meters/blob/master/sample.png)

This is a skin and layout bundle created to be used with [Rainmeter](https://www.rainmeter.net/).

The skin is composed of 4 different modules:
- Temps (CPU + GPU, with colors changing based on current temp)
- System (CPU load histogram, and RAM usage)
- Disks
- Network (Current IP, Download and Upload gauges)

They sit on top of a lightly tinted overlay that allows them to easily blend with most wallpapers.

Everything is set on variables, so the modules are pretty easy to edit.


## Compatibility 

It was built upon Rainmeter 4.3 Final Release, but it may work with older versions.

Temps are monitored using the MSIAfterBurner plugin included on the .rmiskin bundle, however you need to install [RivaTuner Statistics Server](https://www.guru3d.com/files-details/rtss-rivatuner-statistics-server-download.html) for it to work.

## FAQ

1. Is it possible to use CoreTemp?

Kinda. CoreTemp plugin comes out-of-the box with Rainmeter, and the Coretemp app that needs to be installed is lighter than RivaTuner, but it lacks GPU temp support. To make this skin work with CoreTemp, edit the following section of Temps.ini:
Replace
```ini
    Plugin=Plugins\MSIAfterburner.dll
    DataSource=CPU temperature
```
With
```ini
    Plugin=CoreTemp
    CoreTempType=MaxTemperature
```

2. Is it possible to change the background transparency?

Yes. On the [Rainmeter] section of each .ini, change the value of `SolidColor=0,0,0,25` to whatever you like. The format is `Red, Green, Blue, Opacity` with values ranging from 0 to 255.