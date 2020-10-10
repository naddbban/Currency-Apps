# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap senilai Rp. 15.000

## Scope and Functionalities
- user dapat memasukkan angka
- user dapat menyentuh tombol hitung
- user mendapat info 'INVALID' jika yang dimasukkan berupa text

## How Does it works?
Diawali dari methods `MainWindow` pada class MainWindow.xaml.cs kita mendeklarasikan  ...
```csharp
	public MainWindow()
        {
            InitializeComponent();
            currencyController = new CurrencyController();
        }
```
logika perhitungan terdapat pada class `CurrencyController.cs` sebagai berikut
```csharp
    public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```