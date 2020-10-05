# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap senilai Rp 15.000
## Scope & Funcionalities
* User dapat memasukkan angka
* User dapat menyentuh tombol hotung
* User mendapat info "INVALID" jika yang dimasukkan berupa text 
## How Does it works?
Diawali dengan method `MainWindow` pada class `MainWindows.xml.cs` kita mendeklarasikan `InitializeComponent()` berfugsi sebagai method yang membuat dan menginisialisasi user interface object yang telah dibuat, selanjutnya yaitu membuat object dari class `CurrencyController.cs` dengan syntax `currencyController = new CurrencyController();`

```csharp
    public MainWindow()
        {
            InitializeComponent();
            currencyController = new CurrencyController();
        }
``` 
 logika perhitungan terdapat pada class `CurrencyController.cs` sebagai berikut cara kerjanya pertama mendeklarasikan variabel baru yaitu nominalDouble yang berisi nilai variabel nominal yang telah diconvert menjadi double, selanjutnya membuat variabel result yang berisi `nominalDouble * 15000` kemudian nilai result kita convert ke string dan dikembalikan ke nominal  
```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```