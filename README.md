##laravel-Fpdf-barcode

Fork of https://github.com/anouarabdsslm/laravel-fpdf, with barcode and QR generation capabilities.

###Usage

```php
$fpdf = new FpdfBarcode();
$fpdf->AddPage();

// Code 128 horizontal
// $x, $y, $code, $width, $height, $vertical
$fpdf->code128(15, 15, 'HORIZONTAL CODE', 85, 10, false);

// Code 128 vertical
// $x, $y, $code, $width, $height, $vertical
$fpdf->code128(150, 15, 'VERTICAL CODE', 85, 10, true);

// QR
// $code, $x, $y, $size
$fpdf->QR('QR CODE', 15, 50, 20);

$fpdf->Output();
```
