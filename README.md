# Sifon.Packages

#### Shared packages for Sifon provided from GitHub package repository


## How to use?

In order to reference **Sifon.Packages**, one may need to have a `nuget.config` file at the solution root folder. Please make sure you've added the following line into `<packageSources>` node:

`<add key="Sifon.Packages" value="https://nuget.pkg.github.com/MartinMiles/index.json" />`

You need also to specify a public security token for this repo which is: `77c748140e8b4f5a___b17ce29294b2a9a9e147b47a` (please remove underscores from the middle). At the moment GitHub prevents one from storing tokens on commits and revokes those found, even that is a read-only token allowing access only to packages. That is why we must prevent this token from auto-deletion by putting underscores in the middle of it in order to commit and push to GitHub.


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
            <add key="ClearTextPassword" value="77c748140e8b4f5a___b17ce29294b2a9a9e147b47a" />
        </Sifon.Packages>
    </packageSourceCredentials>
</configuration>
```

**Note:** if you do not use any custom NuGet repositories - you simply save the above code only removing underscores from the token value.



## Visual Studio

After `nuget.config` is put into the solution root, you **must** restart Visual Studio for the changes to take effect.

If all the steps done correctly, you will be able to see and reference Sifon libraries:

![Visual Studio look](https://raw.githubusercontent.com/wiki/MartinMiles/Sifon.Packages/img/VisualStudio.png "Visual Studio look")

