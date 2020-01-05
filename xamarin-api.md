## Project Structure
* Xamarin Forms Project (Shell)
    *  Android 9.0 (Pie)
    * .NET Standard 2.0 library 
* .NET Core 3.0 API

(need screenshots from VS new project wizard)

## Setting Up to Debug
We're going to start off using plain HTTP to simplify configuration and end to end testing. This is somewhat easier than using HTTPS and trusting the self signed SSL certificate, but it should not be used for production deployment (neither should trusting self signed certificates).

**Information: Android enforces strict transport security rules regarding HTTP transport - by default, applications must use HTTPS, and the HTTPS connection must use a valid server certificate. This is fine in production, but makes it difficult to debug locally. To get around this, we have three options: 
* We can allow HTTP (plain text transport) 
* We can allow untrusted certificates
* We can make our API publically accessible and use a valid SSL certificate (e.g. https://letsencrypt.org)

All three options have some security issues, so we wil go with the easiest and arguably most secure - enabling plain text transport in debug mode.

In the API project:
1. Open the API project properties
2. Change the API project to host using 'Project' instead of IIS Express.
3. Change the URL to http://localhost:5000

In the Android project:
1. Expand the 'Properties' folder.
2. Open the AssemblyInfo.cs file
3. Add the following code:

//code to allow plain text connections while debugging:

#if DEBUG

[assembly: Application(UsesCleartextTraffic = true)]

#endif

Now we will change the solution configuration to start up both the Android and API projects when debugging. 

1. Right click the solution and select 'Properties'
2. Common Properties/Startup Project and change the API and Android Projects to 'Start' 
3. Ensure the Android project is set to 'Deploy' as well.

(Add screenshot from project properties)

