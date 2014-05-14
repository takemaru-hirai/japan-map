#Japan Map (jQuery plugin)

jQuery plugin to show clickable map of prefectures (or area) of Japan.

[Quick Guide] (http://takemaru-hirai.github.io/japan-map/)

## Installation

Include the script after the jQuery library:

```html
<script src="/path/to/jquery.japan-map.js"></script>
```

## Usage

Creating the clickable map of Japan:

```javascript
$(target).japanMap( options );
```

EXAMPLE - Alert prefecture name when clicked:

```javascript
$(target).japanMap({
    onSelect : function(data){
        alert(data.name);     // "北海道" (Hokkaido) will be shown on dialog when you click Hokkaido Island.
    }
});
```

## Options

Options must be an object, optionally containing the next parammeters:

### selection

Set which type of selection is used, "prefecture" or "area". If you set "area", you have to give an array of object to 
"areas" parameter.

    selection: "area",
    areas: areasObject
    
"areas" object array must define like following. "areas.prefectures" parameter includes prefecture code (from 1 to 47) which belongs to the area.

```javascript
    areasObject = [
        ...
        {
            "code": 3 ,             // any code you classify the areas
            "name":"関東地方",      // name of the area
            "color":"#84b0f6",      // optional, however, if set Areas can be classified by different colors.
            "hoverColor":"#c1d8fd",  // optional. If not not, 20% brightened when the area hovered.
            "prefectures":[8,9,10,11,12,13,14]  // prefecture code (defined by government of Japan) belongs to the area
        },
        ...
    ];
```    

## Authors

[Takemaru Hirai](https://github.com/takemaru-hirai)

##License

Japan Map is released under the [MIT License](http://opensource.org/licenses/MIT).
