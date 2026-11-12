# Gold Radar XAUUSD

Dashboard analisis teknikal XAU/USD statis berbasis browser.

## Sumber data

- Quote spot: [XAUS XAU/USD API](https://xaus.com/api/v1/spot?compact=1). Aplikasi membaca timestamp dan status data (fresh/stale/unavailable).
- OHLC historis: [XAUS chart API](https://xaus.com/api/v1/chart?symbol=xau&range=5d&interval=5m), yang menurut dokumentasinya memakai proxy Yahoo Finance.
- Timeframe M5, M15, dan H1 diambil dari feed OHLC; H4 diagregasi dari H1.
- Quote spot dan OHLC chart dapat memiliki perbedaan serta tidak sama dengan kuotasi broker. Aplikasi mengunci sinyal saat quote tidak fresh atau harga spot terlalu jauh dari candle chart.

## Aktifkan GitHub Pages

Satu langkah manual diperlukan karena koneksi GitHub yang dipakai untuk mengunggah file tidak memiliki izin administrasi Pages:

1. Buka **Settings → Pages** pada repository.
2. Pada **Build and deployment → Source**, pilih **GitHub Actions**.
3. Workflow deploy akan berjalan saat ada push ke branch `main`. Jika tidak otomatis, buka tab **Actions** dan jalankan workflow **Deploy Gold Radar**.

Setelah sukses, halaman dapat diakses di:
https://sw6623649-blip.github.io/gold-radar-xauusd/

## Analisis

EMA20/50, RSI14, ATR14, swing 20 candle, breakout, pullback EMA20, dan konfirmasi arah H1/H4. Entry/SL/TP hanya ditampilkan untuk kondisi yang memenuhi filter; area pemantauan ditandai sebagai pantauan, bukan sinyal entry.

## Catatan risiko

Ini alat bantu analisis teknikal, bukan sinyal pasti atau jaminan profit. Periksa harga, spread, slippage, dan ukuran posisi pada platform broker sebelum mengambil keputusan.
