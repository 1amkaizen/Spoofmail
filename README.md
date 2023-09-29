# Spoofmail

### sebelum melakukan serangan kita harus tahu dulu email dari target kita.
**contoh :** misalkan disini saya ada target@gmail.com

**skenario :** pak presiden mengirim email ke pegawainya dan menyuruh untuk mereview aplikasi,yang dimana aplikasi itu adallah trojan.Di sini pegawai adalah target kita atau korbannya,dan presiden adalah kita yang menyamar agar si pegawai percaya bahwa emal itu dai presiden. 

# Persiapan
- Buat SMTP server
- install sendemail
- install Spoofmail

### buat smtp server
**untuk membuat SMTP server bisa di :**
- https://brevo.com
- https://mailjet.com
- https://microsoft.com
- dll

### Contoh SMTP server
  
  **Catatan :** disini saya menggunakan https://brevo.com.
 
- SMTP server  : smtp-relay.brevo.com
- Port : 587
- Login : myemail@gmail.com
- Password : mypassword

### Install sendemail
```
apt install sendemail
```
### Install Spoofmail
```
git clone https://github.com/1amkaizen/Spoofmail/
```
```
cd Spoofmail
```
### jalankan
```
./spoofmail
```

Kita akan di suruh memasukkan informasi berupa UserName, smtp server, dll
```
Username: 
Password: 
SMTP-Server:
Port:
Email Pengirim: 
Email Target: 
Subject:  
Pesan: 
Header:
TLS:
```

# Penjelasan

**Username:** Username yang di pakai mendaftar ke penyedia SMTP<br>
**Password:** password yang di pakai untuk login ke penyedia SMTP<br>
**SMTP-Server:** contohnya smtp.relay.brevo.com<br>
**Port :** port smtp server<br>
**Email Pengirim:** email yang di pakai untuk menyamar, contohnya presiden@gmail.com<br>
**Email Target:** email target atau korban yang akan di kirimkan email<br>
**Subject:**  Subject pesan<br>
**Pesan:** isi pesannya<br>
**Header:** header pesannya<br>
**TLS:** pilih yes/no


# Contoh
```
Username: myemail@gmail.com
Password: mypassword
SMTP-Server: smtp-relay.brevo.com
Port : 587
Email Pengirim: presiden@gmail.com
Email Target: target@gmail.com
Subject: Review Aplikasi
Pesan: Tolong review aplikasi ini: https.//aplikasi.com
Header: From <presiden@gmail.com>
TLS: yes
```

# Konfigurasi tambahan untuk TLS

### Install cpanm
```
sudo apt-get install cpanminus
```

### Install Net::SSLeay dan IO::Socket::SSL: 

```
sudo cpan install Net::SSLeay
```

```
sudo cpan install IO::Socket::SSL
```

Setelah menginstal modul Perl yang diperlukan, pastikan instalasi berhasil dengan menjalankan perintah-perintah berikut: 

```
perl -MNet::SSLeay -e 'print "$Net::SSLeay::VERSION\n"'
```

```
perl -MIO::Socket::SSL -e 'print "$IO::Socket::SSL::VERSION\n"'
```
**berhasil:**Jika versi berhasil dicetak, berarti instalasi berhasil. 

**Coba SendEmail Lagi:**
Setelah menginstal modul yang diperlukan, coba jalankan kembali SendEmail dan periksa apakah kesalahan masih terjadi.

Jika semua langkah di atas diikuti dengan benar dan modul Perl terinstal dengan sukses, seharusnya Anda dapat menggunakan SendEmail tanpa kesalahan terkait TLS.


