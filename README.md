#Japan Map (jQuery plugin)

jQuery plugin to show clickable map of prefectures (or area) of Japan.

[Download, Quick Start, Examples, Usage] (http://takemaru-hirai.github.io/japan-map/)

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

Please visit [the Project Page] (http://takemaru-hirai.github.io/japan-map/) to see more informations.


## Authors

[Takemaru Hirai](https://github.com/takemaru-hirai)

##License

Japan Map is released under the [MIT License](http://opensource.org/licenses/MIT).
