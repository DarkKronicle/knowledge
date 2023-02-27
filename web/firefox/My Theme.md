I use a modified version of [cascade](https://github.com/andreasgrafen/cascade). [My fork](https://github.com/DarkKronicle/cascade) includes support for [Sidebery](https://github.com/mbnuqw/sidebery) out of the box, as well as custom CSS for Sidebery. This creates a gorgeous minimal setup with tons of tab power. Checkout some more information in [[Sidebery]] to see how I use it.


![[firefox_showcase.png]]

## How to Setup

1. Install [Sidebery from GitHub](https://github.com/mbnuqw/sidebery) version >= 5.0.0. You may need to install the beta.
2. Look at [[User Chrome]] to see how to enable the user chrome feature. For the contents of `chrome`, use [my cascade fork](https://github.com/DarkKronicle/cascade). 
3. (Optional) In `userChrome.css` comment out the line that imports `cascade-colours` and install the addon [Adaptive Tab Color](https://addons.mozilla.org/en-US/firefox/addon/adaptive-tab-bar-color/). This changes the color of the strip based on the color of the webpage
4. In Sidebery's settings, scroll down to `Custom CSS` and paste in the contents from [sidebery.css](https://github.com/DarkKronicle/cascade/blob/main/integrations/sidebery/sidebery.css). 
5. Configure Sidebery however you want now.
6. Make sure to reload Firefox to apply any updates to your user chrome

