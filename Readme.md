Add [turbolink](https://github.com/rails/turbolinks) support to ASP.NET 5 applications 

This provides middlewear to add support for turbolinks. Simply add `app.UseTurboLinks();` and a build of turbolinks (one can be found in the wwwroot/js dir of the example project)


## Why use turbolinks?

If you have an application that may not fit into an SPA, or just have a lot of code that is tied to .NET this provides SPA like speed by ajaxing the html and replacing it. This allows the browser to keep the cache of existing scripts. Turbolinks was made in the rails community, and a lot of existing documentation already exists.


**Warning** This stops page loads thus `$(document).ready(function(){})` does not fire on new pages.

## What about asp.net 4x?

I am going to back port this to owin, and eventually more classic version of ASP.NET In the mean time, you can find an MVC action filter [here](https://github.com/kazimanzurrashid/aspnetmvcturbolinks)