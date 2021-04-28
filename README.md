# ListView GettingStarted

## About the sample
This repository contains the sample to get started with the Syncfusion's ListView control

Create a new blank (Xamarin.Forms.Portable) application in Xamarin Studio or Visual Studio for Xamarin.Forms.
Import the SfListView control namespace Syncfusion.ListView.XForms and set the SfListView control to the ContentPage.

```xml

<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:syncfusion="clr-namespace:Syncfusion.ListView.XForms;assembly=Syncfusion.SfListView.XForms"
             xmlns:local="clr-namespace:GettingStarted;assembly=GettingStarted"
             x:Class="GettingStarted.MainPage">
  <syncfusion:SfListView x:Name="listView" />
</ContentPage>

```
```c#
using Syncfusion.ListView.XForms;
using Xamarin.Forms;

namespace GettingStarted
{
    public class App : Application
    {
        SfListView listView;
        public App()
        {
            listView = new SfListView();
            MainPage = new ContentPage { Content = listView };
        }
    }
} 
```

Create a data model to bind it to the control. 

```c#
public class BookInfo : INotifyPropertyChanged
{
    private string bookName;
    private string bookDesc;

    public string BookName
    {
        get { return bookName; }
        set
        {
            bookName = value;
            OnPropertyChanged("BookName");
        }
    }

    public string BookDescription
    {
        get { return bookDesc; }
        set
        {
            bookDesc = value;
            OnPropertyChanged("BookDescription");
        }
    }

    public event PropertyChangedEventHandler PropertyChanged;

    public void OnPropertyChanged(string name)
    {
        if (this.PropertyChanged != null)
           this.PropertyChanged(this, new PropertyChangedEventArgs(name));
    }
}
```

Create a model repository class with BookInfo collection property initialized with required number of data objects.

```c#
public class BookInfoRepository
{
    private ObservableCollection<BookInfo> bookInfo;

    public ObservableCollection<BookInfo> BookInfo
    {
        get { return bookInfo; }
        set { this.bookInfo = value; }
    }

    public BookInfoRepository()
    {
        GenerateBookInfo();
    }

    internal void GenerateBookInfo()
    {
        bookInfo = new ObservableCollection<BookInfo>();
        bookInfo.Add(new BookInfo() { BookName = "Object-Oriented Programming in C#", BookDescription = "Object-oriented programming is a programming paradigm based on the concept of objects" });
        bookInfo.Add(new BookInfo() { BookName = "C# Code Contracts", BookDescription = "Code Contracts provide a way to convey code assumptions" });
        bookInfo.Add(new BookInfo() { BookName = "Machine Learning Using C#", BookDescription = "You’ll learn several different approaches to applying machine learning" });
        bookInfo.Add(new BookInfo() { BookName = "Neural Networks Using C#", BookDescription = "Neural networks are an exciting field of software development" });
        bookInfo.Add(new BookInfo() { BookName = "Visual Studio Code", BookDescription = "It is a powerful tool for editing code and serves for end-to-end programming" });
        bookInfo.Add(new BookInfo() { BookName = "Android Programming", BookDescription = "It is provides a useful overview of the Android application life cycle" });
        bookInfo.Add(new BookInfo() { BookName = "iOS Succinctly", BookDescription = "It is for developers looking to step into frightening world of iPhone" });
        bookInfo.Add(new BookInfo() { BookName = "Visual Studio 2015", BookDescription = "The new version of the widely-used integrated development environment" });
        bookInfo.Add(new BookInfo() { BookName = "Xamarin.Forms", BookDescription = "Its creates mappings from its C# classes and controls directly" });
        bookInfo.Add(new BookInfo() { BookName = "Windows Store Apps", BookDescription = "Windows Store apps present a radical shift in Windows development" });
    }
}
```

## <a name="requirements-to-run-the-demo"></a>Requirements to run the demo ##

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.

## Related links
[Learn More about Xamarin ListView](https://www.syncfusion.com/xamarin-ui-controls/xamarin-listView/?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples) <br/><br/>
[Download Free Trial](https://www.syncfusion.com/downloads?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples) <br/><br/>
[Pricing](https://www.syncfusion.com/sales/products/xamarin?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples) <br/><br/>
[Documentation](https://help.syncfusion.com/xamarin/listView/getting-started?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples) <br/><br/>
[Online Examples](https://github.com/SyncfusionExamples/ListView-GettingStarted-in-Xamarin-Forms?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples) <br/><br/>
[Community Forums](https://www.syncfusion.com/forums/xamarin.forms/sflistview?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples) <br/><br/>
[Suggest a feature](https://www.syncfusion.com/feedback/xamarin-forms?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples)

## About Syncfusion Xamarin.Forms
Syncfusion's [Xamarin.Forms](https://www.syncfusion.com/xamarin-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples) library offers over 155 UI components to create cross-platform native mobile apps for iOS, Android, UWP and macOS platforms from a single C# code base. In addition to ListView, we provide popular Xamarin components such as [DataGrid](https://www.syncfusion.com/xamarin-ui-controls/xamarin-datagrid?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),[Charts](https://www.syncfusion.com/xamarin-ui-controls/xamarin-charts?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[Scheduler](https://www.syncfusion.com/xamarin-ui-controls/xamarin-scheduler?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples), [Diagram](https://www.syncfusion.com/xamarin-ui-controls/xamarin-diagram?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples), and [Maps](https://www.syncfusion.com/xamarin-ui-controls/xamarin-maps?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples).

## About Syncfusion
Founded in 2001 and headquartered in Research Triangle Park, N.C., Syncfusion has more than 23,000+ customers and more than 1 million users, including large financial institutions, Fortune 500 companies, and global IT consultancies.
 
Today, we provide 1600+ controls and frameworks for web
([Blazor](https://www.syncfusion.com/blazor-components?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[ASP.NET Core](https://www.syncfusion.com/aspnet-core-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[ASP.NET MVC](https://www.syncfusion.com/aspnet-mvc-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[ASP.NET WebForms](https://www.syncfusion.com/jquery/aspnet-webforms-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[JavaScript](https://www.syncfusion.com/javascript-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[Angular](https://www.syncfusion.com/angular-ui-components?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[React](https://www.syncfusion.com/react-ui-components?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[Vue](https://www.syncfusion.com/vue-ui-components?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
and 
[Flutter](https://www.syncfusion.com/flutter-widgets?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples)),
mobile
([Xamarin](https://www.syncfusion.com/xamarin-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[Flutter](https://www.syncfusion.com/flutter-widgets?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[UWP](https://www.syncfusion.com/uwp-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
and
[JavaScript](https://www.syncfusion.com/javascript-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples)),
and desktop development ([Windows
Forms](https://www.syncfusion.com/winforms-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[WPF](https://www.syncfusion.com/wpf-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[WinUI(Preview)](https://www.syncfusion.com/winui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples),
[Flutter](https://www.syncfusion.com/flutter-widgets?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples)
and
[UWP](https://www.syncfusion.com/uwp-ui-controls?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples)).
We provide ready-to-deploy enterprise software for dashboards, reports,
data integration, and big data processing. Many customers have saved
millions in licensing fees by deploying our software.

		
<hr style="height:0.3px;border:none;color:lightgrey;background-color:lightgrey;" />

<p align="center">
  <a href="mailto:sales@syncfusion.com?Subject=Syncfusion Xamarin ListView - Github" target="_top">sales@syncfusion.com</a> | <a href="https://www.syncfusion.com?utm_source=github&utm_medium=listing&utm_campaign=xamarin-listview-github-samples">www.syncfusion.com</a> | 1-888-9 DOTNET <br>
</p>
