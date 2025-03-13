# NTP Notları
## Dosya Kaydetme
```
SaveFileDialog sfd = new saveFileDialog();
sfd.Filter = " Yazı Dosyası | *.txt | Tüm Dosyalar |*.*";
DialogResult cevap = sfd.ShowDialog();
if(cevap == DialogResult.OK){
	txtEditor.SaveFile(sfd.FileName, RichTextBoxStreamType.PlainText);
}
```

## Dosya Açma
```
OpenFileDialog ofd = new OpenFileDialog();
ofd.Filter = "Yazı Dosyaları | *.txt";
DialogResult cevap = ofd.ShowDialog();
if (cevap == DialogResult.OK){
    txtEditor.LoadFile(ofd.FileName, RichTextBoxStreamType.PlainText);
}
```

## Dosya Yazdırma
- Click Fonksiyonu
```
PrintDialog pd = new PrintDialog();
DialogResult cevap = pd.ShowDialog();
if (cevap == DialogResult.OK){
    belge.Print();
}
```

- PrintPage Fonksiyonu - Toolbox:PrintDocument->PrintPage
```
e.Graphics.DrawString(txtEditor.Text, txtEditor.Font, Brushes.Black, new Point(100,100));
```

## Font Seçme
```
FontDialog fd = new FontDialog();
if(fd.ShowDialog() == DialogResult.OK){
	txtEditor.Font = fd.Font;
}
```

## Seçilen Yerin Fontunu Seçme
```
FontDialog fd = new FontDialog();
if(fd.ShowDialog() == DialogResult.OK){
	txtEditor.SelectionFont = fd.Font;
}
```

## Seçilen Yerin Rengini Seçme
```
ColorDialog cd = new ColorDialog();
if(cd.ShowDialog() == DialogResult.OK){
	txtEditor.SelectionColor = cd.Font;
}
```
