# Theory
## UI Objects Pattern (Extend your PageObjects with UI elements)
TBD

## Entity Driven Testing
TBD

## Smart Locators

```
<input type="text" id="name">
<input type="text" id="last-name">
<button id="submit-button">
```
```csharp

public class UserCard : Form<User>
{
    [FindBy(Css = "#name")]
    TextField Name; 
    
    [FindBy(Css = "#last-name")]
    TextField LastName;
    
    [FindBy(Css = "#submit-button")]
    Button SubmitButton;
}

If Smart locator rule is id:
    SmartSearchLocator = "#{0}";
    
and convertation rule is hyphen to csharp name:
    SmartSearchName(string name) => StringExtensions.SplitHyphen(name);
    
So you can write:

public class UserCard : Form<User>
{
    TextField Name; 
    TextField LastName;
    Button SubmitButton;
}

```

```java

public class UserCard extends Form<User> {
    @Css("#name") TextField name;
    
    @Css("#last-name") TextField lastName; 
    
    @Css("#submit-button") Button submitButton; 
}

If Smart locator rule is id:
    WebSettings.SMART_SEARCH_LOCATORS = asList("#%s");
    
and convertation rule is hyphen to java name:
    WebSettings.SMART_SEARCH_NAME = StringUtils::splitHyphen;

So you can write:

public class UserCard extends Form<User> {
    TextField name;
    TextField lastName;
    Button submitButton; 
}

```


If you have your developers follow some standard way to mark ui elements or you have an agreement to add special attribute you can even avoid to write locators for elements and make your page objects much more compact.

You can manage how to create locator from field name using.

### Settings interface ISmartLocators contains:
  
- **SmartSearch** - method that invoked if you have element has no locator

- **SmartSearchLocator** - locator that can be used to try to find element

- **SmartSearchName** -  method how to create locator name from filed name (this value will be passed as parameter in SmartSearchLocator)



## JDI Locators (simple as css powerful as xpath)
TBD
