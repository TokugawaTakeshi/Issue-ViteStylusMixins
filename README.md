# The reproduction of the Vite issue #10605

[🌎 "Maximum call stack size exceeded" error on calling the Stylus mixin from the library while without Vite working fine](https://github.com/vitejs/vite/issues/10605)


## Experiment flow

### Step 1: Installing of the dependencies

```bash
npm i
```


### Step 2: Checking the plain Stylus first

1. Check the contents of **Test.styl** file. 
2. Run `npm run "Stylus test"`. If no error in the console and output CSS file appeared, Stylus works fine.


### Step 3: Checking the Vite

1. Check the **style** section of **App.vue**. The content in even with **Test.styl** but the mixin usage has been commended out. 
2. Run the application with `npm run dev`
3. Open the host assigned by the Vite (usually `http://127.0.0.1:5173/`)
4. Uncomment the lines 25-28. You should see the error `"Maximum call stack size exceeded"` in the browser.
