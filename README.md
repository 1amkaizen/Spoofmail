# Spoofmail

# sebelum melakukan serangan kita harus tahu dulu email dari target kita.
# misalkan disini saya ada target@gmail.com

# skenario
### pak presiden mengirim email ke pegawainya dan menyuruh untuk mereview aplikasi,yang dimana aplikasi itu adallah trojan
### di sini pegawai adalah target kita atau korbannya,dan presiden adalah kita yang menyamar agar si pegawai percaya bahwa emal itu dai presiden

### - email pengirim
**catatan :** Target akan menerima email dari email ini. 

presiden@gmail.com

### - email penerima / target
target@gmail.com


# buat smtp server
### untuk membuat SMTP server bisa di
- https://brevo.com
- https://mailjet.com
- https://microsoft.com
- dll

# Contoh SMTP server
  
  **Catatan :** disini saya menggunakan https://brevo.com.
 
- SMTP server  : smtp-relay.brevo.com
- Port : 587
- Login : myemail@gmail.com
- Password : mypassword


### Install
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
'''
Username: myemail@gmail.com
Password: mypassword                                                           
SMTP-Server: smtp-relay.brevo.co.                                                        
Email Pengirim: presiden@gmail.com
Email Target: target@gmail.com                                                       
Subject: Review Aplikasi                                                            
Pesan: Tolong review aplikasi ini: https.//aplikasi.com
Header: From <presiden@gmail.com>
''
