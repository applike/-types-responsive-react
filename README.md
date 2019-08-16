# typed-responsive-react

This is typed version of [responsive-react](https://www.npmjs.com/package/responsive-react) npm package. 

### [Demo](https://codesandbox.io/s/react-typescript-j14x2)

# Install

`npm i -D typed-responsive-react`

# How to use

Following can be imported from this package 

    import {
        Responsive,
        getWindowDimension,
        getDeviceTypeInfo,
        isMobileDevice,
        isTabletDevice,
        isLaptopDevice,
        isBiggerThanLaptop,
        IDeviceInfo,
        IWindowDimension
    } from 'typed-responsive-react';

**`Responsive`** 

    <>
        <Responsive displayIn={["laptop"]}>
            Content to be displayed in LAPTOP
        </Responsive>
        <Responsive displayIn={["mobile", "tablet"]}>
            Content to be displayed in LAPTOP
        </Responsive>
    </>


**`getDeviceTypeInfo()`** function returns of type `IDeviceInfo` contains following information:

- width = Width of viewport
- height = Height of viewport
- deviceTypeVariant = [MobileSmall, MobileMedium, MobileLarge, Tablet, iPadPro, LaptopSmall, LaptopLarge, LargerThanLaptop, LargeScreenMax]
- deviceType = [Laptop, Tablet, Mobile, LargerThanLaptop]
- orientation = [Landscape, Portrait]
- isFallback = [true, false] default false. true if it detects some awkward dimension (true is very rare)


**`isMobileDevice`**, **`isTabletDevice`**, **`isLaptopDevice`** and **`isBiggerThanLaptop`**

These function returns `boolean` value for each deviceType.