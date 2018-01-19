## \<skeleton-image-uploader\>

`skeleton-image-uploader` is a [Polymer 2](http://polymer-project.org) and [Firebase](https://firebase.google.com/) element for uploading images with a progress indication bar and drag and drop capability.

## Installation

Install skeleton-image-uploader with Bower

```shell
$ bower install --save FabricElements/skeleton-image-uploader
```

## Usage

Import it into the `<head>` of your page

```html
<link rel="import" href="bower_components/skeleton-image-uploader/skeleton-auth.html">
```

### Example: basic usage

Configure your Firebase app

```html
<firebase-app
  apiKey="AIzaSyCJRNdR0eodnswyi8MHCtF1YOjY235mhM8"
  authDomain="fabricelements.firebaseapp.com"
  databaseURL="https://fabricelements.firebaseio.com"
  storageBucket="fabricelements.appspot.com"
  messagingSenderId="908593247251"
></firebase-app>

> See [Polymerfire](https://www.webcomponents.org/element/firebase/polymerfire/) docs for more information.

Then add the `skeleton-image-uploader` element.

```html
<skeleton-image-uploader circle
                         content-type="image/jpeg"
                         metadata='{"customMetadata":{"type":"avatar"}}'
                         path="demo.jpg"
                         placeholder="./placeholder.jpg"
                         vision="AIzaSyDqtR51PSS-Pr9FSUHAKQGkNiy_cqPA9W4"
                         ></skeleton-image-uploader>
```

### Attributes

* `circle` (boolean) - The shape of the container.
* `content-type` (string) - The media type of the resource.
* `metadata` (object) - The metadata to save along with the image.
* `path` (string) - Firebase storage reference.
* `placeholder` (string) - The placeholder image.
* `vision` (String) - The vision API key.

### Other attributes

* `imageAnalysing` (boolean) - Checks if the image is being analyzed.
* `uploading` (boolean) - True when the image starts uploading.
* `uploadProgress` (number) - The upload progress of the image.
* `uploaded` (boolean) - True when the image is uploaded.
* `progressValue` (number) - The value for the stroke-dashoffset attribute.
* `horizontal` (boolean) - The shape (rectangular) of the container.
* `showCircleProgress` (boolean) - True when circle is set and image is uploaded.
* `showHorizontalProgress` (boolean) - True when horizontal is set and image is uploaded.
* `strokeWidth` (number) - The stroke-width attribute.
* `src` (string) - The image src.
* `imageVisionError` (boolean) - True when vision throws an error.
* `imageSafe` (boolean) - True when image is safe.
* `imageUnsafeLogos` (boolean) - True when an image has brands content.
* `imageUnsafeAdult` (boolean) - True when an image has adult content.
* `imageUnsafeSpoof` (boolean) - True when an image has spoof content.
* `imageUnsafeMedical` (boolean) - True when an image has medical content.
* `imageUnsafeViolence` (boolean) - True when an image has violent content.
* `finalMetadata` (object) - The final metadata.
* `disabled` (boolean) - Disable option.
* `captureMethod` (string) - The image capture method.
* `exist` (boolean) - True when path exists.
* `maxWidth` (number) - The max width of the image.
* `maxHeight` (number) - The max height of the image.
* `minWidth` (number) - The min width of the image.
* `minHeight` (number) - The min height of the image.
* `error` (object) - Error.

### Events

* `error-changed` - Fired when the error property has changed.

## Contributing

Please check [CONTRIBUTING](./CONTRIBUTING.md).

## License

Released under the [BSD 3-Clause License](./LICENSE.md).
