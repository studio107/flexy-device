[![Build Status](https://travis-ci.org/studio107/flexy-device.svg?branch=master)](https://travis-ci.org/studio107/flexy-device)

# default device list

```scss
laptop
laptop-retina
iphone-4-4s
iphone-4-4s-portrait
iphone-4-4s-landscape
iphone-5-5s
iphone-5-5s-portrait
iphone-5-5s-landscape
iphone-6
iphone-6-portrait
iphone-6-landscape
iphone-6-plus
iphone-6-plus-portrait
iphone-6-plus-landscape
ipad-mini
ipad-mini-portait
ipad-mini-landscape
ipad-1-2
ipad-1-2-portrait
ipad-1-2-landscape
ipad-3-4
ipad-3-4-portrait
ipad-3-4-landscape
```

# flexy-device-has

```scss
@include assert-false(flexy-device-has(hello));
@include assert-true(flexy-device-has(iphone-4-4s));
```

# flexy-device-get

```scss
@include assert-equal(flexy-device-get(laptop), (min-device-width: 1200px, max-device-width: 1600px, -webkit-min-device-pixel-ratio: 1));
```

# flexy-device-media

```scss
@include assert-equal(flexy-device-media(iphone-4-4s), '(-webkit-min-device-pixel-ratio: 2) and (max-device-width: 480px) and (min-device-width: 320px)');
```

# custom devices

```scss
// Define your device
$flexy-devices: (
        hello: (min-device-width: 1200px)
);
// Include flexy-device
@import "~flexy-device/src/device";

@include assert-true(flexy-device-has(hello)); // true
```
