# poc-transformation-net-core
POC to Settings Transformation in .Net core 3.1.

Default priority to capture values:
1. Environment variables
2. appSettings.environmentName.json
3. appSettings.json

# Project PocTransformationGood
Easiest way to use transformation in .net core, also easiest to adapt legacy to use transformation.
In this project was used interface IConfiguration to capture key and values settings, respecting default priority, and to get the value was used GetValue, passing key name by hardcoded string.

# Project PocTransformationTop
Better and recommended way to use transformation in net core. In this project was used interface ILogger and a personalized object, created based on settings values. 
To bind object was used `services.Configure<Object>(Configuration.GetSection("nameSection"));` and to get the value only is necessary access object attribute.
