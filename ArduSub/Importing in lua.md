
importer.lua
```lua
gcs:send_text(0, 'trying to import')
local mavlink_msgs = require("test/importee")
```

modules/test/importee.lua:
```lua
gcs:send_text(0, "import worked")
```