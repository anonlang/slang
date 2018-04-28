# slang
Standard Language: Pluggable to match any modern or future language.

## Example
    ; MyApp.app
    ; A sample app that shows "Hello, World!", compilable to any platform
    text-view 'Hello World'

## Parser
    app statement*
    statment type-block? line-comment?
    type-block type type-input*
    type [a-zA-Z_-][a-zA-Z0-9_-]+
    type-input number|text|type
    number [0-9]+
    text '.*'
    line-comment ;.*
    
## Standard Library
    api app
        start
        stop
        api config
            author
                email
                name
                website
            description
            title
            version
    api database
    api file
    api lang
        api boolean
        api number
        api text
    api math
    api text
    api type
    api view
        height
        id
        width
        on-click
        on-double-click
        on-gesture
        on-hover
        on-long-click
        on-swipe
        api button
        api canvas
        api image
            api back
            api forward
            api pause
            api save
            api start
            api stop
        api input
            default-text
            hint-text
            label-text
            api email
            api number
            api text
                number-of-columns
                number-of-rows
        api layout
            col
            flow
            grid
            row
        api menu-bar
        api option
            is-allow-multiple-selections
            is-show-all
            number-of-options-to-show
        api table
        api text
        api video
            is-show-pause
            is-show-play
            is-show-save
            is-show-share
            is-show-stop
