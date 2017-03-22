# SSRS_Questions
Interview Questions

Q. What is SSRS?

    SSRS or SQL Server Reporting Service is a server-based report generation software systems from Microsoft and is part of Microsoft BI.
    It is used for preparing and delivering interactive and variety of reports.
    It is administered through an web based interface.
    Reporting services utilizes a web service interface for supporting and developing of customized reporting applications.
    SSRS lets you create very rich reports (Tabular/Graphical/Interactive) from various datasources with rich data visualization (Charts, Maps, sparklines)
    SSRS allows are reports to be exported in various formats (Excel, PDF, word etc)

Q. Explain SSRS Architecture?

Reporting services architecture comprises of integrated components. It is a multi-tiered, included with application, server and data layers. This architecture is scalable and modular. A single installation can be used across multiple computers. It includes the following components: –
Report Manager, Reporting Designer, Browser Types Supported by Reporting services, Report server, Report server command line utilities, Report Server Database, Reporting Services Extensibility, Data sources that is supported by Reporting Services.

Q: Explain Reporting Life Cycle?

Reporting Services has mainly three phases:

    Development of Reports (Developer) – First of all a report needs to be design which is primarily done by report developer
    Management of Reports (DBA) – Once the Report is being developed, DBA need to ensure
    Security – Only authorized user should access the report
    Execution – How the report will be executed to optimize data sources performance
    Scheduling of reports – so that report are executed on scheduled timings
    Report Delivery (DBA + Developer) – Once the report is being developed and executed now the report should be reached to final recipients (business users) who are going to understand / analyze report data. if any changes, we again go back to development stage.

Q. What are the Reporting Services components?

Reporting services components assist in development. These processing components include some tools that are used to create, manage and view reports.

    Report Designer is used to create the reports.
    Report Sever is used to execute and distribute reports.
    Report Manager is used to manage the report server.

Q. SQL Server Reporting Services vs. Crystal Reports.

Crystal reports are processed by IIS while SSRS have a report server. Caching in Crystal reports is available through cache server. On the other hand, caching in SSRS is available for Report history snapshots. Crystal reports have standards and user defined field labels. SSRS allows only user defined field labels.
Q. How does the report manager work in SSRS?

Report manager is a web application. In SSRS it is accessed by a URL. The interface of this Report manager depends on the permissions of the user. This means to access any functionality or perform any task, the user must be assigned a role. A user with a role of full permissions can entire all the features and menus of the report. To configure the report manager, a URL needs to be defined.
Q. How can I add Reporting Services reports to my application?

Visual Studio / SSDT / BI Data Tools (Standard and Enterprise editions) contains a set of freely redistributable Report Viewer controls that make it easy to embed Reporting Services functionality into custom applications. Two versions of the Report Viewer exist, one for rich Windows client applications and one for ASP.NET applications.
Q. Do I need a report server to run reports in my application?

In addition to publishing reports to a report server, you can build reports using the Report Designer that is directly integrated with Visual Studio language projects. You can embed reports directly in any Windows Forms or ASP.NET Web application without access to a report server. The data access in embedded reports is a natural extension of the Visual Studio data facilities. Not only can you use traditional databases as a source of data for your reports, you can use object collections as well.
Q. What are different types of roles provided by SSRS?

    Browsers
    Content Manager
    My Reports
    Publishers
    Report Builder

Q. Name and Describe few console utilities for SSRS?

RSConfig.exe: Configuration of connection properties between the Report Server to the repository database.
RSKeyMgmt.exe: Management of encryption keys via command-line
RS.exe: Utility used for deploying the report on report server
Q. What are the drawbacks of reporting in SSRS?

For many years, Microsoft had no direct solution for reporting with the SQL Server besides Crystal Reports. Now, they have SQL Server Reporting Services, but it does have several drawbacks. It is still complex to understand the complete functionality and structure of this new component, and many users are still relying on the reporting application they are more familiar with, which is Crystal Reports. Also, components in SSRS like Report Builder and Report Designer are meant for different users for different aspects of the report process, yet complete understanding and exposure to both is important to utilize both functions fully and extensively. There are also issues when exporting very large reports to Microsoft Excel, as it can lead to a loss of data.
Q. What are the three different part of RDL file explain them?

In visual studio RDL files has three parts.

    Data: It contains the dataset on which we write the query. Data set is connected with data source.
    Design: In design you can design report. Can create tables and matrix reports. Drag columns values from source.
    Preview: to check the preview after the report run.

Q. Which language rdl files made of?

RDL files are written in XML.
Q. Can you edit the .rdl code associated with a linked report?

No, because a linked report has no .rdl code of its own. It refers to the .rdl code of the base report
Q. What is report rendering ?

Exporting a report data with design o different type of file types is knows as Report rending. SQL Server Reporting Services supports multiple rendering extensions like Word, Excel, CSV, PDF, HTML etc.
Q. What are the different types of data sources in SSRS?

SSRS use different data source. Some of them are listed below.

    Microsoft SQL Server
    OLEDB
    Oracle
    ODBC
    SQL Server Analysis Service
    Report Server Model
    SAP Net weaver BI
    Hyperion
    Teradata
    XML

Q. What is the name of reporting services config file and what’s it’s used for?

Reporting service config file is used for report configuration details. It contains the report format and also the report import types. Report service config reside at ISS.
Q. What are Advantages of SSRS or why we should use SSRS?

The SQL Server Reporting Services or SSRS has some Advantages

    It is faster and cheaper
    Efficient reporting access to information residing in both Oracle and MS SQL Server databases
    No need for expensive specialist skills
    The default report designer is integrated with Visual Studio .NET so that we can create application and its reports in the same environmen
    The security is managed in a role-based manner and can be applied to folders as well as reports
    Once parameters are defined, the UI for these parameters is automatically generated
    Subscription based reports are automatically sent by mail to the users

Q. What are the limitations/drawbacks or SSRS 2008 R2?

The SSRS 2008 R2 has some limitations. Some limitations are given below:

    There is no print button. In order to print need to export excel, PDF or others format
    It is very hard to debug expression or custom code
    Its does not use page number or total pages in report body
    Don’t support rounding rectangle
    There is no way to pass values from sub-reports to main report
    It is not possible to insert a sub-report into the page header or page footer
    Page header creates extra spaces in the next pages

Q. What are the Export Options of SSRS?

SSRS allow many ways of rendering the reports:

    HTML (MHTML)
    Excel
    Acrobat
    Tiff (image)
    XML
    CSV

Q. What is report snapshot?

Snapshot means a instance of a report for future reference, that means a copy of report (data is freezed) will be saved on a report server for future reference.
Q. What are Data Driven Subscriptions?

Reporting Services provides data-driven subscriptions so that you can customize the distribution of a report based on dynamic subscriber data. Data-driven subscriptions are intended for the following kinds of scenarios: Distributing reports to a large recipient pool whose membership may change from one distribution to the next. For example distribute a monthly report to all current customers. Distributing reports to a specific group of recipients based on predefined criteria. For example send a sales performance report to the top ten sales managers in an organization.
Q. When to Use Null Data driven Subscription?

Create a data-driven subscription that uses the Null Delivery Provider. When you specify the Null Delivery Provider as the method of delivery in the subscription, the report server targets the report server database as the delivery destination and uses a specialized rendering extension called the null rendering extension. In contrast with other delivery extensions, the Null Delivery Provider does not have delivery settings that you can configure through a subscription definition.
Q. How to fine-tune Reports?

To tune-up the Reporting Services, follow the below mentioned ways: – Expand the Server or utilizing the reporting services of another database server. For better embedding of report contents, report application’s logic and characteristics can have a duplicate copy of data. – Replication of data continuously. Using (nolock), the issues of locking can well be resolved and the performance of the query can be improved. This can be done by using dirty read at the time of duplicating the data is unavailable.
Q. User wants only to display only PDF as export option in report Manager. How to achieve this?

You need to edit RsReportServer.Config file to limit the exporting extensions to only PDF.
You can find the file under;
%Program Files%\Microsoft SQL Server\MSRS10.\Reporting Services\ReportServer\
Q. Can you import Microsoft Excel data to SSRS?

Reporting Services does not import data. It only queries data in whatever format it is stored in their native storage system. I will assume that you’re asking whether you can create reports and use Excel spreadsheets as data sources. The answer is Yes, Reporting Services supports a wide variety of data sources, including Excel files. You’ll get the best performance with the built-in native .NET providers but you should be able to connect to any ODBC or OLE-DB data source, whether it comes from Microsoft or a third-party company.
Q. Difference between Logical Page and Physical Page in SSRS.

Logical page breaks are page breaks that you insert before or after report items or groups. Page breaks help to determine how the content is fitted to a report page for optimal viewing when rendering or exporting the report. The following rules apply when rendering logical page breaks: Logical page breaks are ignored for report items that are constantly hidden and for report items where the visibility is controlled by clicking another report item. Logical page breaks are applied on conditionally visible items if they are currently visible at the time the report is rendered. Space is preserved between the report item with the logical page break and its peer report items. Logical page breaks that are inserted before a report item push the report item down to the next page. The report item is rendered at the top of the next page. Logical page breaks defined on items in table or matrix cells are not kept. This does not apply to items in lists.
Q. Name few Endpoints exposed by SSRS 2012?

    Management Endpoints
    Execution Endpoint
    SharePoint Proxy Endpoints

Q. What are the new features are introduced in SQL Server 2012 reporting services?

    Power View – interactive data exploration
    SQL Server 2012 is fully integrated with SharePoint
    Introduction to Data Alerts, data alerts are a data-driven alerting solution that informs you about changes in report data that are of interest to you, and at a relevant time
    SQL Server Data tool
    New rendering extensions supports MS Office 2010
    Project Crescent is being introduced

Q. What new data source types were added in SSRS 2014?

In addition to the data source types available in SSRS (SQL Server, Oracle, ODBC, OLE DB), the following have been added in SSRS 2012: SQL Server Analysis Services SQL Server Integration Services SQL Server Report Builder Models XML (through URL and Web services)
Q. Is SSRS support other database except MS SQL Server?

Yes. SSRS can be building based on relational or multidimensional data source like Oracle, OLEDB. ODBC etc
Q. What is Query parameter in SSRS?

Query parameters is mentioned in the query of the datasources that are to be included into the SQL script’s WHERE clause of the SQL that can accept parameters. Query parameters begin with the symbol @.The name should not contain spaces and can not begin with numeral. For clarity, we use only letters.
Q. What is a matrix in SSRS?

A matrix is a data region linked to a report set. Matrix allows us to create crosstab reports with the report variables displaying on rows and columns. It allows us to drag and drop fields into it.
Q. What are sub reports and how to create them?

A sub report is like any other reports which can be called in main report and can be generate through main report. Parameters can be passed from main report to sub report and basis of that report can be generated.
Q. What is the chart in report?

Chart reports are for graphical representation. You can get pie charts columns harts and various other options. 3d charts are also available in reporting services.
Q. How to add the custom code in Report?

To add the custom codes in report go to report tab on top then properties and there you will find the options for custom code.
Q. In case you have filters in your report, when filters will be applied in Cached Report instance?

Filters are applied when a report is rendered, Filters will not create a new cached instance on the Report Server.
Q. What are data regions?

Data regions are report items that display repeated rows of summarized information from datasets.
Q. You want to generate a report that is formatted as a chart. Can you use the Report Wizard to create such a report?

No, the Report Wizard lets you create only tabular and matrix reports. you must create the chart report directly by using the Report Designer.
Q. Can we use datagrids for our report in SSRS?

We have an ASP.NET project that populates a datagrid. Using datagrid as my datasource for my report using SQL Server Reporting Services. Is this possible? The simple answer is no. However, nothing’s ever simple. A set of reporting controls was added in Visual Studio 2010 allowing you to report in a dataset, on data that was supplied by you. So, if you retrieved your data into a dataset, bound the datagrid to the dataset so it had data to display, you could then use that dataset as the datasource for the reporting controls. These are then client-side reports, not server reports though.
Q. Describe different Processing Modes offered by SSRS?

    Local Processing Mode: Processes reports in the client application.
    Remote Processing Mode: Renders server reports that are processed on a SQL Server Reporting Services report server.

Q. What is ReportServer and ReportServerTempDB ?

Reporting Services uses two SQL Server databases for storage by default, the databases are named ReportServer and ReportServerTempdb.
ReportServer is a main database, which store all internal configuration and report meta data whereas ReportServerTempdb is used to store temporary data, session information, and cached reports.
Q. What is encryption key?

Encryption keys are used by the report server so that items such as connection strings are maintained securely. These keys are required in case you want to perform restoration of report server databases
Q. How to backup encryption key ?

Encryption Keys backup, use SQL Server Reporting Services Configuration tool to backup symmetric keys.
Q. What are the key configuration files for SQL Server Reporting Services ?

Mostly all Configuration files located at Install Directory:
\Microsoft SQL Server\\Reporting Services\ReportServer and  ReportManager
RSReportServer.config stores configuration settings for feature areas of the Report Server service: ReportManager, the Report Server Web service, and background processing.
RSSrvPolicy.config stores code access security policies for the server extensions.
RSMgrPolicy.config stores code access security policies for Report Manager
ReportingServicesService.exe.config stores configuration settings that specify the trace levels and logging options for the Report Server service.
RSReportDesigner.config contains settings for Report Designer and this file is located in the..\Program Files\Visual Studio 9.0\Common7\IDE\PrivateAssemblies
RSPreviewPolicy.config stores server extensions used during report preview and this file is located in ..\Program Files \Microsoft SQL Server\100\Tools \ReportDesigner
Q. What is Report Builder?

Report Builder is a business-user, ad-hoc report design client that allows users to design reports based on the business terms (Report Builder model) they are familiar with, but without needing to understand database schemas or how to write SQL or MDX queries. Report Builder works with both SQL Server and Analysis Services data sources.
Q. In which SQL Server version report builder introduced?

Report builder introduced in SQL Server 2005. While creating or deploying report model project on report server you can get error or it might not get created. For this you need to check whether the service pack 22 is installed or not.
Q. How does Report Builder support Analysis Services cubes?

Report Builder supports relational SQL and Analysis Services data sources in SQL Server. To create a model for Analysis Services cube, go to Report Manager or Management Studio, create a data source for your Analysis Services database, and then select the Generate Model option to create the model.
Q. How do users use Report Builder with SQL Server data sources?

While models that provide access to SQL Server Analysis Services are automatically generated on the report server, the Report Builder Model Designer can be used to generate or modify the models that are built on top of SQL Server relational databases. These model-building projects are a new type of project within a Visual Studio–based development shell.
Q. How do I get Report Builder to generate a parameter that can be set by users viewing the report?

In the filter dialog box, click the name of the criteria that you would like to prompt the user for when viewing the report. For example, for the criteria Order Year=2000, click Order Year. Select the Prompt option in the drop-down list.
Q. Can we run Reporting Services with SQL Server express edition, which is a free version of SQL Server?

Yes we can. SQL Server Express Edition with Advanced Services support Reporting Services. These is the free version.
Q. What are the limitations in SSRS on SQL Server express edition?

Microsoft offers reporting services free as part of SQL Server Express with Advance Services edition. But it has the following limitations:

    Management Studio cannot be used to administer report server
    Report Models will not be available
    Report Builder is not available
    Caching, History and Delivery of Report is not available.
    SQL Server agent is not available
    No scheduling is possible
    Remote server database is not available for Report Data Source (Local SQL Server is a only option,)
    We cannot store the report server database on a remote server (it has to be local only)
    Reports can be rendered only in Excel, PDF, Image formats only
    Reporting Services will not be able to use more than 1 GB of RAM
    No Subscriptions (Standard and Data Driven) can be made
    Can not be integrated with Share Point
    Can not implement Role based security
    Only named instances is supported
    Scale-out Report Servers will not be available

Q. What are the tools available in market as an Alternative to SQL Server Reporting Services?

    Non-Open Source:
        Actuate
        Hyperion (BRIO)
        SIEBEL-CRM
        BusinessObjects
        Oracle Express OLAP
        Qlikview
        Cognos
        Informatica Power Analyzer
        Proclarity
        IntelliView
        Dundas Chart for .NET
        MS-Excel
        SAS
        MicroStrategies
        Pentaho
    Open Source:
        Jasper Reports
        JFreeReport
        BIRT (Business Intelligence Reporting Tools)
        OpenReport
        DataVision
        Pentaho

Q. How to deploy the Report?

We can deploy SSRS report in three ways.

    Using Visual Studio: In visual studio we can directly deploy the report through Solution explorer by providing the report server URL in project properties at Target Server URL. As our choice this will deploy entire project or single report as.
    Using Report Server: We can directly go to the report server and deploy the report by browsing the report from the disk location of server.
    Creating the Utility: SQL server provides the facilities to Create a customize utility to deploy the report.

Q. What are the new features of SQL Server 2008 R2 reporting service?

The SQL Server 2008 R2 has introduced a lot of new features. Some of them are given below:

    New Report Types – Table, Matrix, List, Chart, and Sub report
    Some New Tools is added to report designer Toolbox
    Report Data Panel – built in page numbers
    Report Builder 3.0

Q. What are the new features of SQL Server 2012 reporting service?

The SQL Server 2012 has introduced a lot of new features. Some of them are given below:

    Power View – interactive data exploration
    SharePoint integration
    Introduction to Data Alerts
    SQL Server Data tool
    New rendering extensions (supports MS Office 2010)
    Project Crescent is being introduced

Q. How to backup SQL Server Reporting Services ?

There are mainly three things, which should be backed up as part of reporting services backup

    Report Server Databases, which can be backed up by SQL server backup and restore method.
    SQL Server Reporting Services Configuration, SQL Server Reporting Services Configuration is saved in config files, which can be copied as part of backup. look for other to know config files and there location.
    Encryption Keys backup, use SQL Server Reporting Services Configuration tool to backup symmetric keys.

Q. What is the web service used for reporting services?

Reporting Service Web Service used in SSRS. By accessing this web service you can access all report server component and also get the report deployed on report server.
Q. What is a cache in SSRS?

Report server can lay up a copy of processed report in a memory and return the copy when a user opens the report. This server memory is known as cache and the process is called caching.
Q. Can you always create a cache of a report?

No, you can create a cache of a report only when certain requirements, such as having credentials stored in the Report Server, are met.
Q. What are the Types of SSRS?

The types of SSRS are given below:

    Parameterized reports
    Linked reports
    Snapshot reports
    Cached reports
    Ad hoc reports
    Clickthrough reports
    Drilldown reports
    Drillthrough reports
    Subreports

Q. What is Parameterized Reports in SSRS ?

A parameterized report uses input values to complete report or data processing. With a parameterized report, you can vary the output of a report based on values that are set when the report runs. Parameterized reports are frequently used for drillthrough reports, linked reports, and subreports, connecting and filtering reports with related data.
Q. What is Linked Report?

A linked report is a report server item that provides an access point to an existing report. Conceptually, it is similar to a program shortcut that you use to run a program or open a file.
A linked report is derived from an existing report and retains the original’s report definition. A linked report always inherits report layout and data source properties of the original report. All other properties and settings can be different from those of the original report, including security, parameters, location, subscriptions, and schedules.
You can create a linked report on the report server when you want to create additional versions of an existing report. For example, you could use a single regional sales report to create region-specific reports for all of your sales territories.
Although linked reports are typically based on parameterized reports, a parameterized report is not required. You can create linked reports whenever you want to deploy an existing report with different settings
Q. What is Snapshot Report?

A report snapshot is a report that contains layout information and query results that were retrieved at a specific point in time. Unlike on-demand reports, which get up-to-date query results when you select the report, report snapshots are processed on a schedule and then saved to a report server. When you select a report snapshot for viewing, the report server retrieves the stored report from the report server database and shows the data and layout that were current for the report at the time the snapshot was created.
Report snapshots are not saved in a particular rendering format. Instead, report snapshots are rendered in a final viewing format (such as HTML) only when a user or an application requests it. Deferred rendering makes a snapshot portable. The report can be rendered in the correct format for the requesting device or Web browser.
Report snapshots serve three purposes:

    Report history: By creating a series of report snapshots, you can build a history of a report that shows how data changes over time.
    Consistency: Use report snapshots when you want to provide consistent results for multiple users who must work with identical sets of data. With volatile data, an on-demand report can produce different results from one minute to the next. A report snapshot, by contrast, allows you to make valid comparisons against other reports or analytical tools that contain data from the same point in time.
    Performance: By scheduling large reports to run during off-peak hours, you can reduce processing impact on the report server during core business hours.

Q. What is Cached Report?

A cached report is a saved copy of a processed report. Cached reports are used to improve performance by reducing the number of processing requests to the report processor and by reducing the time required to retrieve large reports. They have a mandatory expiration period, usually in minutes.
Q. What are Click through Reports?

A click through report is a report that displays related data from a report model when you click the interactive data contained within your model-based report. These reports are generated by the report server based on the information contained within the report model. The person who created the model determines which fields are interactive and which fields are returned when a click through report is opened. These field settings cannot be changed in the report authoring tools. Click through reports are auto-generated. However, you can create an alternative customized report to the model for interactive data items that is displayed instead. The custom report is a standard Reporting Services report.
Q. What are Drilldown Reports?

Drilldown reports initially hide complexity and enable the user to toggle conditionally hidden report items to control how much detail data they want to see. Drilldown reports must retrieve all possible data that can be shown in the report. For reports with large amounts of data, consider drill through reports instead.
Q. What are Drillthrough Reports?

Drillthrough reports are standard reports that are accessed through a hyperlink on a text box in the original report. Drillthrough reports work with a main report and are the target of a drillthrough action for a report item such as placeholder text or a chart. The main report displays summary information, for example in a matrix or chart. Actions defined in the matrix or chart provide drillthrough links to reports that display greater details based on the aggregate in the main report. Drillthrough reports can be filtered by parameters, but they do not have to be. Drillthrough reports differ from subreports in that the report does not display within the original report, but opens separately. They differ from clickthrough reports in that they are not autogenerated from the data source, but are instead custom reports that are saved on the report server. They differ from drilldown reports in that they retrieve the report data only for the specified parameters or for the dataset query.
Q. What is Subreport?

A subreport is a report that displays another report inside the body of a main report. Conceptually, a subreport is similar to a frame in a Web page. It is used to embed a report within a report. Any report can be used as a subreport. The subreport can use different data sources than the main report. The report that the subreport displays is stored on a report server, usually in the same folder as the parent report. You can set up the parent report to pass parameters to the subreport.
Although a subreport can be repeated within data regions using a parameter to filter data in each instance of the subreport, subreports are typically used with a main report as a briefing book or as a container for a collection of related reports. For reports with many instances of subreports, consider using drillthrough reports instead.
Q. What is Data Set in report?

Data set is a set of data which we want to show in report. Data source is the source of data from where we are getting this data (database server name, database name, connection string).
Q. Are there issues when exporting SSRS reports into Microsoft Excel? When my users are trying to export a SSRS report into Microsoft Excel, one or two columns in the report appear to merge together. Why might this be?

Exporting from SSRS is not always perfect, even if you stay within the Microsoft range of products. If you have extra resources, you could splurge for an add-on that offers much better control over exporting to Excel, such as OfficeWriter. From my experience, though, it is usually headers or footers that cause exporting issues. If any of these headers or footers overlap with data columns in your report, you will find that the exported version of the report has merged cells. Also, check columns next to each other to make sure that there is no overlap, as well.
Q. What is report subscription?

Subscriptions are standing requests to deliver report data to requested recipients. Once the report is being subscribed and subscriber will get updates from report server on scheduled interval.
Q. Can you use a stored procedure to provide data to an SSRS report?

Yes, you can use a stored procedure. However, your stored procedure should return only a single result set. If it returns multiple result sets, only the first one is used for the report dataset.
Q. How to send a SSRS report from SSIS?

Often there is a requirement to be able to send a SSRS report in Excel, PDF or another format to different users from a SSIS package one it has finished performing a data load. In order to do this, first you need to create a subscription to the report. You can create a SSRS report subscription from Report Manager. At the report subscription you can mention the report format and the email address of the recipient. When you create a schedule for the SSRS report, a SQL Server Agent Job will be created. From the SSIS, by using sp_start_job and passing the relevant job name you can execute the SSRS report subscription.
Q. You want to use BIDS to deploy a report to a different server than the one you chose in the Report Wizard. How can you change the server URL?

You can right-click the project in Solution Explorer and then change the Target-Server URL property.
Q. Can we deploy SSRS reports on our personal website?

Your reports can only be deployed on a reporting services site. Your only option for viewing them from other sites is an HTTP link. Some tools, like SharePoint offer controls allowing you to view reports in the context of the other websites, but the report is still deployed to and hosted from reporting services.

Reference: http://mindmajix.com/ssrs-interview-questions
