# GChartsDataTableBlazorfied

Author: Ryan Kueter  
Updated: November, 2023

## About

**GChartsDataTableBlazorfied** provides a Google Charts datatable builder for the GChartsBlazorfied library.

### Targets:
- .NET 7, .NET 8

## Introduction

This library provides a Google Charts datatable builder. Developers have the option of using an object array as a data source for the GChartsBlazorfied library. But if developers want to use the more advanced features of Google Charts, such as tooltips, then the Google Charts datatable builder is required.

```csharp
// Example object array
private List<object> ObjectArray = new List<object>
{
    new List<object>() { "Year", "Sales", "Expenses", "Losses" },
    new List<object>() { "2013", 1000, 400, 100 },
    new List<object>() { "2014", 1170, 460, 50 },
    new List<object>() { "2015", 660, 1120, 20 },
    new List<object>() { "2016", 1030, 540, 30 }
};

// Example GChartsDataTable builder
private gcDataTableBuilder GetDataTable()
{
    var DataTableBuilder = new gcDataTableBuilder();
    DataTableBuilder.Columns!.Add(new gcColumn() { label = "Year", type = gcType.String });
    DataTableBuilder.Columns!.Add(new gcColumn() { label = "Sales", type = gcType.Number });
    DataTableBuilder.Columns!.Add(new gcColumn() { type = gcType.String, role = gcRole.Tooltip, p = new gcP { html = true } });
    DataTableBuilder.Columns!.Add(new gcColumn() { label = "Expenses", type = gcType.Number });
    DataTableBuilder.Columns!.Add(new gcColumn() { type = gcType.String, role = gcRole.Tooltip, p = new gcP { html = true } });
    DataTableBuilder.Columns!.Add(new gcColumn() { label = "Losses", type = gcType.Number });
    DataTableBuilder.Columns!.Add(new gcColumn() { type = gcType.String, role = gcRole.Tooltip, p = new gcP { html = true } });
    DataTableBuilder.AddRow()
        .AddCell("2013")
        .AddCell(1000)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2013</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(400)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2013</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(100)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2013</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""");
    DataTableBuilder.AddRow()
        .AddCell("2014")
        .AddCell(1170)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2014</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(460)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2014</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(50)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2014</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""");
    DataTableBuilder.AddRow()
        .AddCell("2015")
        .AddCell(660)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2015</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(1120)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2015</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(20)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2015</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""");
    DataTableBuilder.AddRow()
        .AddCell("2016")
        .AddCell(1030)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2016</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(540)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2016</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""")
        .AddCell(30)
        .AddCell(""""<div style="padding: 10px"><h1>Html Tooltip 2016</h1> <a href="https://developers.google.com/chart">Google Charts</a></div>"""");
    return DataTableBuilder;
}

// To build the table, you call the build method:
DataTableBuilder.Build();
```

###
## Contributions

This project is being developed for free by me, Ryan Kueter, in my spare time. So, if you would like to contribute, please submit your ideas on the Github project page.