# Sifon.Packages

#### Shared packages for Sifon provided from GitHub package repository


## How to use?

In order to reference **Sifon.Packages**, one may need to have a nuget.config file at the solution root folder. Please make sure you've added the following line into `<packageSources>` node:

`<add key="Sifon.Packages" value="https://nuget.pkg.github.com/MartinMiles/index.json" />`

You need also to specify a public security token for this repo which is: `893e082c10d3cceb937673b97c6a7adb6c720ca6`. 

You may end up having something similar to below:

```
<?xml version="1.0" encoding="utf-8"?>
<configuration>
    <packageSources>
        <clear />
        <add key="nuget.org" value="https://www.nuget.org/api/v2/" />
        <add key="Sifon.Packages" value="https://nuget.pkg.github.com/MartinMiles/index.json" />
    </packageSources>
    <packageSourceCredentials>
        <Sifon.Packages>
            <add key="Username" value="miles@martin.by" />
            <add key="ClearTextPassword" value="893e082c10d3cceb937673b97c6a7adb6c720ca6" />
        </Sifon.Packages>
    </packageSourceCredentials>
</configuration>
```

**Note:** if you do not use any custom NuGet repositories - you simply save the above code as-it.



## Visual Studio

After `nuget.config` is put into the solution root, you **must** restart Visual Studio for the changes to take effect.

If all the steps done correctly, you will be able to see and reference Sifon libraries:

![Visual Studio look](https://raw.githubusercontent.com/wiki/MartinMiles/Sifon.Packages/img/VisualStudio.png "Visual Studio look")

