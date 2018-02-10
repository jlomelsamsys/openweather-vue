# Weather App with Vue.js & OpenWeatherMap API

The overall goal of this exercice is to display the weather of one city for instance with the OpenWeatherMap API and Vue.js.

![WeatherApp](img/Weather_Example.png)

## Prerequise
Notions in vue.js, Javascript, HTML.

## Use of vue.js

>  https://vuejs.org/

To install vue.js, you have several choices. It's simple because it's Javascript library.


Here, we will use a Content Delivery Network (CDN).

You can use a Content Delivery Network (CDN). This is a special server whose aim is to deliver data to users with high availibility and hig performance. 

In this case it is even simpler.
You have the links available on the site https://vuejs.org/. 
Then you juste provide a script tag. Here is the recommended link : 

```javascript

<script src="https://cdn.jsdelivr.net/npm/vue@2.5.13/dist/vue.js"></script> 

```
The version 2.5.13 can be changed.

 There are other ways to install vue.js but they only have to be considered for large applications You have all the details on the site.

## Use of Bootstrap

Bootstrap is a project that provides a set of styles and Javascript tools for developping a responsive and nice application without having to think a lot about CSS.

Here, we will use a CDN too.

````HTML
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">

````

## Index.html

Create an index.html in your directory

````HTML
<!DOCtyPE html>
<html>
<head>
    <title>Weather App</title>
</head>

...

````
## App.js

Create an app.js file.

```javascript
new Vue ({
    el: '#app',
    data: {
        city:''
    },

    methods: {
        getData: function(){
            ...
        }
    }
})
```
In this file, create a function to get the data of the weather via the API.

## App's form & Components (Vue, JQuery) 

In your file HTML, call your file ".js" and the library jquery.

````HTML
<script src="app.js" type="text/javascript" charset="utf-8"></script>

<script src="http://code.jquery.com/jquery-3.3.1.js" integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60=" crossorigin="anonymous"></script>
````

## Use vue.js tags to the form

You can use the differents directives such as :
- v-on
- v-if / v-else
- v-for
- v-model
- ...

## OpenWeatherMap

- Go to https://openweathermap.org/ and sign-up and sign-in (to get the key app)

![OpenWeather](img/API_Key.png)

To get access to weather API you need an API key whatever account you choose.

- How to use API Key in API Call : http://openweathermap.org/appid
- Endpoint for any API calls : api.openweathermap.org
- API documentation : http://openweathermap.org/api
- Example of API call : Weather in London

````JSON
{"coord":{"lon":-0.13,"lat":51.51},"weather":[{"id":802,"main":"Clouds","description":"scattered clouds","icon":"03n"}],"base":"stations","main":{"temp":273.79,"pressure":1017,"humidity":59,"temp_min":272.15,"temp_max":275.15},"visibility":10000,"wind":{"speed":2.6,"deg":350},"clouds":{"all":36},"dt":1517944800,"sys":{"type":1,"id":5091,"message":0.0029,"country":"GB","sunrise":1517902169,"sunset":1517936430},"id":2643743,"name":"London","cod":200}
````

## API

API Call : http://api.openweathermap.org/data/2.5/forecast?id=524901&APPID={APIKEY}

|Méthode HTTP       |     Action     |
| ------------- | -------------   |
| GET       |    Read      |
| POST     |      Create |
| PUT        |      Update/Replace     |
| PATCH        |      Update/Modify     |
| DELETE        |      Delete     |