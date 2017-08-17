# ionic2-picture-directive

Ionic2PictureDirective help you use capture picture to device with just a directive and a very simple configuration.

## Install

```bash
ionic cordova plugin add cordova-plugin-camera
npm install --save @ionic-native/camera
```

## Import directive

Import the directive into your app module.

```typescript
import {Ionic2PictureDirective} from "ionic2-picture-directive";

@NgModule({
    declarations: [
        MyApp,
        Ionic2PictureDirective,
        HomePage
    ],
    imports: [
        BrowserModule,
        IonicModule.forRoot(MyApp),
        HttpModule
    ],
    bootstrap: [IonicApp],
    entryComponents: [
        MyApp,
        HomePage
    ],
    providers: [
        StatusBar,
        SplashScreen,
        {provide: ErrorHandler, useClass: IonicErrorHandler}        
    ]
})
export class AppModule {
}
```

## Usage

Add directive in your project

Add in your tag with 'picture' and receive a return in 'return-picture'.


## Example

```html
<!-- HTML -->
<img src="{{url}}" picture (retorna-picture)="setPicture($event)">
<!-- JS -->
setPicture(picture){
    this.url = picture;
}
```

## Contribute

Any pull-request and issue is more than welcome.

## License

[The MIT License (MIT) Copyright (c) 2013](http://opensource.org/licenses/MIT) 
 