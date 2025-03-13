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

## MessageBox Buton Kontrolleri
```
DialogResult cevap = MessageBox.Show("İşlem Yapılsınmı","Uygulama",MessageBoxButtons.YesNo,MessageBoxIcon.Question);
if(cevap == DialogResult.Yes){
	//Yapılacak İşlem
}
else if (cevap== DialogResult.No){
	//İşlemin İptal Durumu
}
```

## Dizi Oluşturma
```
string[] yazilar = new string[x]; // x = dizi uzunluğu
string[,] yazilar2 = new string[x,y]; // x = dizi uzunluğu, y = satır adeti

int[] double = new int[x]; // x = dizi uzunluğu
int[,] double2 = new int[x,y]; // x = dizi uzunluğu, y = satır adeti
```

## Sayıya Dönüştürme
```
Convert.ToInt32(<Dönüşücek Değer>); 
int.Parse(<Dönüşücek Değer>);
```

## Yazıya Dönüştürme
```
<Dönüşücek Değer>.ToString();
```
