---
title: Lehçe İntrastat
description: Bu makalede, Polonya'daki İntrastat raporlaması hakkında bilgiler yer almaktadır.
author: AdamTrukawka
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 473581fa4f3f1e8cac06d5748f28116e6615215e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281657"
---
# <a name="polish-intrastat"></a>Lehçe İntrastat

[!include[banner](../includes/banner.md)]

**İntrastat** sayfası, Avrupa Birliği (AB) ülkeleri arasındaki ticaret hakkında bilgi oluşturmak ve raporlamak için kullanılır. Lehçe İntrastat bildirimi, raporlama için mal ticareti hakkında bilgiler içerir.

Aşağıdaki alanlar, Lehçe İntrastat bildirimine dahil edilir. **RodzajTransportu** (taşıma modu) ve **KrajPochodzenia** (kaynak ülke veya bölge) hariç, gönderenlere dahil edilmemiş tüm alanlar ve varışlara dahil edilmeyen **IdKontrahenta** (müşterinin yabancı KDV numarası).

| Alan adı | Tanım |
|-------------------------|-------------------------|
| Deklaracja Verileri | Belgenin oluşturulduğu tarih. |
| Miesiac | Bildirimin referans ayı. |
| Rok | Bildirimin referans yılı. |
| Numer | Referans dönemindeki beyanname numarası. |
| Wersja | Beyannamenin versiyon numarası. |
| NrWlasny | Beyanname tanımlayıcısı. Değer otomatik olarak oluşturulur. |
| Typ | Rapor yönü.</br><li>Varışlar için, "P" yazdırılır.</li><li>Gönderilerde, "W" yazdırılır.</li> |
| Rodzaj | Beyanname türü. Değer, raporun orijinal bildirim mi yoksa düzeltme bildirimi mi olduğunu belirtir. |
| UC | İntrastat beyannamesinin adreslendiği birim kodu. Değer, **Yabancı ticaret parametreleri** sayfasının **Aracı** sekmesindeki **Satış vergisi** kısmında yer alan **Vergi muafiyet numarası** alanında belirtilir. |
| Nazwa | Şirketin adı. |
| Miejscowosc, UlicaNumer, KodPocztowy | Yasal varlığın tam adresi. |
| Nip | Lehçe vergi kimlik numarası (katma değerli vergi [KDV] kodu). |
| Regon | Lehçe istatistiksel kimlik numarası (kurumsal numara). |
| LacznaWartoscFaktur | Fatura değerlerinin toplamı. |
| LacznaWartoscStatystyczna | İstatistiksel değerlerinin toplamı. |
| LacznaLiczbaPozycji | Ürün maddelerinin toplam sayısı. |
| PozId | Belirli bir mal maddesinin ardışık numarası. |
| OpisTowaru | Emtianın ticari adı. |
| KrajPochodzeniaWysylki | Karşı taraftaki ülke veya bölgenin Uluslararası Standardizasyon Teşkilatı (ISO) kodu. |
| WarunkiDostawy | Teslimat koşullarının İntrastat kodu. |
| RodzajTransakcji | Hareketin yapısını gösteren kod. Polonyalı şirketler iki basamaklı işlem kodları kullanır. |
| KodTowarowy | Birleşik Terminolojisine göre sekiz basamaklı emtia kodu. |
| RodzajTransportu | Taşıma modunun İntrastat kodu. |
| KrajPochodzenia | Emtianın üretildiği veya oluşturulduğu ülkenin veya bölgenin ISO kodu. |
| MasaNetto | Kilogram cinsinden net kütle. |
| IloscUzupelniajacaJm | Tüm sayılarda, tamamlayıcı ölçü biriminde bulunan miktar. |
| WartoscFaktury | Bir maddeyle kaplanan tüm hareketlerin fatura değeri. |
| WartoscStatystyczna | İstatistiksel değer. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, E-posta | Bildirimi gönderen kişinin ilk ve son adları, telefon numarası, faks numarası ve e-posta adresi. |
| IdKontrahenta | Bir AB devlet üyesindeki müşterinin yabancı KDV numarası. |


## <a name="set-up-intrastat"></a>İntrastat'ı ayarlama

Global depodan aşağıdaki Elektronik raporlama (ER) yapılandırmalarının en güncel sürümlerini mevcut kuruluma aktarabilirsiniz.

   - Intrastat modeli
   - Intrastat raporu
   - Intrastat (PL)

Daha fazla bilgi için bkz. [Yapılandırma hizmeti Genel deposundan ER yapılandırmalarını indirme](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Şirketiniz için bir KDV kodu ve bir kuruluş numarası ayarlayın

### <a name="create-registration-types-for-company-codes"></a>Şirket kodları için kayıt türleri oluştur

Şirket kodları için iki kayıt türü oluşturmanız gerekir: bir adet KDV kodu (NIP kodu), diğeri ise kuruluş numarası için (Regon kodu).

1. **Organizasyon yönetimi** > **Genel adres defteri** > **Kayıt türleri** > **Kayıt türleri**'ne gidin.
2. Eylem bölmesinde, KDV kimliği için kayıt türü oluşturmak üzere **Yeni**'yi seçin.
3. **Kayıt türü ayrıntıları gir** iletişim kutusunda, **Ad** alanına yeni kayıt türü için bir ad girin. Örneğin, **NIP** girin.
4. **Ülke/bölge** alanında **POL**'yu seçin.
5. **Oluştur**'u seçin.
6. Eylem bölmesinde, şirket numarası için kayıt türü oluşturmak üzere **Yeni**'yi seçin.
7. **Kayıt türü ayrıntıları gir** iletişim kutusunda, **Ad** alanına yeni kayıt türü için bir ad girin. Örneğin, **Regon** yazın.
8. **Ülke/bölge** alanında **POL**'yu seçin.
9. **Oluştur**'u seçin.

### <a name="match-the-registration-types-with-registration-categories"></a>Kayıt türlerini kayıt kategorileriyle eşleştir

1. **Organizasyon yönetimi** > **Genel adres defteri** > **Kayıt türleri** > **Kayıt kategorileri**'ne gidin.
2. Eylem bölmesinde, oluşturduğunuz her kayıt türü ve bir kayıt kategorisi arasına bağlantı oluşturmak için **Yeni**'yi seçin.

    - KDV koduna ait kayıt türü (NIP kodu) için **KDV kodu** kayıt kategorisini seçin.
    - Şirket numarasına ait kayıt türü (Regon kodu) için **Şirket kodu (COID)** kayıt kategorisini seçin.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Şirketiniz için bir KDV kodu ve bir kuruluş numarası ayarlayın

1. **Kuruluş yönetimi** > **Kuruluşlar** > **Tüzel kişilikler**'e gidin.
2. Izgarada şirketinizi seçin.
3. Eylem Bölmesi'nde, **Kayıt Kimlikleri**'ni seçin.
4. **Kayıt Kimliği** hızlı sekmesinde **Ekle**'yi seçin.
5. **Kayıt türü** alanında, daha önce oluşturduğunuz kayıt türlerinden birini seçin.
6. Önceki adımda seçtiğiniz kayıt türüne bağlı olarak şirketinizin KDV kodunu (NIP kodu) veya kuruluş numarasını (Regon kodu) girin.
7. Daha önce oluşturduğunuz diğer kayıt türü için 4 ile 6 arasındaki adımları yineleyin.

## <a name="set-up-a-company-address"></a>Şirket adresini ayarlama

1. **Kuruluş yönetimi** > **Kuruluşlar** > **Tüzel kişilikler**'e gidin.
2. Izgarada şirketinizi seçin.
3. **Adresler** sekmesinde, **Düzenle**'yi seçin.
4. **Adresi düzenle** iletişim kutusunda, **ZIP/Posta kodu** alanında şirketinizin ZIP/posta kodunu seçin.
5. **Cadde** alanına adresinizi girin.
6. **Şehir** alanında, şehrinizi seçin.

## <a name="set-up-foreign-trade-parameters"></a>Dış ticaret parametreleri ayarla

1. **Vergi** > **Kurulum** > **Yabancı ticaret parametreleri**'ne gidin.
2. **İntrastat** sekmesindeki **Elektronik raporlama** hızlı sekmesinde **Dosya biçimi eşlemesi** alanında, **İntrastat (PL)** seçeneğini belirleyin.
3. **Rapor biçimi eşlemesi** alanında **İntrastat raporu**'nu seçin.
4. **Emtia kodu hiyerarşisi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.
5. **Hareket kodu** alanında mal transferleri için hareket kodunu seçin. Bu kodu, ücret (mali veya başka türlü) karşılığında fiili ya da planlı bir mal aktarımına neden olan hareketler için kullanırsınız. Düzeltmeler için de kullanırsınız. Polonya'daki şirketler iki basamaklı işlem kodları kullanır.
6. **Alacak dekontu** alanında malların iadesi için hareket kodunu seçin.
7. **Ülke/bölge özellikleri** sekmesinde, **Ülke/bölge** alanında, şirketinizin iş yaptığı tüm ülke veya bölgeleri listeleyin. AB üyesi olan her ülkenin İntrastat raporunuzda görüntülenmesi için her ülke için **Ülke/bölge türü** alanında **EU** seçeneğini belirleyin. Polonya için **Ülke/bölge türü** alanında, **Yurtiçi** seçeneğini belirleyin.
8. **Aracı** sekmesinde, **Aracı** hızlı sekmesinde, **Satış vergisi** bölümünde, **Vergi muafiyet numarası** alanına, İntrastat beyannamesinin ilgili olduğu birim kodunu belirtmek için **420000** girin.
9. **Sözleşme** sekmesinde bildirimi gönderen kişinin adını, telefon numarasını, faks numarasını ve e-posta adresini girin.
10. **Numara serileri** sekmesinde, **XML dosya numarası** referansı için **Numara serisi kodu** alanında, maksimum dokuz karaktere sahip, devamlı olmayan bir numara serisi belirtin. Bu alan, İntrastat raporundaki **Beyanname tanımlayıcı** alanı için otomatik olarak değer oluşturmak amacıyla kullanılır.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>İntrastat bildirimi için ürün parametrelerini ayarlayın

1. **Ürün bilgileri yönetimi** > **Ürünler** > **Serbest bırakılan ürünler**'e gidin.
2. Kılavuzda, bir ürün seçin.
3. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde **Emtia** alanında emtia kodunu seçin. Emtia adı, İntrastat raporundaki **Emtia açıklaması** alanına yazdırılır.
4. **Kaynak** bölümünde, **Ülke/bölge** alanında, ürünün ülkesini veya kaynak bölgesini seçin.
5. **Stok yönetimi** hızlı sekmesinde, **Net ağırlık** alanına ürünün ağırlığını kilogram olarak girin.

## <a name="set-up-compression-of-intrastat"></a>Intrastat sıkıştırmasını ayarla

-   **Vergi** > **Kurulum** > **Dış ticaret** > **İntrastat Sıkıştırması** seçeneğine gidin ve İntrastat bilgileri özetlendiğinde karşılaştırılacak alanları seçin. Lehçe İntrastat için aşağıdaki alanları seçin:

    - Emtia
    - Hareket kodu
    - Menşe ülkesi/bölgesi
    - Taşıma
    - Teslimat koşulları
    - Gönderenin ülkesi/bölgesi
    - Ülke/bölge
    - Düzeltme
    - Vergi muafiyet numarası
    - Yön
    - Fatura

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Taşıma yöntemini ve teslimat koşullarını ayarlayın

1.  Taşıma kodlarını ayarlayın.

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Taşıma yöntemi**'ne gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Taşıma** alanına benzersiz bir kod girin. Polonyalı şirketler bir basamaklı taşıma kodları kullanır.

2.  Teslimat şekli İntrastat kodları kurulumu.

    1. **Tedarik ve kaynak atama** > **Kurulum** > **Dağıtım** > **Teslimat koşulları**'na gidin.
    2. Kılavuzda teslimat koşulları kümesini seçin.
    3. **Genel** hızlı sekmesindeki **İntrastat kodu** alanında benzersiz kodu girin.

## <a name="intrastat-transfer"></a>İntrastat transferi

**İntrastat** sayfasında, Eylem Bölmesi'nde, satış siparişlerinizden, serbest metin faturalarınızdan, satın alma siparişlerinizden, satıcı faturalarınızdan, satıcı ürün girişlerinden, proje faturalarından ve transfer emirlerinizden topluluk içi ticaret hakkındaki bilgileri otomatik olarak aktarmak için **Transfer**'i seçebilirsiniz. Yalnızca varış ülkesi veya bölgesi veya konsinye olarak bir AB ülkesine sahip belgeler aktarılacaktır.

Eylem Bölmesi'nde **Yeni**'yi seçerek hareketleri el ile de girebilirsiniz.

### <a name="generate-an-intrastat-report"></a>İntrastat raporu oluşturma

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde **Çıktı** &gt; **Rapor**'u seçin.
3. **İntrastat Raporu** iletişim kutusunda aşağıdaki alanları ayarlayın.

    | Alan | Tanım |
    |-------------------------|-------------------------|
    | Başlangıç tarihi | Raporun başlangıç tarihini seçin. |
    | Dosya oluştur | İntrastat raporunuzda bir .xml dosyası oluşturmak için bu seçeneği **Evet** olarak ayarlayın. |
    | Dosya adı | .xml dosyasının adını girin. |
    | Rapor oluştur | İntrastat raporunuzda bir .xlsx dosyası oluşturmak için bu seçeneği **Evet** olarak ayarlayın. |
    | Rapor dosyası adı | .xlsx dosyasının adını girin. |
    | Yön | Topluluk içi gelenlerle ilgili bir rapor için **Gelenler**'i seçin.</br>Topluluk için gönderimler hakkında rapor için **Gönderimler**'i seçin. |
    | Beyanname tanımlayıcısı | Belge kodu otomatik olarak oluşturulur ve güncelleştirilebilir. |
    | Beyanname türü | Orijinal bir beyanname için **Beyanname** seçin.</br>Önceden varolan, daha önce gönderilen orijinal veya düzeltme bildirimini tümüyle değiştirmek için **Beyanname düzeltmesi – değiştirme** öğesini seçin. |
    | Belge oluşturma şehri | İntrastat beyannamesindeki **Miejscowosc** alanında yazdırılması gereken değeri girin. |
    | Belge oluşturulma tarihi | İntrastat beyannamesindeki **Deklaracja Verileri** alanında yazdırılması gereken değeri girin. |
    | Belge No | İntrastat beyannamesindeki **Numer** alanında yazdırılması gereken değeri girin. |
    | Belge sürümü | İntrastat beyannamesindeki **Wersja** alanında yazdırılması gereken değeri girin. |

4. **Tamam**'ı seçin ve oluşturulan raporları inceleyin.

## <a name="example"></a>Örnek

**DEMF** tüzel kişiliğini kullanarak bu örnekte, İntrastat için gelenlerin ve gönderimlerin deftere nasıl nakledileceğini gösterilmektedir.

### <a name="preliminary-setup"></a>Ön kurulum

Aşağıdaki ER yapılandırmalarının en son sürümünü içeri aktarın:

   - Intrastat modeli
   - Intrastat raporu
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Şirket adresini ayarlama

1. **Kuruluş yönetimi** > **Genel adres defteri** > **Adresler** > **Adres kurulumu**'na gidin.
2. **Şehir** sekmesinde, **Yeni**'yi seçin.
3. **Ülke/bölge** alanında **POL**'yu seçin.
4. **Şehir** alanına **Warsaw** yazın.
5. **ZIP/posta kodu** sekmesinde, **Yeni**'yi seçin.
6. **Ülke/bölge** alanında **POL**'yu seçin.
7. **Şehir** alanında, **Warsaw**'ı seçin.
8. **ZIP/ postal kodu** alanına **00-844** girin.
9. **Kuruluş yönetimi** > **Kuruluş** > **Tüzel kişilikler**'e gidin ve **DEMF** tüzel kişiliğini seçin.
10. **Adresler** hızlı sekmesinde, **Düzenle**'yi seçin.
11. **Ülke/bölge** alanında **POL**'yu seçin.
12. **ZIP/ postal kodu** alanında **31-111**'i seçin.
13. **Cadde** alanına **Statystyczna 22/1** girin.
14. **Şehir** alanında, **Warsaw**'ı seçin.
15. **Tamam**'ı seçin.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Şirketiniz için bir KDV kodu ve bir kuruluş numarası kodu ayarlayın

### <a name="create-registration-types-for-company-codes"></a>Şirket kodları için kayıt türleri oluştur

1. **Organizasyon yönetimi** > **Genel adres defteri** > **Kayıt türleri** > **Kayıt türleri**'ne gidin.
2. Eylem bölmesinde, KDV kimliği (NIP kodu) için kayıt türü oluşturmak üzere **Yeni**'yi seçin.
3. **Kayıt türü ayrıntılarını girin** iletişim kutusunda, **Ad** alanına **NIP** girin.
4. **Ülke/bölge** alanında **POL**'yu seçin.
5. **Oluştur**'u seçin.
6. Eylem bölmesinde, şirket numarası (Regon kodu) için kayıt türü oluşturmak üzere **Yeni**'yi seçin.
7. **Kayıt türü ayrıntılarını girin** iletişim kutusunda, **Ad** alanına **Regon** girin.
8. **Ülke/bölge** alanında **POL**'yu seçin.
9. **Oluştur**'u seçin.

### <a name="match-the-registration-types-with-registration-categories"></a>Kayıt türlerini kayıt kategorileriyle eşleştir

1. **Organizasyon yönetimi** > **Genel adres defteri** > **Kayıt türleri** > **Kayıt kategorileri**'ne gidin.
2. Eylem bölmesinde, oluşturduğunuz her kayıt türü ve bir kayıt kategorisi arasına bağlantı oluşturmak için **Yeni**'yi seçin.

    - **NIP** kayıt türü için **KDV kodu** kayıt kategorisini seçin.
    - **Regon** kayıt türü için **Şirket kodu (COID)** kayıt kategorisini seçin.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Şirketiniz için bir KDV kodu ve bir kuruluş numarası ayarlayın

1. **Kuruluş yönetimi** > **Kuruluşlar** > **Tüzel kişilikler**'e gidin.
2. Izgarada, **DEMF**'i seçin.
3. Eylem Bölmesi'nde, **Kayıt Kimlikleri**'ni seçin.
4. **Kayıt Kimliği** hızlı sekmesinde **Ekle**'yi seçin.
5. **Kayıt türü** alanında **NIP**'yi seçin.
6. **Kayıt numarası** alanına **1234567890** girin.
7. **Ekle**'yi seçin.
8. **Kayıt türü** alanında **Regon**'u seçin.
9. **Kayıt numarası** alanına **12345678901234** girin.

### <a name="set-up-a-number-sequence-code"></a>Numara sıra kodu belirleyin

1. **Kuruluş yönetimi** > **Numara serileri** > **Numara serileri**'ne tıklayın.
2. Eylem Bölmesinde **Sıra sayısı** sekmesindeki **Yeni** grubunda **Sıra sayısı**'nı seçin.
3. **Kimlik** hızlı sekmesinin **Numara serisi kodu** alanında **XML\_dosya** girin.
4. **Kapsam parametreleri** hızlı sekmesindeki **Kapsam** alanında, **Şirket** seçeneğini belirleyin.
5. **Şirket** alanında, **DEMF**'yi seçin.
6. **Segmentler** hızlı sekmesinde, **Alfa sayısal** segmenti için **Uzunluk** alanında **4** değerini girin.
7. **Genel** hızlı sekmesinde, **Kurulum** bölümünde, **Sürekli** seçeneğini **Hayır** olarak ayarlayın.
8. **Numara tahsisatı** bölümünde, **En büyük** alanında, **9999** girin.

### <a name="set-up-foreign-trade-parameters"></a>Dış ticaret parametreleri ayarla

1. **Vergi** > **Kurulum** > **Dış ticaret** > **Dış ticaret parametreleri**'ne gidin.
2. **İntrastat** sekmesindeki **Genel** hızlı sekmesinde **Hareket** **kodu** alanına **11**'i seçin.
3. **Elektronik raporlama** hızlı sekmesindeki **Dosya biçimi eşlemesi** alanında **İntrastat (PL)** seçeneğini belirleyin.
4. **Rapor biçimi eşlemesi** alanında, **İntrastat Raporu**'nu seçin.
5. **Emtia kodu hiyerarşisi** hızlı sekmesindeki **Kategori hiyerarşisi** alanını **İntrastat** olarak seçtiğinize emin olun.
6. **Ülke/bölge özellikleri** sekmesinde, **Yeni**'yi seçin.
7. **Taraf ülkesi/bölgesi** alanında **POL**'yı seçin. Ardından **Ülke/bölge türü** alanında, **Yurtiçi** seçeneğini belirleyin.
8. **Taraf ülkesi/bölgesi** alanında **DEU**'yı seçin. Ardından **Ülke/bölge türü** alanında **EU** seçeneğini belirleyin.
9. **Aracı** sekmesinde, **Aracı** hızlı sekmesinde **Satış vergisi** bölümünde, **Vergi muafiyet numarası** alanında **420000** girin.
10. **İletişim** sekmesinde, **Ad** alanına **Manish Chopra** girin.
11. **Telefon** alanına **425-555-5068** girin.
12. **Faks numarası** alanına **425-555-5049** girin.
13. **E-posta** alanına **manishc@contoso.com** girin.
14. **Numara serileri** sekmesinde, **XML dosya numarası** referansı için **Numara serisi kodu** alanında **XML\_dosya**'yı seçin.

### <a name="set-up-product-information"></a>Ürün bilgilerini ayarlama

1. **Ürün bilgi yönetimi** > **Ürünler** > **Piyasaya sürülmüş** **ürünler**'e gidin.
2. Izgarada, **D0001**'i seçin.
3. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde, **Emtia** alanında **100 200 30**'ü seçin.
4. **Stok yönetimi** hızlı sekmesindeki **Ağırlık ölçümleri** bölümünde **Net ağırlık** alanına **2** girin.
5. Eylem bölmesinde, **Kaydet**'i seçin.
6. Izgarada, **D0003**'i seçin.
7. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde, **Emtia** alanında **100 200 30**'ü seçin.
8. **Menşe** bölümündeki **Ülke/bölge** alanında, **DEU**'yu seçin.
9. **Stok yönetimi** hızlı sekmesindeki **Ağırlık ölçümleri** bölümünde **Net ağırlık** alanına **5** girin.
10. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="change-the-site-address"></a>Tesis adresini değiştirme

1. **Ambar yönetimi** > **Kurulum** > **Ambar** > **Tesisler**'e gidin.
2. Kılavuzda, **1**'i seçin.
3. **Adresler** hızlı sekmesinde, **Düzenle**'yi seçin.
4. **Adresi düzenle** iletişim kutusunda, **Ülke/bölge** alanında **POL**'yi seçin.
5. **Tamam**'ı seçin.

### <a name="set-up-a-transport-method"></a>Taşıma yöntemi ayarlayın

1. Taşıma yöntemi oluşturun.

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Taşıma yöntemi**'ne gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Taşıma** alanına, **3** yazın.
    4. **Açıklama** alanına, **Yol taşıması** girin.

2. Yeni taşıma yöntemini teslimat yöntemine atayın. Bu şekilde, karşılık gelen teslimat şekli seçildiğinde, taşıma yöntemi için kullanılan varsayılan değerleri ayarlarsınız.

    1. **Tedarik ve kaynak atama** > **Kurulum** > **Dağıtım** > **Teslimat modları**'na gidin.
    2. Kılavuzda, **10**'i seçin.
    3. **Dış ticaret** hızlı sekmesindeki **Taşıma** alanında **3**'i seçin.

3. Bir müşteri için varsayılan teslimat modunu seçin.

    1. **Alacak hesapları** > **Müşteriler** > **Tüm müşteriler**'e gidin.
    2. Kılavuzda, **DE-016**'yı seçin.
    3. **Fatura ve teslimat** hızlı sekmesindeki **Teslimat yöntemi** alanında **10**'u seçin.

4. Bir satıcı için varsayılan teslimat modunu seçin.

    1. **Borç hesapları** > **Satıcılar** > **Tüm satıcılar** seçeneğine gidin.
    2. Kılavuzda, **DE-001**'yı seçin.
    3. **Fatura ve teslimat** hızlı sekmesindeki **Teslimat yöntemi** alanında **10**'u seçin.

### <a name="set-up-codes-for-terms-of-delivery"></a>Teslimat koşulları kodlarını ayarlayın

1. Teslimat koşullarının İntrastat kodunu ayarlayın.

    1. **Tedarik ve kaynak atama** > **Kurulum** > **Dağıtım** > **Teslimat koşulları**'na gidin.
    2. Izgarada, **CIF**'i seçin.
    3. **Genel** hızlı sekmesindeki **İntrastat kodu** alanında **CIF**'yi seçin.

2. Bir müşteri için varsayılan teslimat koşullarını seçin.

    1. **Alacak hesapları** > **Müşteriler** > **Tüm müşteriler**'e gidin.
    2. Kılavuzda, **DE-016**'yı seçin.
    3. **Fatura ve teslimat** hızlı sekmesindeki **Teslimat koşulları** alanında **CIF**'yi seçin.

3. Bir satıcı için varsayılan teslimat koşullarını seçin.

    1. **Borç hesapları** > **Satıcılar** > **Tüm satıcılar** seçeneğine gidin.
    2. Kılavuzda, **DE-001**'yı seçin.
    3. **Fatura ve teslimat** hızlı sekmesindeki **Teslimat koşulları** alanında **CIF**'yi seçin.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>AB müşterisinin vergi muafiyeti numarası kodunu doğrulama

1. **Alacak hesapları** > **Müşteriler** > **Tüm müşteriler**'e gidin.
2. Kılavuzda, **DE-016**'yı seçin.
3. **Fatura ve teslimat** hızlı sekmesinde, **Satış vergisi** bölümünde, **Vergi muafiyet numarası** alanında **DE9012**'nin seçili olduğunu doğrulayın.

### <a name="create-a-sales-order-with-an-eu-customer"></a>AB müşterisiyle bir satış siparişi oluşturma

1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satış siparişi oluşturma** iletişim kutusunda, **Müşteri** hızlı sekmesindeki **Müşteri** bölümünde **Müşteri hesabı** alanında **DE-016**'yi seçin.
4. **Genel** hızlı sekmesinde **Depolama boyutları** bölümündeki **Site** alanında **1**'i seçin.
5. **Ambar** alanında **11**'i seçin.
6. **Adres** sekmesinde, Müşteri Almanya'dan olduğu için **Adres** alanının **Teichgasse 12, Kiel, 24103, DEU** olarak ayarlandığını doğrulayın.
7. **Tamam**'ı seçin.
8. **Başlık** sekmesinde, **Teslimat** hızlı sekmesinde, **Teslimat koşulları** alanının **CIF** olarak ayarlandığını ve **Teslimat modunun** **10** olarak ayarlandığını doğrulayın.
9. **Satırlar** sekmesindeki **Satış siparişi satırları** hızlı sekmesinde **Madde numarası** alanında **D0001**'i seçin. Ardından, **Miktar** alanına **8** yazın.
10. **Satır ayrıntıları** hızlı sekmesinde , **Dış ticaret** sekmesinde, **Hareket kodu** alanının **11** olarak ayarlandığını doğrulayın , **Emtia** alanı **100 200 30** olarak ayarlanır ve **Kaynak ülke/bölge** alanı da **POL** olarak ayarlanır.
11. Eylem bölmesinde, **Kaydet**'i seçin.
12. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
13. **Faturayı deftere naklet** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Parametre** bölümünde, **Miktar** alanında **Tümü**'nün öğesini seçin.
14. **Kurulum** hızlı sekmesindeki **Satış tarihi** alanında **10/18/2021**'i (18 Ekim 2021) seçin.
15. Faturayı deftere nakletmek için **Tamam**'ı seçin.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Hareketi İntrastat günlüğüne transfer etme ve sonucu inceleme

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
3. **İntrastat (Transfer)** iletişim kutusunda, **Parametreler** bölümünde, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
4. **Filtre**'yi seç.
5. **İntrastat Filtresi** iletişim kutusundaki **Aralık** sekmesinde ilk satırı seçin ve **Alan** alanının **Tarih** olarak ayarlandığından emin olun.
6. **Ölçüt** alanında geçerli tarihi seçin.
7. **İntrastat Filtresi** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
8. **İntrastat (Transfer)** iletişim kutusunu kapatmak için **Tamam**'ı seçin ve sonucu inceleyin. Satır, daha önce oluşturduğunuz satış siparişini temsil eder.

    ![intrastat sayfasındaki satış siparişini temsil eden satır](media/intrastat_pl_1.png)

9. Hareket satırını seçin ve ardından daha fazla ayrıntı görüntülemek için **Genel** sekmesini seçin.

    ![İntrastat sayfasının Genel sekmesindeki satış siparişi ayrıntıları](media/intrastat_pl_2.png)

10. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
11. **İntrastat Raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Tarih** bölümünde, **Başlangıç tarihi** alanında geçerli ayın ilk gününü seçin.
12. **Dışarı Aktarma** **seçenekleri** bölümünde, **Dosya oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Dosya adı** alanına gerekli adı girin.
13. **Rapor oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Rapor dosyası adı** alanına gerekli adı girin.
14. **Yön** alanında, **Gönderimler**'i seçin.
15. **Dosya biçimi eşleme** bölümünde, **Bildirim türü** alanının **Bildirim** olarak ayarlandığını doğrulayın.
16. **Belge oluşturma şehri** alanına, **Krakow** girin.
17. **Belge oluşturma tarihi** alanında, **10/19/2021** (19 Ekim 2021) öğesini seçin.
18. **Belge Numarası** alanına, **11** girin.
19. **Belge sürümü** alanına, **22** girin.
20. **Tamam**'ı seçin ve XML biçiminde oluşturulan raporu inceleyin. Aşağıdaki tabloda örnek raporlardaki değerler gösterilmektedir.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Alan adı</strong></p>
    </td>
    <td>
    <p><strong>Alan açıklaması</strong></p>
    </td>
    <td>
    <p><strong>Değer</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Belge hakkındaki bilgiler</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Verileri</p>
    </td>
    <td>
    <p>Belgenin oluşturulduğu tarih.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Belgenin oluşturulduğu şehir.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Toplam madde sayısı.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Toplam İstatistiksel değer.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Toplam fatura değeri.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Birim kodu.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Beyanname türü.</p>
    </td>
    <td>
    <p>B</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Belge sürümü.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Belge numarası.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Referans ayı.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Referans yılı.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>Rapor yönü.</p>
    </td>
    <td>
    <p>Ç</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>Beyanname tanımlayıcısı.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Şirketle ilgili bilgiler</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>Şirketin bulunduğu şehir.</p>
    </td>
    <td>
    <p>Varşova</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>Şirket Regon kodu.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Şirket NIP kodu.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Şirket ZIP/posta kodu.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Şirketin bulunduğu cadde.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Şirketin adı.</p>
    </td>
    <td>
    <p>Contoso Eğlence Sistemi Almanya</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Mal hakkında bilgiler</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>İstatistiksel değer.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Fatura değeri.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Net kütle.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>Müşterinin KDV numarası.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Emtia kodu.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Hareket kodu.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Teslimat modu koşulları.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Gönderme/hedef ülke veya bölge kodu.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Emtiaların bir açıklaması.</p>
    </td>
    <td>
    <p>Donanım</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Madde numarası.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>İletişim bilgileri</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-posta</p>
    </td>
    <td>
    <p>Gönderenin e-posta adresi.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Gönderenin faks numarası.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Gönderenin telefon numarası.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Gönderenin adı.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Excel biçiminde oluşturulan raporu inceleyin.

    ![Gönderimler için İntrastat raporu](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

1. **Borç hesapları** > **Satınalma siparişleri** > **Tüm satınalma siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satınalma siparişi oluştur** iletişim kutusundaki **Satıcı hesabı** alanında **DE-001**'i seçin.
4. **Tesis** alanında **1**'i seçin.
5. **Ambar** alanında **11**'i seçin.
6. **Tamam**'ı seçin.
7. **Başlık** sekmesinde, **Teslimat** hızlı sekmesinde, **Teslimat yöntemi** alanının **10** olarak ayarlandığını ve **Teslimat koşullarının** **CIF** olarak ayarlandığını doğrulayın.
8. **Satırlar** sekmesindeki **Satınalma siparişi satırları** hızlı sekmesinde **Madde numarası** alanında **D0003**'i seçin. Ardından, **Miktar** alanına **6** yazın.
9. **Satır ayrıntıları** hızlı sekmesinde , **Dış ticaret** sekmesinde, **Hareket kodu** alanının **11** olarak ayarlandığını ve **Taşıma** alanının **3** olarak ayarlandığını, **Emtia** alanı **100 200 30** olarak ve **Kaynak ülke/bölge alanı** da **DEU** olarak ayarlandığını doğrulayın.
10. Eylem Bölmesi'nde, **Satınalma** sekmesindeki **Eylemler** grubunda **Onayla**'yı seçin.
11. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
12. Eylem Bölmesinde, **Varsayılandan**'ı seçin ve **Satırlar için varsayılan miktar** alanında, **Sipariş miktarı**'nı seçin. Daha sonra **Tamam**'ı seçin.
13. **Satıcı Faturası başlığı** hızlı sekmesinde, **Fatura kimliği** bölümünde **Numara** alanına **00010** girin.
14. **Fatura tarihleri** bölümündeki **Fatura tarihi** alanında geçerli tarihi seçin. Bu tarih İntrastat transfer için kullanılır.
15. **Belge alma tarihi** alanında, **10/18/2021** (18 Ekim 2021) öğesini seçin.
16. Eylem Bölmesi'nde, faturayı deftere nakletmek için **Deftere Naklet**'i seçin.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Gelenler için bir İntrastat bildirimi oluşturma

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
3. **İntrastat (Transfer)** iletişim kutusunda, **Satıcı faturası** seçeneğini **Evet** olarak ayarlayın.
4. Hareketleri transfer etmek için **Tamam**'ı seçin ve ardından İntrastat günlüğünü inceleyin.

    ![İntrastat sayfasındaki satınalma siparişini temsil eden satır](media/intrastat_pl_4.png)

5. Satınalma siparişi için **Genel** sekmesindeki bilgileri gözden geçirin.

    ![İntrastat sayfasının Genel sekmesindeki satınalma siparişi ayrıntıları](media/intrastat_pl_5.png)

6. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
7. **İntrastat Raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Tarih** bölümünde, **Başlangıç tarihi** alanında geçerli ayın ilk gününü seçin.
8. **Dışarı Aktarma** **seçenekleri** bölümünde, **Dosya oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Dosya adı** alanına gerekli adı girin.
9. **Rapor oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Rapor dosyası adı** alanına gerekli adı girin.
10. **Yön** alanında **Gelenler**'i seçin.
11. **Dosya biçimi eşleme** bölümünde, **Bildirim türü** alanının **Bildirim** olarak ayarlandığını doğrulayın.
12. **Belge oluşturma şehri** alanına, **Krakow** girin.
13. **Belge oluşturma tarihi** alanında, **10/19/2021** (19 Ekim 2021) öğesini seçin.
14. **Belge Numarası** alanına, **11** girin.
15. **Belge sürümü** alanına, **22** girin.
16. **Tamam**'ı seçin ve XML biçiminde oluşturulan raporu inceleyin. Aşağıdaki tabloda örnek raporlardaki değerler gösterilmektedir.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Alan adı</strong></p>
    </td>
    <td>
    <p><strong>Alan açıklaması</strong></p>
    </td>
    <td>
    <p><strong>Değer</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Belge hakkındaki bilgiler</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Verileri</p>
    </td>
    <td>
    <p>Belgenin oluşturulduğu tarih.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Belgenin oluşturulduğu şehir.</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Toplam madde sayısı.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Toplam İstatistiksel değer.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Toplam fatura değeri.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Birim kodu.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Beyanname türü.</p>
    </td>
    <td>
    <p>B</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Belge sürümü.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Belge numarası.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Referans ayı.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Referans yılı.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>Rapor yönü.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>Beyanname tanımlayıcısı.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Şirketle ilgili bilgiler</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>Şirketin bulunduğu şehir.</p>
    </td>
    <td>
    <p>Varşova</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>Şirket Regon kodu.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Şirket NIP kodu.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Şirket ZIP/posta kodu.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Şirketin bulunduğu cadde.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Şirketin adı.</p>
    </td>
    <td>
    <p>Contoso Eğlence Sistemi Almanya</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Mal hakkında bilgiler</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>İstatistiksel değer.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Fatura değeri.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Net kütle.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>Kaynak ülke veya bölge kodu.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Taşıma modu kodu.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Emtia kodu.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Hareket kodu.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Teslimat modu koşulları.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Gönderme/hedef ülke veya bölge kodu.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Emtiaların bir açıklaması.</p>
    </td>
    <td>
    <p>Donanım</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Madde numarası.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>İletişim bilgileri</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-posta</p>
    </td>
    <td>
    <p>Gönderenin e-posta adresi.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Gönderenin faks numarası.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Gönderenin telefon numarası.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Gönderenin adı.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Excel biçiminde oluşturulan raporu inceleyin.

    ![İntrastat gelenler raporu](media/intrastat_pl_6.png)
