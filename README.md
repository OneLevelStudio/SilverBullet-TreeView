# TreeView

A fork of `joekrill/silverbullet-treeview` at [`8769979`](https://github.com/joekrill/silverbullet-treeview/tree/8769979891176d498c949a8eec3d7fb907196207).

## Usage

`space-lua`
```space-lua
config.set {
  -- ================================================== --
  -- ================================================== --
  -- ================================================== --
  plugs = {
    "github:OneLevelStudio/SilverBullet-TreeView/treeview.plug.js",
  },
  -- ================================================== --
  -- ================================================== --
  -- ================================================== --
  -- The treeview plug configuration
  treeview = {
    position = "lhs", -- "lhs" / "rhs" / "bhs" / "modal"
    size=0.35,
    dragAndDrop = { enabled = false, confirmOnRename = true },
    exclusions = {
      { type = "regex", rule="^(?:CONFIG|Library).*$", negate= false },
      { type = "tags", tags = {"meta"}, negate = false }
    }
  },
  -- ================================================== --
  -- ================================================== --
  -- ================================================== --
  actionButtons = {
    {
      icon = "home", description = "Home",
      run = function() editor.invokeCommand("Navigate: Home") end
    },
    {
      icon = "folder", description = "Folder",
      run = function() editor.invokeCommand("Tree View: Toggle") end
    },
  },
  -- ================================================== --
  -- ================================================== --
  -- ================================================== --
}
```
