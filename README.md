# Building Airbnb(Front-end)

Hi! Did Airbnb Challenge cloning Airbnb(frontend).The challenge was hosted by Sonny Sangha.I learnt couple of tech stacks through the completion of the challenge.


# Tech Stack used for this challenge

 **Next.js**
 **Tailwind CSS**
 **API**
 
 

## Installation

**Install tailwind CSS with Next.js.**

```bash
npx create-next-app -e with-tailwindcss my-project
cd my-project
```
This will automatically configure your Tailwind setup based on the official Next.js example.Now when you run `npm run dev`, Tailwind CSS will be ready to use in your Next.js project.

**Launching VS Code from command line. Here is the trick**
-   Launch VS Code.
-   Open the  **Command Palette**  (Cmd+Shift+P) and type 'shell command' to find the  **Shell Command: Install 'code' command in PATH**  command.

**How to import image  and optimize the image in Next.js**

Image Optimization can be enabled via the `<Image />` component exported by `next/image`.

*Usage*
For an example, consider a project with the following files:

-   `pages/index.js`
-   `public/me.png`

We can serve an optimized image like so:

```jsx
import Image from 'next/image'
import profilePic from '../public/me.png'

function Home() {
  return (
    <>
      <h1>My Homepage</h1>
      <Image src={profilePic} alt="Picture of the author" />
      <p>Welcome to my homepage!</p>
    </>
  )
}

export default Home

```

*Required*
The  `<Image />`  component requires the following properties.

### [src](https://nextjs.org/docs/api-reference/next/image#src)

Required and must be one of the following:

1.  A statically imported image file, as in the example code above, or
2.  A path string. This can be either an absolute external URL, or an internal path depending on the  [loader](https://nextjs.org/docs/api-reference/next/image#loader).

When using an external URL, you must add it to  [domains](https://nextjs.org/docs/basic-features/image-optimization#domains)  in  `next.config.js`.

### [width](https://nextjs.org/docs/api-reference/next/image#width)

The width of the image, in pixels. Must be an integer without a unit.

Required, except for statically imported images, or those with  [`layout="fill"`](https://nextjs.org/docs/api-reference/next/image#layout).

### [height](https://nextjs.org/docs/api-reference/next/image#height)

The height of the image, in pixels. Must be an integer without a unit.

Required, except for statically imported images, or those with  [`layout="fill"`](https://nextjs.org/docs/api-reference/next/image#layout).
```
[For information about image optimization](https://nextjs.org/docs/api-reference/next/image)

**Tailwind plugin scrollbar hide feature**

#using npm
npm install tailwind-scrollbar-hide

# Using Yarn
yarn add tailwind-scrollbar-hide

Then add the plugin to your  `tailwind.config.js`  file:

// tailwind.config.js
module.exports = {
  theme: {
    // ...
  },
  plugins: [
    require('tailwind-scrollbar-hide')
    // ...
  ]
}
```
**Date range picker feature**
```
npm install --save react-date-range
```

This plugin expects  `react`  and  `date-fns`  as peerDependencies, It means that you need to install them in your project folder.

```
npm install --save react date-fns
```
## [](https://github.com/hypeserver/react-date-range#usage)Usage
You need to import skeleton and theme styles first.
```
import 'react-date-range/dist/styles.css'; // main style file
import 'react-date-range/dist/theme/default.css'; // theme css file
```
### [](https://github.com/hypeserver/react-date-range#datepicker)`DatePicker`
```
import { Calendar } from 'react-date-range';

class MyComponent extends Component {
  handleSelect(date){
    console.log(date); // native Date object
  }
  render(){
    return (
      <Calendar
        date={new Date()}
        onChange={this.handleSelect}
      />
    )
  }
}
```

***installing loading bar progress feature***
```
$ npm i @badrap/bar-of-progress
```
## Usage
Import the package and create a progress bar instance:
```
import ProgressBar from "@badrap/bar-of-progress";

const progress = new ProgressBar();
```

## Deploy your App

- Use Vercel "https://vercel.com/" or any other free web hosting services

## Credits
- Huge thanks to Sonny Sangha learnt a lot and looking forward to more live tutorials
