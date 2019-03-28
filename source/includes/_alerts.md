# Alerts

<aside class="notice">
This section is about working with alerts.
</aside>

**Alert** –  a window with a message that displays on the screen and pauses the execution of the script until the user performs an action.

Here is the list of available methods:

|Method | Description | Return Type
--- | --- | ---
**Ok()** |Accepts an alert  | void
**Cancel()** |Dismisses an alert  | void
**SendKeys()** |Sends key to the alert textbox  | void
**GetText()** |Returns the text displayed in the alert  | string

Action > Examples:

```csharp 
[Test]
public void CancelAlertExample() 
{
    MyPage.GetAlert().Cancel();
}

[Test]
public void GetAlertText() 
{
    Assert.AreEqual(MyPage.GetAlert().GetText(), "JDI Title");
}

```
