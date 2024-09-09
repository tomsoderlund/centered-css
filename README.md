# Centered CSS framework

**A centered, auto-scaling CSS box**

NPM: https://www.npmjs.com/package/centered-css

Demo: https://tomsoderlund.github.io/centered-css/

![Screenshot of Centered CSS](docs/demo.gif)


## Installation and usage

    yarn add centered-css

Add class `centered` on your element that you want centered ([demo](https://tomsoderlund.github.io/centered-css/index.html)).

Class `centered portrait` will make it in portrait aspect ratio, more suitable for phones ([demo](https://tomsoderlund.github.io/centered-css/portrait.html)).

Then, use `em` or `%` size units (not `px`) and they will auto-scale with the window size.

## Import in JavaScript

    import '../node_modules/centered-css/dist/centered.min.css'

Optional: Add this for iOS Safari resize fix:

    <script type="application/javascript">
      // iOS Safari resize fix
      function handleResize () { window.document.documentElement.style.setProperty('--vmin', `${Math.min(window.innerWidth, window.innerHeight) * 0.01}px`); };
      window.onload = handleResize;
      window.onresize = handleResize;
    </script>

or for React:

    useLayoutEffect(() => {
      // iOS Safari resize fix in React
      function handleResize () { window.document.documentElement.style.setProperty('--vmin', `${Math.min(window.innerWidth, window.innerHeight) * 0.01}px`); };
      window.addEventListener('resize', handleResize);
      handleResize();
      return () => window.removeEventListener('resize', handleResize);
    }, []);

## Update NPM

    yarn publish

(Will run `yarn prepare` automatically, which builds the `/dist` folder)
