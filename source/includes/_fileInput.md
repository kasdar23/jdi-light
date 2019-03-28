# File input

<aside class="notice">
This section is about working with file input.
</aside>

**File input** –  control for uploading files on web application.

Here is the list of available methods:

|Method | Description | Return Type
--- | --- | ---
**SelectFile()** |Sends file to control without posting form | void

Action > Examples:

```csharp 
[Test]
public void FileInputTest() 
{
     TestSite.Html5Page.FileInput.SelectFile(CreateFile(filename));
     var uploadedFile = TestSite.Html5Page.FileInput.GetAttribute("value");
}


```
