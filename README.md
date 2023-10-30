# Fuyo Cloverfield Chat CSS for OBS

## Step 1: Create a new browser source

In a scene, create a new browser source:

![](readme-imgs/obs1.png)

## Step 2: Youtube chat URL

Open your stream in your browser, click on the chat popout button and copy the
URL.

![](readme-imgs/yt1.png)
![](readme-imgs/yt2.png)

### Holodex Chat Redirect

You can also use [Holodex Chat Redirect](https://github.com/clovercharms/holodex-chat-redirect) to automatically redirect to the earliest
scheduled stream. This way you won't need to update the popout chat URL for
every stream!

For more instructions, check the link above or check out the example
for Fuyo Cloverfield's channel below:

https://clovercharms.github.io/holodex-chat-redirect/?apiKey=14830ce2-3b83-42f7-aabe-61ba314fd619&channelId=UC8zgKaS8LiyL28mdhRC2nBg

## Step 3: Enter all the stuff into OBS Studio

In OBS, when creating the browser source, paste the youtube chat URL for the
`URL`.

Set `Width` to something like 400. `Height` your choice.

Lastly, copy the CSS from this file [here](yuko-chat.css) into the `Custom CSS`
field, delete the default text first.

![](readme-imgs/obs2.png)

DONE! :D

# Customization

You can customize the colors yourself in the first paragraph! Even change the
emote in the background, or provide your own image url.

```css
:root {
    /* Theme Colors */
    --chat-color-accent: #f0fee4;
    --chat-color-primary: #cbf2aa;
    --chat-color-secondary: #71c185;
    --chat-color-tertiary: #406345;

    /* General */
    --chat-font: "Subscribe Regular";
    --chat-font-size: 2.2rem;
    --chat-border-width: 2.5px;
    --chat-border-radius: 1rem;
    --chat-dot-spacing: 2rem;
    --chat-animation-duration: 0.5s;
    ...;
}
```

# Caveats

## Updating URL

Unfortunately, when not using [Holodex Chat Redirect](#holodex-chat-redirect),
you need to set the URL for every stream.

Pro tip, just replace the youtube stream ID (the part after the `&v=`) thats
all you need.

## Member Streams

For _member streams_ you need to log in to your OBS browser first. Create a new
browser source for `youtube.com` and click `interact` to log in with your
youtube account. You might need to copy + paste your credentials.

once done you can delete the browser source, your cookies are shared between
different sources.

![](readme-imgs/obs3.png)
