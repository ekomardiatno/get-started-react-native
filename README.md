### Cara Install React Native

#### Install Depecencies
1. Install **[NodeJS LTS](https://nodejs.org/en/download/)** terbaru.
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

#### Install React Native CLI
- Jalankan perintah berikut di CMD **`npm i -g react-native-cli`** untuk menginstall React Native CLI pada komputer anda

#### Memulai project baru React Native
1. Buka **CMD**, lalu arahkan ke folder yang digunakan untuk menyimpan project anda.
2. Jalankan perintah pada CMD `react-native init my-project`.
  ***Note:** "my-project" pada skrip adalah untuk penamaan project anda*
3. Setelah itu `cd my-project` untuk masuk ke folder project anda
3. Jalankan perintah pada CMD `react-native start` untuk mengaktifkan server react native.
4. `react-native run-android` untuk menjalankan aplikasi di perangkat Android atau Emulator Android

