# Centered CSS framework

**A centered, auto-scaling CSS box**

NPM: https://www.npmjs.com/package/centered-css

Demo: https://tomsoderlund.github.io/centered-css/

![Screenshot of Centered CSS](docs/demo.gif)


## Install

    yarn add centered-css


## Import in JavaScript

    import '../node_modules/centered-css/dist/centered.min.css'

Add this for iOS Safari resize fix:

    <script type="application/javascript">
      // iOS Safari resize fix
      function handleResize () { window.document.documentElement.style.setProperty('--vmin', `${Math.min(window.innerWidth, window.innerHeight) * 0.01}px`); };
      window.onresize = handleResize;
      handleResize();
    </script>

## Update NPM

    yarn publish

(Will run `yarn prepare` automatically, which builds the `/dist` folder)
