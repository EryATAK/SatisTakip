# EXCEL İLE SATIŞ TAKİP VE PRİM HESAPLAMA

> Bu proje; satış miktarına göre prim belirleyip, bu prim ile birlikte web üzerinden güncel kur verisi ile çalışanların maaş hesabını yapan excel tablolarını içermektedir

<p>Şampuan, parfüm ve deodorant ürünlerini satan örnek firmamızda 3 bölgede satış yapılmaktadır. Toplam 20 adet satış birimine bağlı personel bulunmaktadır ve bu personellerin 3 tanesi takım lideri olup aktif olarak satış yapmamakta, takımlarını yönetmektedirler.</p>
<p>Her personelin aylık sabit aldıkları maaş ve prim usulü ile çalışılmaktadır. Ödenecek olan miktar satışlardan gelen primlerin eklenmesi sonucu ortaya çıkar ve anlık dolar kuru üzerinden ödemeler gerçekleşmektedir. Ödemeler hangi banka kanalı aracılığı ile yapılacaksa kur ona göre hesaplanmaktadır.  </p>
<p>Prim hesabı, aylık toplam satış 150.000 ₺ üzerinde ise toplam prim 3.000<span>$</span>, altında ise 2.000$’dır. Bu primin %10’luk dilimi bireysel olarak en fazla satış yapan personele, %90’lık dilimi ise takım olarak en çok satış yapan takımın payı olarak ayrılmıştır. En çok satış yapan takım, aldığı %90’lık dilimi ise %30 Takım lideri payı, %70 takım personelleri payı olarak ayrılmıştır. Takımda kaç adet personel varsa %70’lik dilimi kendi arasında paylaşmaktadır.  </p>

## İÇERİK
![1](https://ogrencievi.net/uploads/eray/satistakipexceli/1.png)
<p>Personel Listesi Ekranı : Personellere ait; personel kimlik numaraları, İsim soyisim bilgileri, firma içindeki görevi, maaş bilgisi ve maaş ödemesinin yapılacağı IBAN bilgisi bu sayfada yer almaktadır.  </p>

![1](https://ogrencievi.net/uploads/eray/satistakipexceli/2.png)
<p>İş Dağılımı Ekranı: Personel No ID’sinden DÜŞEYARA() formülü ile isim soyisim bilgisi gelmektedir. Kişinin bağlı olduğu takım lideri, çalışma bölgesi ve görevi bu sayfada gösterilmektedir.  </p>

![1](https://ogrencievi.net/uploads/eray/satistakipexceli/3.png)
<p>Malzeme Listesi Ekranı: Aktif olarak satışı yapılan malzeme listesinin bulunduğu ekrandır. Malzemeye ait malzeme kodu, malzemenin adı ve satış fiyatı bilgisi bu sayfada bulunmaktadır.  </p>

![1](https://ogrencievi.net/uploads/eray/satistakipexceli/4.png)
<p>Satış Adetleri Ekranı: Yapılan satışların listelendiği sayfadır. Satışa ait; satış tarihi, Satışı yapan personelin ID’si, satışı yapan personelin isim soyisim bilgisi, bağlı olduğu takım lideri bilgisi, sattığı ürüne ait; malzeme kodu, malzeme adı, adet fiyatı, satış adeti bilgileri bulunmaktadır. Bu sayfaya SAP, ERP gibi sistemlerden çekilen veriler eklenebilir.  </p>

![1](https://ogrencievi.net/uploads/eray/satistakipexceli/5.png)
<p>Toplam Satışlar Ekranı: Malzeme bazında yapılan satışların toplamını gösteren pivot tabloyu ve satışları grafik ile gösteren sayfadır. Grafiğe bakıldığında hangi takım liderinin, hangi kodlu personelinin hangi malzeme de ivmelendiği gözlemlenebilmektedir.  </p>

![1](https://ogrencievi.net/uploads/eray/satistakipexceli/6.png)
<p>Prim Payları Ekranı: Toplam satışlar tablosunda oluşturulan pivot sayesinde Takım lideri odaklı ve satış personeli odaklı satış bilgilerinin bulunduğu sayfadır. Listede personellerin, satışlardan kazandığı toplam TL miktarları gösterilmektedir. Bu miktara göre yine aynı sayfada prim hesaplama algoritması çalışmaktadır. 
Yapılan satış miktarı, 150.000 ₺üzerinde ise toplam prim ücreti kısmı yazılan formül ile 3.000<span>$</span> , 150.000 ₺ altında ise 2.000$ olarak değişmektedir. Bu sayfada her bir değer birbirine formüller ile bağlıdır. Yapılan satış miktarlarına göre bireysel olarak en çok satış yapan personel bireysel satış primi “1” numaralı alanda, takım olarak en çok satış yapan takım ve takım liderine ait bilgiler ise “2” numaralı alanda gösterilmektedir. </p>

![1](https://ogrencievi.net/uploads/eray/satistakipexceli/7.png)
<p>Aylık Maaş Ekranı: “1” numaralı hücrede maaş ödemesinin yapılacağı banka kanallarının bulunduğu açılır pencere bulunmaktadır. Buradan ödeme yapılacak kanal seçildiğinde sayfada bulunan güncel kur sütunu yenilenmektedir. Güncel kur bilgisi Excel içerisinde gizli durumda bulunan “Güncel Kur Verisi” isimli sayfadan alınmaktadır ve “Güncel Kur Verisi” içerisinde bulunan veriler, https://finans.mynet.com/doviz/usd-dolar/ web sitesinden dakika başı güncellenecek şekilde alınmaktadır. Sayfada bulunan yenile butonu içerisinde tüm sayfaları yenileyecek olan kodlar yazılmıştır ve buton sayesinde her yeni veri girişi yapıldığında güncel kur bilgisi ve pivotlarda yapılması gereken yenileme işlemi gerçekleşmektedir.  </p>

![1](https://ogrencievi.net/uploads/eray/satistakipexceli/8.png)
<p>Maaş Belgesi Ekranı: “1” numaralı hücreden personel seçilerek Maaş Dökümü Getir butonu ile personel maaş dökümünün hazırlandığı sayfadır. İlgili satırda personel ismi bilgisi, tarih bilgisi, ödeme yapılan banka kanalı, ödenen ücret bilgileri Aylık Maaş sayfasından, IBAN bilgisi ise Personel Listesi sayfasından alınmaktadır.</p>

