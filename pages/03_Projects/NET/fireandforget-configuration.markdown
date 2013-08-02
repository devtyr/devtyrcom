Title: FireAndForget - Configuration - DevTyr
Description: Easy to configure, lightweight and asynchronous message bus
Keywords: FireAndForget, Message, Service, Bus, Lightweight, Asynchronous
Author: DevTyr / Norbert Eder
Menu: FireAndForget
MenuTitle: Configuration
Sidebar: FireAndForget
Template: page_sidebar
Directory: projects/fireandforget
-----

## Configuration

There is not a lot to configure. Nearly all configurations are stored in the `app.config` of the console application. Per default the Message Bus is executed as a self hosted HTTP container within a console application. The section `ServiceBusConfiguration` is necessary for `FireAndForget` to run. There are very important settings:

* `appSettings`: Use the key `repository` to configure the implemenation of data access. This is by default the SQL Server. The connection string is configured in the default settings of the `app.config`.
* `Server`: This is the URI the server listening for messages
* `Workers`: Configure named workers here. For each worker an own queue is created
* `Executors`: Executors are mapped to message types (see section *Messages* below) and a specific worker. Please note: there is no registration for message events, it is a direct mapping, nothing more.

<pre>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot; ?&gt;
&lt;configuration&gt;
  &lt;configSections&gt;
    &lt;section name=&quot;ServiceBusConfiguration&quot; 
             type=&quot;FireAndForget.Configuration.ServiceBusConfigurationSection, FireAndForget&quot;/&gt;
  &lt;/configSections&gt;
  
  &lt;appSettings&gt;
    &lt;add key=&quot;repository&quot; 
         value=&quot;FireAndForget.Core.Persistence.SqlServerRepository, FireAndForget.Core&quot;/&gt;
  &lt;/appSettings&gt;
  &lt;connectionStrings&gt;
    &lt;add name=&quot;sqlserver&quot; connectionString=&quot;Server=localhost;Database=FireAndForget;Trusted_Connection=True;&quot; providerName=&quot;System.Data.SqlClient&quot;/&gt;
  &lt;/connectionStrings&gt;

  &lt;ServiceBusConfiguration&gt;
    &lt;Server uri=&quot;http://localhost:2900&quot;/&gt;
    &lt;Workers&gt;
      &lt;Worker name=&quot;default&quot;/&gt;
      &lt;Worker name=&quot;test&quot;/&gt;
    &lt;/Workers&gt;
    &lt;Executors&gt;
      &lt;Executor worker=&quot;default&quot; 
                type=&quot;FireAndForget.TestClient.TaskExecutors.DefaultTaskExecutor, FireAndForget.TestClient&quot;/&gt;
      &lt;Executor worker=&quot;test&quot; 
                type=&quot;FireAndForget.TestClient.TaskExecutors.TestTaskExecutor, FireAndForget.TestClient&quot;/&gt;
    &lt;/Executors&gt;
  &lt;/ServiceBusConfiguration&gt;
&lt;/configuration&gt;
</pre>

If you create your own executor that needs a configuration, add the settings to the `app.config` and read it within your executor.

## Database

All messages are persisted, so erroneous/unfinished tasks can be reexecuted, if necessary. Therefore a storage is needed. By default there is an implementation for Microsoft SQL Server. The needed table and indices are created by FireAndForget. All you need is to create and/or configure the used database within the connection string.