![](https://github.com/Starexify/Starexify/blob/main/resources/FNF/CCAPI/ccapi_logo.png?raw=true)

## API Usage Examples

### Registering a KeyBind:
```haxe
override public function onCreate(event:ScriptEvent) {
  ControlsAPI.instance.registerKeybind("Dodge", [32, 0], "NOTES", ["justPressed", "justReleased"]);
}
```

### Registering a Header:
```haxe
override public function onCreate(event:ScriptEvent) {
  ControlsAPI.instance.registerHeader("Header", 1);
}
```

### Binding a Callback for the custom keybind
```haxe
var addedKeyBinds:Bool = false;

override public function onUpdate(event:UpdateScriptEvent) {
  if (addedKeyBinds) return;
  ControlsManager.registerCallback("Dodge", InputsUtil.JUST_PRESSED, key -> {
    trace("Just pressed key: " + key);
  });
  addedKeyBinds = true;
}
```


<sub>This will be replaced in the future with a centralized documentation page for all my mods.</sub>