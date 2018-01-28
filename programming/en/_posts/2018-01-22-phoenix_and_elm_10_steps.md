---
layout: post-comments
title:  10 sequential steps to use Elm with a Phoenix app
date:   2018-01-28 00:01:00
excerpt: "Note to my future self: configuring Elm with Phoenix."
description: "A straightforward sequence of steps to make you ready to Elm on
Phoenix."
image: /images/2018-01-22-phoenix_and_elm_10_steps/screen_with_code.png
categories:
  - en
  - elm
  - phoenix
  - programming
---

![This is a Phoenix, with and Elm inside of it!]({{page.image}}){:class="center-image" }

At the time of this writing
the following steps are straight to the point
to create a new _Phoenix_ application
and configuring _Elm_ on top of it.

I'll assume that you have
_Phoenix_, _Elm_ and _NodeJS_ ready to rock.
Ah, and you would probably like to
use your application name where you read *mr_wednesday*:

 1. __$__ mix phx.new mr_wednesday
 2. __$__ cd mr_wednesday/assets
 3. __$__ npm install `--save-dev elm-brunch`
 4. __$__ mkdir elm
 5. __$__ cd elm
 6. __$__ elm package install elm-lang/html
 7. __edit__ `mr_wednesday/assets/brunch-config.js`
   * add the _elm_ dir to the _watched paths_ section:

    ```js
    paths: {
      watched: ["static", "css", "js", "vendor", "elm"],
      // ...
    }
    ```
    * add the a new section called `elmBrunch`
    to the config under `plugins`:

    ```js
    elmBrunch: {
      elmFolder: "elm",
      mainModules: ["Main.elm"],
      outputFolder: "../js"
    }
    ```

 8. __create__ `mr_wednesday/assets/elm/Main.elm`

    ```elm
    module Main exposing (..)

    import Html exposing (text, Html)


    main : Html a
    main =
        text "Hello World"
    ```

 9. __edit__ `mr_wednesday/assets/js/app.js` and add:

    ```js
    import Elm from "./main"
    const elmDiv = document.querySelector("div#elm-app")
    Elm.Main.embed(elmDiv)
    ```
 10. __edit__ `mr_wednesday/lib/mr_wednesday_web/templates/page/index.html.eex`:

      ```html
      <div id="elm-app"></div>
      ```

### Run the app.

Why not, right? Some more steps for you:

 1. __$__ cd mr_wednesday
 2. __$__ mix ecto.create
 3. __$__ mix phx.server
 4. __visit__ http://localhost:4000

And you should see a unsurprisingly boring
hello world directly from _Elm_.
