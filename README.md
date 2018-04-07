# Mobile Device Frames
#### Add Simple CSS iPad Frames to preview your Web App

Mobile Device Frames by @AlanThinks  
Version 1.0  
www.AlanThinks.com  
www.github.com/alanthinks  

**Includes:**
1. iPad White Frame
2. iPad Black Frame

How To Use:
======   
*Should be used with 2 divs:*
1. An outside div with the frame color AND type:
   ```css
   <div class="white ipad-frame">
   ```
2. An inner div where you set the div size to match the device screen size
    ```css
    <div class="ipad-screen-size">
    ```

**Included Classes:**   
**`."color"`** classes should be applied to an outer div where you'll also add the frame
    Colors available: "white", "black"
**`."device-frame"`** classes should be applied to an outer div where you'll also add the color  
    Frames available: "ipad-frame"
**`."device"-screen-size`** classes should be applied to the actual inner component you're working on   
    Device Screen Sizes available: "ipad-screen-size"   

Implementing in REACT:
======   
If you use Facebook's [Create React App](https://github.com/facebook/create-react-app g"Create React App") you can implement your device frame in a few ways:
1. In your `public/index.html` as so:
   ```html
   <div class="white ipad-frame">
    <div class="ipad-screen-size" id="root"></div>
   </div>
   ```
2. Or in your React Components as so:  
    <code>_Example below includes "React Flux Dash" Flux.Views, therefore some terminology changes from a regular React.Component_</code>
    ```javascript
    import React from "react";
    import Flux from "@4geeksacademy/react-flux-dash";
    import myStore from "./MyStore";
    import "./device-frames.css";

    class App extends Flux.View {
    constructor() {
        super();
        this.state = {

        };

        this.bindStore(MyStore);
    }

    handleStoreChanges() {
     }

    render() {
     return (
         <div className="white ipad-frame"
            <div className="App ipad-screen-size">
                <h1>My App</h1>
            </div>
         </div>
      )
     }
    }
    ```


