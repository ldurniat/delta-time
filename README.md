# delta-time

*delta time* is simple module for time based animations for [Corona SDK](https://coronalabs.com/corona-sdk/). It is supposed to work with [*enterFrame*](https://docs.coronalabs.com/api/event/enterFrame/index.html) event. 

### deltatime.getTime()

This function returns the actual number of milliseconds that have gone by since the previous frame.

### deltatime.restart()

Start counting delta time from 0. It is useful if you don't use `deltatime.getTime()` for a while.

#### Example:

```
local dt = require( 'deltatime' )

local player = display.newRect( 100, 100, 50, 50 )

local function loop( event )

	-- Move player object 50 pixels per second
	local dx = 50 * dt.getTime()

	player:translate( dx, 0 )

end

Runtime:addEventListener( 'enterFrame', loop )
```

### Run

To run code you need install [Corona SDK](https://portal.coronalabs.com) 

### License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/ldurniat/delta-time/blob/master/LICENSE) file for details.