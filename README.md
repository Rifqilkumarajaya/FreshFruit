# FreshFruit

Aplikasi penjualan buah sederhana, dengan proses simpel hanya dengan memilih buah lalu memasukkan kedalam keranjang

# BucketEventListener

Berfungsi untuk memproses gagal atau berhasilnya proses pada keranjang

# Diagram

Diagram ada di direktori fresh fruit

# Logika

        Seller rifqi;

        public MainWindow()
        {
            InitializeComponent();

            Bucket keranjangBuah = new Bucket(2);
            BucketController bucketController = new BucketController(keranjangBuah, this);

            rifqi = new Seller("rifqi", bucketController);

            ListBoxBucket.ItemsSource = keranjangBuah.findAll();
        }
Melakukan Intance untuk rifqi untuk mengambil alih keranjang

        interface BucketEventListener
        {
            void onSucceed(string message);
            void onFailed(string message);
        }

Interface dari BucketEventListener yang fungsinya sudah disebutkan diatas

Untuk Class BucketController.cs berisi pendeklarasian proses-proses pada keranjang. Seperti penambahan, penghitungan item dan lain-lain. Juga termasuk secara private mengambil proses dari BucketEventListener.cs untuk menampilkan notifikasi pesan. interface.


