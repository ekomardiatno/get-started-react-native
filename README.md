### Cara Install dan Jalankan Aplikasi React Native di Nox Player (Windows)
#### Install Depecencies
1. Install **[NodeJS LTS](https://nodejs.org/en/download/)** terbaru
  ***Note:** Jalankan perintah `node -v` di CMD untuk mengetahui nodejs telah terinstall di komputer anda.*
2. Install **Chocolatey**
    - Buka **CMD** sebagai administrator
    - Masukan perintah dibawah ini untuk menginstall Chocolatey
      ```shell
      @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
      ```
3. Install **Python2**, **JDK**
    - Buka **CMD** sebagai administrator
    - Masukan perintah dibawah ini untuk menginstall Phyton2 dan JDK
      ```shell
      choco install -y python2 jdk8
      ```
4. Install **Android SDK Manager**
    - Pastikan pilih **Install just for user**
    - Jangan lupa salin path di bagian **Destination Folder** pada halaman **Choose Install Location** untuk **Konfigurasi ANDROID_HOME**

#### Install React Native CLI
- Jalankan perintah berikut di CMD **`npm i -g react-native-cli`** untuk menginstall React Native CLI pada komputer anda

#### Konfigurasi ANDROID_HOME
1. Buka **Control Panel**, pilih **System and Security** kemudian **System**
2. Pada halaman System, pilih **Advanced system settings** yang berada di bagian samping halaman
3. Setelah muncul jendela **System Properties**, pastikan telah berada pada tab **Advanced** lalu klik tombol **Environment Variables...**
4. Pada jendela **Environment Variables** klik tombol **New...** di bagian **User variables**
5. Masukan `ANDROID_HOME` pada **Variable name**, kemudian masukan hasil salinan saat install Android SDK tadi ke **Variable value** contohnya bisa dilihat dibawah ini:
    ```
    C:\Users\[YOUR_USERNAME]\AppData\Local\Android\android-sdk
    ```
6. Terakhir klik **OK**

#### Install packages yang diperlukan di Android SDK Manager
- Buka aplikasi **SDK Manager** pada folder yang sama dengan path untuk konfigurasi ANDROID_HOME sebelumnya atau cari melalui **Start Menu**
- Pada list **Tools** install/update package berikut:
  - Android SDK Tools
  - Android SDK Platform-tools
  - Android SDK Build-tools
    *Untuk build-tools pilih saja versi package yang sama dengan platform-tools.*
- Pada list **Extras** (list paling bawah) install/update package berikut:
  - Google USB Driver
- Sedangkan untuk install Android API, install sesuai kebutuhan. Misalnya ingin menginstall Android 9/Pie. Pilih dan buka list **Android 9 (API 28)** kemudian centang **SDK Platform**.
  ***Note:** Centang package **Google APIs** jika tersedia dalam list*
  ***Saran:** Install Android API sesuai perangkat atau emulator yang anda miliki.*
- Kemudian tekan tombol **Install** di samping kanan bawah
- Terakhir pada jendela **Choose Packages to Install** klik **Accept License** lalu tekan Install

#### Memulai project baru React Native
1. Buka **CMD**, lalu arahkan ke folder untuk menyimpan folder anda.
2. Jalankan perintah pada CMD `react-native init my-project`
  ***Note:** "my-project" pada skrip adalah untuk penamaan project anda*
3. Setelah itu `cd my-project` untuk masuk ke folder project anda
3. Jalankan perintah pada CMD `react-native start` untuk mengaktifkan server react native.
4. `react-native run-android` untuk menjalankan aplikasi di perangkat Android atau Emulator Android

#### Konfigurasi Nox App Player
1. Buka aplikasi **Nox App Player**
2. Tekan tombol Pengaturan berlogo *gear* pada bar diatas aplikasi.
3. Pilih tab **Advanced settings**, lalu pada **Resolustion settings** ganti ke **Mobile phone**, kemudian tekan **Save settings**.
4. Terakhir restart Nox App Player
5. Setelah kembali ke aplikasi Nox App Player, buka aplikasi **Settings**.
6. Buka menu **About tablet** di menu paling bawah.
7. Kemudian tekan 7x pada **Build number** untuk mengaktifkan mode Developer.
8. Setelah itu kembali, buka menu **Developer Options** dan aktifkan **USB Debugging**
