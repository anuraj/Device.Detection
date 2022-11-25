# Device.Detection

This is simple nuget package will help you to identify whether request is coming from a Mobile device or not. This package useful when you migrate your .NET Framework application to .NET Core - where `Request.Browser.IsMobileDevice` equivalent is not available.

Once installed, you will get an extension method - `IsMobileDevice` to Request object.

```
using Device.Detection;

public IActionResult Index()
{
    var isMobile = HttpContext.Request.IsMobileDevice();
    if(isMobile)
    {
        return View("MobileIndex");
    }
    return View();
}
```

## License

MIT