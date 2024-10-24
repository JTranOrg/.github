
### All Things Related to JTran

#### What is JTran?
JTran is a portmanteau that comes from "Json Transformation". It is a language that is itself a Json document that describes how to transform one json document into another. It borrows concepts and in some cases syntax from XSLT.

    {
       "#foreach(Vehicles, Cars)":
       {
           "Make":          "#(Manufacturer)",
           "Model":         "#(Model)",
           "Year":          "#(Year)",
           "PrimaryDriver": "#(Drivers[0].FirstName + ' ' + Drivers[0].LastName)"
       }
    }

##### Some of the main benefits/features of JTran are:

- Simple but powerful language based on Json.
- Ability to customize
    - Create custom functions in any .Net language or in JTran itself.
    - Create custom elements using JTran.
- Data source can be a json document, a collection/enumerable or even a POCO.
- Transform large sets of data 
    - Stream a large json file
    - Transform source can be any collection (IEnumerable), e.g. a database collection


For a complete JTran language reference go [here](https://github.com/JTranOrg/JTran/blob/master/docs/reference.md).

#### JTran Nuget package

The JTran repository below contains a project for creating the main .Net NuGet package that you reference in your .Net projects in order to do JTran transformations.

#### JTran Console App

The JTran repository below also contains a project for creating the console app to do command line transformations. This console app is also available in NuGet as a dotnet tool.

#### JTran Azure DevOps Custom Task

You can do JTran transformations in your Azure Devops pipelines using the [Azure DevOps Custom Task](https://marketplace.visualstudio.com/items?itemName=JTranOrg.JTranTransform). The JTran.CICD repository below contains the code for that custom task.

