devtyrcom
=========

http://devtyr.com

See this as an example for [Gullap](https://github.com/devtyr/gullap "Gullap static website generator for .NET/Mono").

## Important

The first call should be the following to create the missing output folder:

> GullapConsole -i %ClonePath%

Then call

> GullapConsole -g %ClonePath%

to generate the output.

To view the output correctly, you need to point your webserver to this page. If you don't do that, all style sheets and JavaScript files won't be found as they are all referenced from the root folder of the website. This has nothing to do with `Gullap`, it's just how the templates are written.
