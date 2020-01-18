**Certificate Manager** is a package which makes it easy to create certifcates which can be used to in client server authentication and IoT Devices like Azure IoT Hub

// TODO can setup once the repo is public 

|                           | Build                                                                                                                                                       | Certificate Manager                                                                                                                                |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| .NET Core                 | [![Build status](https://ci.appveyor.com/api/projects/status/gyychgc7l5g4g5lb?svg=true)](https://ci.appveyor.com/project/damienbod/aspnet5localization)      | [![NuGet Status](http://img.shields.io/nuget/v/Localization.SqlLocalizer.svg?style=flat-square)](https://www.nuget.org/packages/Localization.SqlLocalizer/) |


========================

[Quickstart](https://github.com/damienbod/AspNetCoreCertificates/tree/master/src/CreateChainedCertsConsoleDemo) | [Documentation](https://github.com/damienbod/AspNetCoreCertificates/blob/master/Documentation.md) | [Changelog](https://github.com/damienbod/AspNetCoreCertificates/blob/master/CHANGELOG.md)

# Basic Usage ASP.NET Core

Add the NuGet package to the your project file

```
<PackageReference Include="CertificateManager" Version="1.0.0" />
```

The NuGet packages uses dependency injection to setup. In a console application initialize the package as follows:
```
var serviceProvider = new ServiceCollection()
    .AddCertificateManager()
    .BuildServiceProvider();

```

Or in an ASP.NET Core application use the Startup ConfigureServices method to initialize the package.

```
public void ConfigureServices(IServiceCollection services)
{
    // ...

    services.AddCertificateManager();
}
```

Now the package is ready to use. See the [Documentation](https://github.com/damienbod/AspNetCoreCertificates/blob/master/Documentation.md)  to create the specific certificates for your use case.

# Examples Creating Certificates:

<ul>
    <li><a href="https://github.com/damienbod/AspNetCoreCertificates/tree/master/src/CreateChainedCertsConsoleDemo">Create **chained** certificate authentication certificates console</a></li>
    <li><a href="https://github.com/damienbod/AspNetCoreCertificates/tree/master/src/CreateSelfSignedCertsConsoleDemo">Create **self signed** certificate authentication certificates console</a></li>
</ul>

# Examples Using Certificates:

<ul>
    <li><a href="https://github.com/damienbod/AspNetCoreCertificates/tree/master/examplesUsingCertificateAuthentication/AspNetCoreChained">ASP.NET Core chained certificate authentication</a></li>
    <li><a href="https://github.com/damienbod/AspNetCoreCertificates/tree/master/examplesUsingCertificateAuthentication/AzureCertAuth">Azure ASP.NET Core self signed certificate authentication</a></li>
    <li><a href="https://docs.microsoft.com/en-us/aspnet/core/security/authentication/certauth">Microsoft Docs: Configure certificate authentication in ASP.NET Core</a></li>
</ul>

