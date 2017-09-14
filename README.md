# Using Azure Tables with MVVM

> **This is a work in progress**
>
> Please check again in a few days, and [subscribe to @LBugnion on Twitter](http://twitter.com/lbugnion) for updates.

Azure Tables are an easy way to get a database in the cloud, without worrying about infrastructure. They can be a good solution if you are looking for a lightweight cloud database, without moving to a more complex and more powerful CosmosDB for example.

This sample shows how you can communicate with Azure Tables from a Model-View-ViewModel based applications, for example a Xamarin or Windows application using MVVM Light, and how to leverage data binding on the client in an easy manner.

# The scenario

When you use Azure Table, you create a table containing rows. Each row can get mapped to a .NET object on the client (for example a UWP or Xamarin application [using the Azure SDK](https://azure.microsoft.com/en-us/downloads/).

> For more information about the Azure SDK, you can [navigate to our docs.Microsoft.com](http://gslb.ch/a2a).

When you map an Azure Table row to a .NET object, this object needs to derive from [the TableEntity class](http://gslb.ch/a3a). Thankfully this base class is lightweight enough that we can use it in our client applications easily. However the challenge is that we cannot use databinding on such an instance, because the properties do not raise the PropertyChanged event which is needed for databinding in Windows, Xamarin.iOS, Xamarin.Android or Xamarin.Forms. 

The goal of this article is to show how you can solve this issue and how your entities can be enhanced to use databinding in an MVVM application.

## The sample

The first sample in this repository shows a client-side application connecting to Azure Table directly using the Azure SDK. The entities are then leveraged directly as model objects in an MVVM application for Windows and Xamarin.

The second sample shows a server side application offering an HTTP endpoint delivering some JSON. The client-side application connects to the end point, and leverages the same entities as the server. Then these objects are used in an MVVM application for Windows and Xamarin.

# About MVVM Light

> [More information about MVVM Light](http://www.mvvmlight.net)

The main purpose of the MVVM Light Toolkit is to accelerate the creation and development of MVVM applications in Windows Universal, WPF, Silverlight, Xamarin.iOS, Xamarin.Android and Xamarin.Forms. 

The MVVM Light Toolkit helps you to separate your View from your Model which creates applications that are cleaner and easier to maintain and extend. It also creates testable applications and allows you to have a much thinner user interface layer (which is more difficult to test automatically).

Even though this sample uses MVVM Light for the demonstration, the principles detailed here can also be applied with any other MVVM framework.

