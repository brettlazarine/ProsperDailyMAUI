## ProsperDailyMAUI

This is a project focusing on the implementation of SQLite, led by Hector Perez on his Udemy course: *.NET MAUI course with Visual Studio 2022 creating PROJECTS*

**NuGet Packages**
- *Humanizer* adjusts the display template of *OperationDate* to give it a more appealing and friendly format
- *Fody* implements *INotifyPropertyChanged* with minimal code
- *Syncfusion* allows for the creation and binding of the *StatisticsPage* chart
- *SQLite* allows for the creation of database storage for the application

**Views**
- *AppContainer* creates a TabbedPage layout for ease of page navigation
- *DashboardPage* acts as the MainPage, binding and displaying Model info that updates when new transactions are added
- *TransactionsPage* allows for the creation of a *Transaction*
- *StatisticsPage* displays the *Transaction* Collection like *DashboardPage*, but also displays a chart for a visual representation

**ViewModels**
- *DashboardViewModel* implements *FillData()*, which orders *Transactions* and applies each *transaction* to *Income* or *Expenses*, then to *Balance*
- *TransactionsViewModel* uses *SaveTransaction()* to save the created *Transaction* to the database
- *StatisticsViewModel* utilizes *GetTransactionSummary()* to group and order all *transactions* for the chart in the View

**Converters**
- *AmountToColorConverter* and *AmountToCurrencyConverter* detect if a *Transaction* is *Income* or *Expense*, and then applies the appropriate style to that Label

**Repositories**
- *BaseRepository* houses all of the necessary Methods for interacting with the SQLite database
