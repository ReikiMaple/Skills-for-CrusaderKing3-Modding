# 06 GUI Jomini

## Jomini Expressions

- GUI and localization can use Jomini-style expressions and object methods.
- Clausewitz script scopes often need conversion before GUI/Jomini access, commonly through `MakeScope` or related methods.
- Check generated data type docs or vanilla examples before inventing GUI method chains.

## Scripted GUI

Scripted GUI entries usually live in `common/scripted_gui`.

Typical shape:

```txt
my_scripted_gui = {
    scope = character
    is_shown = { }
    is_valid = { }
    effect = { }
}
```

GUI calls pass root and saved scopes through `GuiScope`.

## Data Context

- `datacontext` provides the object context inherited by child widgets.
- A widget can draw data from its own context and parent contexts.
- Context type mismatch can cause repeated errors because GUI is evaluated very often.

## GUI Safety

- GUI visibility and validity checks can run repeatedly while the interface is open.
- Avoid expensive traversal in GUI-visible conditions.
- Missing scripted GUI or missing GUI objects can turn whole expression lines into surprising truthy behavior or repeated warnings.
- Verify GUI changes in-game or with screenshots/logs when possible.

