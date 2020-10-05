![HEXATONIC: An overengineered hex color code conversion library for Love2D](https://i.imgur.com/MslYNVh.png)

An overengineered hex color code conversion library for Love2D

Built off of [Hex Maniac](https://github.com/LavenderTheGreat/HexManiac.git) by LavenderTheGreat

# Features
- Convert from RGB(A) with an optional opacity value
- Converts correctly for both 0-1 and 0-255 seemlessly
- Argument validation for both hex color codes and opacity
- Takes console logging functions on initalization

# Require
HEXATONIC can be `require`d in multiple ways
```lua
-- Multistep
local HEXATONIC = require 'hexatonic')
local hex = HEXATONIC(Logger)

-- Single step
-- #1
local hex = require 'hexatonic'(Logger)
-- #2
local hex = require('hexatonic')(Logger)
```
The `logger` argument is a table expected to contain `log`, `alert`, and `error` functions for HEXATONIC to call when or if required.

# Usage
Usage is simple, simply call `hex` with a hex color code and optional opacity value (0-1), it will return a table matching Love's requirements for a color.
```lua
love.graphics.setColor(hex('20214F'))
love.graphics.setColor(hex('20214FA3'))
love.graphics.setColor(hex('20214F', 0.25))
```