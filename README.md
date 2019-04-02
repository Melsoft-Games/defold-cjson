![](docs/logo.png)

# Defold-CJSON

Defold-CJSON [Native Extension](https://www.defold.com/manuals/extensions/) for the [Defold Game Engine](https://www.defold.com) 

This extension allow you encode lua table to JSON and decode JSON to lua table in native part


## Platforms

* **iOS**
* **Android**
* **MacOS**
* **Windows**

## Setup

You can use the Defold-CJSON extension in your own project by adding this project as a [Defold library dependency](https://www.defold.com/manuals/libraries/). Open your game.project file and in the dependencies field under project add:

> https://github.com/Melsoft-Games/defold-cjson/archive/master.zip

Or point to the ZIP file of a [specific release](https://github.com/Melsoft-Games/defold-cjson/releases).

## API

#### `cjson.encode(lua_table)`
return encoded lua table to json string

#### `cjson.decode(valid_json)`
return parsed lua_table 

**Note**: *json must be valid, or cjson will throw error. You can wrap it with pcall, or change extension and call cjson safe_decode from lua-cjson lib*


## Benchmark
**rxlua** - pure lua JSON encode/decode [implementation](https://github.com/rxi/json.lua)

time in ms

| Json: | 4KB | 971KB | 1.8MB |
| -- | -- | -- | -- |
| defold decode  |  0  		|  0.032  	|  0.075  |
|  -- 			 |  --  	| --   		| --		|
|  rxlua encode  |  0  		|  0.0734  	|  0.148  |
|  rxlua decode  |  0.0003  |  0.0308  	|  0.051  |
|  -- 			 |  --  	| --   		| --		|
|  cjson encode  |  0  		|  0.0057  	|  0.0122  |
|  cjson decode  |  0  		|  0.0066  	|  0.0117  |



## License, Authors
*MIT license*
This NE wrapped by [Denis Smirnov](https://github.com/trouble1337)

Original module: [lua-cjson](https://github.com/mpx/lua-cjson)
[License](https://github.com/mpx/lua-cjson/blob/master/LICENSE)

## Issues and suggestions

If you have any issues, questions or suggestions please [create an issue](https://github.com/Melsoft-Games/defold-cjson/issues) or contact me: insality@gmail.com
