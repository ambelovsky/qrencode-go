QR Encoder
==========

A QR-Code encoder written in GoLang and licensed under the LGPL v3.


Installation
============

```
sudo go get github.com/ambelovsky/qrencode-go/qrencode
sudo go install github.com/ambelovsky/qrencode-go/qrencode
```


Usage
=====

```
import "github.com/ambelovsky/qrencode-go/qrencode"

func Example() {
	grid, err := Encode("Testing one two three four five six seven eight nine ten eleven twelve thirteen fourteen fifteen sixteen seventeen eighteen nineteen twenty.", ECLevelQ)
	if err != nil {
		return
	}
	f, err := os.Create("/tmp/qr.png")
	if err != nil {
		return
	}
	defer f.Close()
	png.Encode(f, grid.Image(8))
}
```