# delta-time

*delta time* is simple module for time based animations for [Corona SDK](https://coronalabs.com/corona-sdk/). It is supposed to work with [*enterFrame*](https://docs.coronalabs.com/api/event/enterFrame/index.html) listener. 

Whatever you restart animations you need call ``` dt.restart() ``` function.

#### Example:

```
local dt = require( 'deltatime' )

local player = display.newRect( 100, 100, 50, 50 )

local function loop( event )
	local dx = 5 * dt.getTime()
	player:translate( dx, 0 )
end

Runtime:addEventListener( 'enterFrame', loop )
```
