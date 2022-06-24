---
title: Norveç için yazar kasa işlevi
description: Bu makale, Microsoft Dynamics 365 Commerce'ta Norveç için kullanılabilir olan yazar kasa işlevine genel bir bakış sağlar ve işlevin ayarlanmasına yönelik yönergeler sunar.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 778a947f03866518219e9c0fa44660d66f19f53a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906711"
---
# <a name="cash-register-functionality-for-norway"></a>Norveç için yazar kasa işlevi

[!include[banner](../includes/banner.md)]

Bu makale, Dynamics 365 Commerce'ta Norveç için kullanılabilir olan yazar kasa işlevine genel bir bakış sağlar. Ayrıca bu işlevin ayarlanmasına yönelik yönergeler sunar. İşlev aşağıdaki bölümlerden oluşur:

- Tüm ülke veya bölgelerdeki müşteriler tarafından kullanılabilen ortak satış noktası (POS) özellikleri. Örnekler arasında, bir makbuz kopyasının birden fazla kez yazdırılmasını engellemenizi sağlayan bir seçenek bulunur.
- Satış hareketlerine yönelik dijital imzalar gibi, Norveç'e özgü özellikler.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Norveç için yazar kasa işlevine genel bakış

### <a name="common-pos-features"></a>Ortak POS özellikleri

Tüm ülke ve bölgelerdeki müşteriler tarafından kullanılabilen POS özellikleri hakkında bilgi edinmek için bkz. [Dynamics 365 Retail yardım kaynakları](../index.md).

Daha önce uygulamaya konan ve tüm ülke veya bölgelerdeki müşteriler tarafından kullanılabilen aşağıdaki POS yerelleştirme özellikleri artık özellikle Norveç için kullanılabilir:

- **Makbuza büyük yazı tipi boyutunda metin alanları yazdırma.** Makbuz biçimindeki bir alanda büyük yazı tipi boyutu kullanılması gerektiğini belirtmek için makbuz biçimi tasarımcısındaki **Yazı tipi boyutu** parametresini kullanabilirsiniz. (Büyük yazı tipi boyutu, her zamanki yazı tipi boyutunun yaklaşık iki katıdır.) Örneğin, bir makbuz kopyasına büyük karakterlerle "Kopya" göstergesi yazdırmak için bu parametreyi kullanabilirsiniz.
- **POS denetimi olay günlüğünde yazdırılan makbuz kopyalarını kaydetme.** Makbuz kopyalarının yazdırılmasını ve diğer POS denetim olaylarının kaydedilmesini etkinleştirmek için POS işlevi profilindeki **Denetim** parametresini kullanabilirsiniz. Denetim olayları kanal veritabanına ve Headquarters'a kaydedilir. Denetim olaylarını, **Denetim olayları** sayfasında görüntüleyebilirsiniz.
- **Makbuz kopyasının birden fazla kez yazdırılmasını engelleme.** POS işlevi profilindeki **Denetim** parametresi etkinleştirildiğinde **Makbuz kopyalarının yazdırılmasına izin ver** POS izni, makbuz kopyalarının yazdırılıp yazdırılmayacağını denetler. Ayrıca, bir makbuz kopyasının birden fazla kez yazdırılmasını engellemenizi sağlayan bir seçenek de bulunur.

Ek olarak, aşağıdaki POS özelliği Norveç için uygulamaya konmuş ancak tüm ülke veya bölgelerdeki müşteriler tarafından kullanılabilir hale getirilmiştir:

- **POS denetimi olay günlüğüne ek olayları kaydetme.** POS işlevi profilindeki **Denetim** parametresi etkinleştirilirse aşağıdaki olaylar POS denetimi olay günlüğüne kaydedilir:

    - Fiyat denetimleri
    - Vergi geçersiz kılmaları
    - Satır miktarlarında düzeltmeler
    - Kanal veritabanındaki hareketleri temizleme

### <a name="norway-specific-pos-features"></a>Norveç'e özgü POS özellikleri

Aşağıdaki Norveç'e özgü POS özellikleri, POS işlevi profilindeki **ISO kodu** parametresi **Hayır** olarak ayarlandığında etkin hale gelir.

#### <a name="digital-signing-of-sales-transactions"></a>Satış hareketlerinin dijital olarak imzalanması

Her satış hareketi dijital olarak imzalanır. İmza, hareketin sonlandırıldığı zamanda oluşturulur ve POS hareket günlüğüne kaydedilir. İmza, denetleme amaçlarıyla dışa aktarılan günlükte de kullanılabilir.

Yalnızca nakit satışı hareketleri imzalanır. İmzalama işleminin dışında bırakılan bazı hareket örnekleri aşağıda verilmiştir:

- Ön ödemeler (müşteri hesabı havalesi)
- Satış siparişlerine yönelik ön ödemeler (müşteri siparişi havalesi)
- Hediye kartı verme
- Satış dışı hareketler (kasa devri girişi, ödeme kaldırma vb.)

İmzalanmış veriler, aşağıdaki veri alanlarından oluşan bir metin dizesidir. Veri alanları noktalı virgüllerle ayrılır.

1. Aynı POS'a ait önceki imza (İlk hareket için \[**0**\] kullanılır.)
2. Hareket tarihi
3. Hareket saati
4. Sıralı imzalı hareket numarası
5. Vergi dahil hareket tutarı
6. Vergi hariç hareket tutarı

Dijital imzalama işlemi, SHA-1 karma işlevine sahip RSA 1024-bit anahtarını (RSA-SHA1-1024) kullanır. Commerce Scale Unit'e yüklenen bir sertifika, imzalama için kullanılır. Sertifikanın benzersiz tanımlayıcısı (ayak izi) imzayla birlikte kaydedilir.

İmza, mağaza verileriyle birlikte mağaza veritabanında ve Headquarters (HQ) veritabanında depolanır. **Mağaza hareketleri** sayfasının **Mali hareketler** hızlı sekmesinde, hareket imzasını ve imzayı oluşturmak için kullanılan hareket verilerini görüntüleyebilirsiniz.

#### <a name="receipts"></a>Makbuzlar

Norveç makbuzlarında, özel alanlar kullanılarak uygulanan ek bilgiler bulunabilir:

- **Makbuz başlığı** – Makbuz türünü tanımlamak için makbuz biçimi düzenine bir alan ekleyebilirsiniz. Örneğin, bir satış makbuzu "Satış makbuzu" metnini içerecektir.
- **İmzalı hareket sıra numarası** – Yazdırılmış bir makbuzu veritabanındaki dijital bir imzayla ilişkilendirmek için, imzalanmış bir hareketin sıralı numarası makbuz üzerinde görünebilir.
- **Makbuz toplamları** -Makbuz toplamlarına ait özel alanlarda, satış dışı tutarlar toplam hareket tutarlarından hariç tutulur. Satış dışı tutarlar aşağıdaki işlemlere ait tutarları içerir:

    - Ön ödemeler (müşteri hesabı havalesi)
    - Satış siparişlerine yönelik ön ödemeler (müşteri siparişi havalesi)
    - Hediye kartı verme
    - Hediye kartına para ekleme

#### <a name="x-and-z-reports"></a>X ve Z raporları

X ve Z raporlarında bulunan bilgiler Norveç'tek, gereksinimleri temel alır. Örneğin, **Toplam nakit satışı** tutarları yalnızca nakit satış hareketlerine ait tutarları içerir ve hediye kartı verme ile ön ödemeleri hariç tutar. Toplam nakit satışlar da her madde grubu ve ödeme yöntemi başına listelenir. Ayrıca, kümülatif **Genel toplam satış** ve **Genel toplam iade** tutarları saklanır ve yazdırılır.

#### <a name="saf-t-cash-register-audit-file"></a>SAF-T Yazar Kasa denetim dosyası

POS hareket günlüğünü önceden tanımlanmış Standart Denetim Dosyası - Vergi (SAF-T) Yazar Kasa biçiminde dışa aktarabilirsiniz. Denetim dosyası; kuruluş hakkındaki bilgiler, ilgili ana veriler (madde grupları, maddeler ve vergi kodları gibi) ve nakit satış hareketi verilerinin yanı sıra, bu hareketlere ait imzaları, satış dışı olay verilerini ve tarih sonu raporu verilerini içerir.

Denetim dosyası aşağıdaki senaryolar için dışa aktarılabilir:

- Mağaza başına
- Tüm mağazalar
- Terminal başına
- Tüm terminaller

Ayrıca, bir tüzel kişilikten başka bir tüzel kişilik adına rapor gönderebilirsiniz. Bu durumda, dışa aktarmayı işlem yapan tüzel kişilikten çalıştırmanız ve raporlayan tüzel kişiliği raporun göndericisi olarak belirtmeniz gerekir.

SAF-T Yazar Kasa biçimi, [Elektronik raporlama](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) kullanılarak Headquarters'da uygulanır. 

## <a name="setting-up-commerce-for-norway"></a>Norveç için Commerce'ı ayarlama

Bu bölümde, Norveç'e özel veya Norveç için önerilen Commerce ayarları açıklanmaktadır. Daha fazla bilgi için [Dynamics 365 Retail yardım kaynaklarına](../index.md) bakın.

Norveç'e özel işlevleri kullanmak için aşağıdaki görevleri tamamlamanız gerekir:

- Tüzel kişiliğin birincil adresinde, **Ülke/bölge** alanını **NOR** (Norveç) olarak ayarlayın.
- Norveç'te bulunan her mağazanın POS işlevi profilinde, **ISO kodu** alanını **NO** (Norveç) olarak ayarlayın.

Norveç için aşağıdaki ayarları da belirtmeniz gerekir.

### <a name="set-up-the-legal-entity"></a>Tüzel kişiliği ayarlama

Tüzel kişilik adının belirtildiğinden emin olun. Bu ad X ve Z raporlarına yazdırılacaktır.

Ayrıca **Banka hesabı bilgileri** hızlı sekmesinde, **Yönlendirme numarası** alanında kuruluş numarasını belirtin.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Norveç'teki gereksinimler uyarınca katma değer vergisini (KDV) ayarlama


Satış vergisi kodları, satış vergisi grupları ve madde satış vergisi grupları oluşturmanız gerekir. Ayrıca, ürün ve hizmetlerle ilgili satış vergisi bilgilerini de ayarlamanız gerekir. Satış vergisinin nasıl ayarlanacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Satış vergisine genel bakış](../../finance/general-ledger/indirect-taxes-overview.md).

Norveç'te bulunan mağazalar için satış vergisi grupları belirtmeniz ve **Fiyatlara satış vergisi dahildir** seçeneğini etkinleştirmeniz de gerekir.

### <a name="set-up-functionality-profiles"></a>İşlev profillerini ayarlama

Denetimi etkinleştirmeniz ve makbuz numaralandırmasını ayarlamanız gerekir.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Mağaza çalışanları için POS izin gruplarını ve bireysel izin ayarlarını güncelleştirme

**Makbuz kopyasını yazdırmaya izin ver** iznini uygun bir değere ayarlayın:

- **Her zaman izin ver** – Operatör makbuzun kopyasını birden çok kez yazdırabilir.
- **Yalnızca bir kez izin ver** – Operatör makbuzun kopyasını yalnızca bir kez yazdırabilir.
- **Yalnızca bir kez ve sadece HQ DB mevcutsa izin ver** – Operatör, makbuzun kopyasını yalnızca bir kez ve sadece Commerce Data Exchange: Real-time Service üzerinden HQ veritabanına erişilebiliyorsa yazdırabilir; böylece sistem, makbuz kopyalarının herhangi bir mağazada daha önce yazdırılmadığını doğrulayabilir.
- **Hiçbir zaman** – Operatör makbuzun kopyasını yazdıramaz.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Özel alanları, satış makbuzlarına yönelik makbuz biçimlerinde kullanılabilecek şekilde yapılandırma

**Dil metni** sayfasında, makbuz düzenlerine yönelik özel alanların etiketlerine aşağıdaki kayıtları ekleyin. Tabloda gösterilen **Dil Kodu**, **Metin Kodu** ve **Metin** değerlerinin yalnızca örnek olduğunu unutmayın. Bunları gereksinimlerinizi karşılayacak şekilde değiştirebilirsiniz.

| Dil kodu | Metin                   | Metin Kodu |
|-------------|------------------------|---------|
| tr-TR       | Makbuz başlığı          | 900011  |
| tr-TR       | Hediye kartıdır           | 900012  |
| tr-TR       | Toplam (satış)          | 900013  |
| tr-TR       | Toplam vergi (satış)      | 900014  |
| tr-TR       | Vergiyle birlikte toplam (satış) | 900015  |
| tr-TR       | Vergi tutarı (satış)     | 900016  |
| tr-TR       | Nakit hareketi kodu    | 900017  |

**Özel alanlar** sayfasında, makbuz düzenlerine yönelik özel alanlara aşağıdaki kayıtları ekleyin. **Açıklamalı alt yazı metni kodu** değerlerinin, **Dil metni** sayfasında belirttiğiniz **Metin Kodu** değerlerine karşılık gelmesi gerektiğini unutmayın.

| Ad                            | Tür    | Altyazı metni kodu |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | Giriş | 900011          |
| IsGiftCard                      | Giriş | 900012          |
| SalesTotalExt                   | Giriş | 900013          |
| TaxTotalExt                     | Giriş | 900014          |
| TotalWithTaxExt                 | Giriş | 900015          |
| AmountPerTaxExt                 | Giriş | 900016          |
| CashTransactionSequentialNumber | Giriş | 900017          |

> [!NOTE]
> Yukarıdaki tabloda listelendiği gibi, doğru özel alan adlarını belirtmeniz önemlidir. Yanlış bir özel alan adı, makbuzlardaki verilerin eksik olmasına neden olur.

### <a name="configure-receipt-formats"></a>Makbuz biçimlerini yapılandırma

Gerekli tüm makbuz biçimleri için **Yazdırma davranışı** alanının değerini **Her zaman yazdır** olarak değiştirin.

Makbuz biçimi tasarımcısında, aşağıdaki özel alanları ilgili makbuz bölümlerine ekleyin. Alan adlarının önceki bölümde tanımladığınız dil metinlerine karşılık geldiğini unutmayın.

1. Üst bilgi:

    - **Makbuz başlığı** – Bu alan, makbuz türünü tanımlar.
    - **Nakit hareketi kodu** – Bu alan, imzalanan nakit hareketinin sıralı numarasını yazdırır.

2. Satırlar:

    - **Hediye kartıdır** – Bu alan, hediye kartı verme veya hediye kartına ekleme işlemiyle ilişkili olarak makbuz satırını işaretler.

3. Alt bilgi:

    - **Toplam (satış)** – Bu alan, makbuzun toplam nakit satışı tutarını yazdırır. Tutara vergi dahil değildir. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.
    - **Toplam vergi (satış)** – Bu alan, makbuzun nakit satışlara ait toplam vergi tutarını yazdırır. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.
    - **Vergiyle birlikte toplam (satış)** – Bu alan, makbuzun toplam nakit satışı tutarını yazdırır. Tutara vergi dahildir. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.
    - **Vergi tutarı (satış)** – Bu alan, vergi kodu başına olmak üzere makbuzun nakit satışlara ait vergi tutarını yazdırır. Ön ödemeler ve hediye kartı işlemleri hariç tutulur.

Makbuz biçimleriyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Makbuz biçimlerini ayarlama ve tasarlama](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>SAF-T Yazar Kasa dışa aktarma biçimini yapılandırma

SAF-T Yazar Kasa yapılandırması Microsoft Dynamics Lifecycle Services'tan (LCS) indirilebilir. Daha fazla bilgi için bkz. [Elektronik raporlama yapılandırmalarını içe aktarma](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Aşağıdaki yapılandırmaları indirmeniz gerekir:

- **Retail channel data.version.1** – Veri modeli yapılandırması.
- **DMM Retail channel data.version.1.14** – Veri modeli eşleme yapılandırması.
- **NO SAF T Cash Register.version.1.20** – Biçim yapılandırması.

Yapılandırmaları içe aktardıktan sonra, **Commerce parametreleri** sayfasındaki **Elektronik belgeler** sekmesinin **SAF-T Yazar Kasa dışa aktarma biçimi** alanında, içe aktarılan biçim yapılandırmasının adını seçin.

Ayrıca, gerekli ana verileri önceden tanımlanmış SAF-T standart kodlarıyla eşlemeniz gerekir. Daha fazla bilgi için Norveç Vergi Dairesi tarafından sağlanan SAF-T Yazar Kasa belgelerine bakın. Eşlemeyi oluşturmak için aşağıdaki sayfalarda yeni **SAF-T Yazar kasa kodu** alanını ayarlamanız gerekir:

- Madde grupları
- Ödeme yöntemleri
- Satış vergisi kodları

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

Norveç'e özel işlevleri etkinleştirmek için kanal bileşenlerini yapılandırmanız gerekir. Daha fazla bilgi için [dağıtım kılavuzlarına](emea-nor-fi-deployment.md) bakın.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
