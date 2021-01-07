# Sublime Text - LaTeX
Kaynak : https://evgenii.com/blog/creating-pdf-from-latex-in-sublime-text-3

#### Elde edilecek Sonuç

- Sublime Text 3'e build komutu gönderildiğinde üzerinde çalışılan tex uzantılı dosyanız derlenip PDF formatına dönüştürülücektir.


#### Bu işleme başlamadan önce gereklilikler: 
- Bir LaTeX derleyicinizin kurulu olması gerekmektedir. 
- Bu örnekteki adımlar Ubuntu Ubuntu 16.04.5 LTS üzerinde uygulanmaktadır.
  - Ubuntu üzerinde latex kurulumu için aşağıdaki komut kullanılır:
  - ``` sudo apt-get install texlive-full ```

#### Kurulum
Yeni bir Build System oluşturulur.

1) Sublime Text 3 açılır
2) Tools > Build System menüsünden New Build System ... seçilir
3) Sublime Text üzerinde yeni bir dosya açılacaktır.
4) Aşağıda yer alan metin blok dosyanın içine yapıştırılır.
```bash	
{
    "shell": true,
    "cmd": ["/usr/bin/pdflatex $file && latexmk -c"],
    "selector": "text.tex.latex"
}
```
LaTeX metnini PDF'e dönüştürmek için gerekli compailer. :
```bash /usr/bin/pdflatex ```

Aşağıdaki komut PDF oluşturulurken derleyici tarafından oluşturulan gereksiz dosyaların temizlenmesini sağlar 
```bash latexmk -c ```

#####  5) Ardından dosya aşağıdaki isimle kaydedilir.
LaTeX.sublime-build

#### Dip Not
1) Sublime Text 3'te build işlemi yapmak için öntanımlı kısayol:
ctrl+b

2) Oluşturulan build system'i daha sonra tekrar düzenlemek isterseniz:  aşğıdaki dosyayı düzenleyebilirsiniz.
   - **LaTeX.sublime-build**
   - öntanımlı dizin : ~/.config/sublime-text-3/Packages/User