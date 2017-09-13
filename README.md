# Using Azure Tables with MVVM

Azure Tables are an easy way to get a database in the cloud, without worrying about infrastructure. They can be a good solution if you are looking for a lightweight cloud database, without moving to a more complex and more powerful CosmosDB for example.

This sample shows how you can communicate with Azure Tables from a Model-View-ViewModel based applications, for example a Xamarin or Windows application using MVVM Light, and how to leverage data binding on the client in an easy manner.

## About MVVM Light

> [More information about MVVM Light](http://www.mvvmlight.net)

The main purpose of the MVVM Light Toolkit is to accelerate the creation and development of MVVM applications in Windows Universal, WPF, Silverlight, Xamarin.iOS, Xamarin.Android and Xamarin.Forms. 

The MVVM Light Toolkit helps you to separate your View from your Model which creates applications that are cleaner and easier to maintain and extend. It also creates testable applications and allows you to have a much thinner user interface layer (which is more difficult to test automatically).

Even though this sample uses MVVM Light for the demonstration, the principles detailed here can also be applied with any other MVVM framework.

> **This is a work in progress**
>
> Please check again in a few days, and [subscribe to @LBugnion on Twitter](http://twitter.com/lbugnion) for updates.