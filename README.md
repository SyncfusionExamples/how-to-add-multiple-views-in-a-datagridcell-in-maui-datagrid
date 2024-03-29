# How to add multiple Views in a DataGridCell in MAUI DataGrid
The [MAUI DataGrid](https://www.syncfusion.com/maui-controls/maui-datagrid) (SfDataGrid) allows add multiple views in a [DataGridCell](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridCell.html) in SfDataGrid using the [DataGridTemplateColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridTemplateColumn.html). You can load any number of views in a DataGridCell by customizing the [CellTemplate](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridTemplateColumn.html#Syncfusion_Maui_DataGrid_DataGridTemplateColumn_CellTemplate) property of the DataGridTemplateColumn.

The below code illustrates how to add multiple views in a DataGridCell.

## XAML
```XML
<syncfusion:SfDataGrid x:Name="dataGrid"
                        AutoGenerateColumnsMode="None"
                    ColumnWidthMode="Fill"
                    ItemsSource="{Binding OrdersInfo}"
                    RowHeight="180">
    <syncfusion:SfDataGrid.Columns>
        <syncfusion:DataGridTemplateColumn HeaderText="Orders Information" MappingName="OrderID">
            <syncfusion:DataGridTemplateColumn.CellTemplate>
                <DataTemplate>
                    <Grid>
                        <Grid.ColumnDefinitions>
                            <ColumnDefinition Width="100" />
                            <ColumnDefinition Width="100" />
                            <ColumnDefinition Width="100" />
                        </Grid.ColumnDefinitions>
                        <Grid.RowDefinitions>
                            <RowDefinition Height="40" />
                            <RowDefinition Height="40" />
                            <RowDefinition Height="40" />
                            <RowDefinition Height="40" />
                        </Grid.RowDefinitions>
                        <Label Grid.Row="0"
                    Grid.Column="0"
                    FontAttributes="Bold"
                    HorizontalTextAlignment="Center"
                    Text="OrderID"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="0"
                    Grid.Column="1"
                    HorizontalTextAlignment="Center"
                    Text=":"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="0"
                    Grid.Column="2"
                    HorizontalTextAlignment="Center"
                    Text="{Binding OrderID}"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="1"
                    Grid.Column="0"
                    FontAttributes="Bold"
                    HorizontalTextAlignment="Center"
                    Text="CustomerID"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="1"
                    Grid.Column="1"
                    HorizontalTextAlignment="Center"
                    Text=":"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="1"
                    Grid.Column="2"
                    HorizontalTextAlignment="Center"
                    Text="{Binding CustomerID}"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="2"
                    Grid.Column="0"
                    FontAttributes="Bold"
                    HorizontalTextAlignment="Center"
                    Text="Freight"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="2"
                    Grid.Column="1"
                    HorizontalTextAlignment="Center"
                    Text=":"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="2"
                    Grid.Column="2"
                    HorizontalTextAlignment="Center"
                    Text="{Binding Freight}"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="3"
                    Grid.Column="0"
                    FontAttributes="Bold"
                    HorizontalTextAlignment="Center"
                    Text="Country"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="3"
                    Grid.Column="1"
                    HorizontalTextAlignment="Center"
                    Text=":"
                    TextColor="Black"
                    VerticalTextAlignment="Center" />
                        <Label Grid.Row="3"
                    Grid.Column="2"
                    HorizontalTextAlignment="Center"
                    Text="{Binding Country}"
                    VerticalTextAlignment="Center" />
                    </Grid>
                </DataTemplate>
            </syncfusion:DataGridTemplateColumn.CellTemplate>
        </syncfusion:DataGridTemplateColumn>
    </syncfusion:SfDataGrid.Columns>
</syncfusion:SfDataGrid>
```

![MultipleViewInDataGridCell](MultipleViewInSfDataGrid.png)
## Conclusion
I hope you enjoyed learning about how to add multiple views in a DataGridCell in MAUI DataGrid (SfDataGrid).

You can refer to our [.NET MAUI DataGrid’s feature tour](https://www.syncfusion.com/maui-controls/maui-datagrid) page to know about its other groundbreaking feature representations. You can also explore our .NET MAUI DataGrid Documentation to understand how to present and manipulate data.
For current customers, you can check out our .NET MAUI components from the [License and Downloads](https://www.syncfusion.com/account/downloads) page. If you are new to Syncfusion, you can try our 30-day free trial to check out our .NET MAUI DataGrid and other .NET MAUI components.
If you have any queries or require clarifications, please let us know in comments below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [Direct-Trac](https://support.syncfusion.com/account/login?ReturnUrl=%2Faccount%2Fconnect%2Fauthorize%2Fcallback%3Fclient_id%3Dc54e52f3eb3cde0c3f20474f1bc179ed%26redirect_uri%3Dhttps%253A%252F%252Fsupport.syncfusion.com%252Fagent%252Flogincallback%26response_type%3Dcode%26scope%3Dopenid%2520profile%2520agent.api%2520integration.api%2520offline_access%2520kb.api%26state%3D8db41f98953a4d9ba40407b150ad4cf2%26code_challenge%3DvwHoT64z2h21eP_A9g7JWtr3vp3iPrvSjfh5hN5C7IE%26code_challenge_method%3DS256%26response_mode%3Dquery) or [feedback portal](https://www.syncfusion.com/feedback/maui?control=sfdatagrid). We are always happy to assist you!