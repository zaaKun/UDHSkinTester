### For your skin to be added to UDH, it will have to be manually approved ! You can submit your skin at [URL TO COME, @me for now]
# Your skin will be automatically rejected if it doesn't fill these two conditions :
* You must have the rights to modify and use all images without attribution
* The Width to Height ratio must be a minimum of 3.0 (example : 600/200, 640/128...)

Here's an example of the default skin :
```json
{
    "Name": "Default",
    "Codename": "default",
    "Description": "Default avatar",
    "AvatarSize": 128,
    "AvatarX": 36,
    "AvatarY": 40,
    "Background": "resources/background.png",
    "Layers": [
        {
            "Image": "resources/foreground.png",
            "StartX": 30,
            "StartY": 20,
            "Width": 640,
            "Height": 209,
            "Modules": [
                {
                    "Type": "AvatarBorder",
                    "StartX": 6,
                    "StartY": 20
                },
                {
                    "Type": "XpBar",
                    "StartX": 150,
                    "StartY": 42,
                    "Width": 360,
                    "Height": 18,
                    "OutsideStrokeColor": "#778899FF",
                    "OutsideFillColor": "#F5F5F5FF",
                    "InsideStrokeColor": "#FFFFFF00",
                    "InsideFillColor": "#32CD32FF"
                },
                {
                    "Type": "XpBarInfo",
                    "StartX": 315,
                    "StartY": 57,
                    "Width": 360,
                    "Height": 18,
                    "Font": "Consolas",
                    "FillColor": "#000000FF",
                    "StrokeColor": "#00000000",
                    "FontPointSize": 17
                },
                {
                    "Type": "Username",
                    "StartX": 150,
                    "StartY": 38,
                    "FontPointSize": 34,
                    "Font": "Consolas",
                    "StrokeColor": "#8A2BE2FF",
                    "FillColor": "#00BFFFFF",
                    "StrokeAntialias": true,
                    "StrokeWidth": 0.4
                },
                {
                    "Type": "TotalXp",
                    "StartX": 535,
                    "StartY": 83,
                    "FontPointSize": 17,
                    "Font": "Consolas",
                    "FillColor": "#000000FF"
                },
                {
                    "Type": "XpRank",
                    "StartX": 535,
                    "StartY": 108,
                    "FontPointSize": 17,
                    "Font": "Consolas",
                    "FillColor": "#000000FF"
                },
                {
                    "Type": "KarmaRank",
                    "StartX": 535,
                    "StartY": 153,
                    "FontPointSize": 17,
                    "Font": "Consolas",
                    "FillColor": "#000000FF"
                },
                {
                    "Type": "KarmaPoints",
                    "StartX": 535,
                    "StartY": 130,
                    "FontPointSize": 17,
                    "Font": "Consolas",
                    "FillColor": "#000000FF"
                },
                {
                    "Type": "Level",
                    "StartX": 220,
                    "StartY": 140,
                    "FontPointSize": 50,
                    "Font": "Consolas"
                }
            ]
        }
    ]
}
```
# Skin
The skin has the following attributes :
* Name
    * A name for the skin
* Codename
    * Lowercap, codename for the skin
* Description
    * A description for the skin
* AvatarSize
    * Size of the avatar in pixel. 128 recommended
* AvatarX
    * X Position of the avatar in pixels
* AvatarY
    * Y Position of the avatar in pixels
* Background
    * Path to the background
* Layers
    * A list of Layer

# Layer
They are drawed in the order they're defined
Each layer has the following attributes :
* Image
    * (optional) path to the image
* StartX, StartY
    * Offset from the background, affects all the modules inside
* Width, Height
    * Width and Height in pixel
* Modules
    * A list of Module


# Modules
For each module, you must specify the Type so reflection works correctly. The Type is simply the name of the module as written below.
All modules have a StartX and StartY, and so it will not be specified again.

Here's a quick rundown of each attributes you will be able to find :

* StartX, StartY :
    * double, position from the top left
* Width, Height
    * double, in pixels
* FontPointSize
    * Size of the font in px
* TextAntiAlias/StrokeAntialias
    *  boolean
* StrokeColor/FillColor
    * Color as an hex string with alpha (example : #FF55FF00)
* Font
    * Font name
* StrokeWidth
    * double, width of the stroke

Here's the available modules :
* AvatarBorder : Draw a square shape around the avatar
    * Available attributes 
        * Size
* XpBar
    * Width
    * Height
    * StrokeWidth
    * OutsideStrokeColor
    * OutsideFillColor
    * InsideStrokeColor
    * InsideFillCoor
* XpBarInfo
    * StrokeWidth
    * FillColor
    * StrokeColor
    * Font
    * FontPointSize
* Level
    * StrokeAntiAlias
    * TextAntiAlias
    * StrokeColor
    * StrokeWidth
    * FillColor
    * Font
    * FontPointSize
* Username
    * StrokeAntiAlias
    * TextAntiAlias
    * StrokeColor
    * StrokeWidth
    * FillColor
    * Font
    * FontPointSize
* TotalXp
    * StrokeAntiAlias
    * TextAntiAlias
    * StrokeColor
    * StrokeWidth
    * FillColor
    * Font
    * FontPointSize
* XpRank
    * StrokeAntiAlias
    * TextAntiAlias
    * StrokeColor
    * StrokeWidth
    * FillColor
    * Font
    * FontPointSize
* KarmaPoints
    * StrokeAntiAlias
    * TextAntiAlias
    * StrokeColor
    * StrokeWidth
    * FillColor
    * Font
    * FontPointSize
* KarmaRank
     * StrokeAntiAlias
    * TextAntiAlias
    * StrokeColor
    * StrokeWidth
    * FillColor
    * Font
    * FontPointSize