# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap Rp.15.000

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info "INVALID" jika yang dimasukkan berupa text 

## How Does It works?

Diawali dari method `MainWindow` pada class MainWindow.xaml.cs

```csharp
    public MainWindow()
            {
                InitializeComponent();
                currency = new CurrencyController();
            }
```

logika perhitungan terdapat pada class `CurrencyControler.cs` sebagai berikut

cara kerjanya adalah mengalikan bilangan yang diinputkan pada tabel (USD) dengan nama variabel nominalDouble dengan angka 15.000 kemudian menampilkan hasilnya pada tabel (IDR) dengan nama variabel result dengan tipe data yang telah di convert menjadi string
```csharp
    public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```
