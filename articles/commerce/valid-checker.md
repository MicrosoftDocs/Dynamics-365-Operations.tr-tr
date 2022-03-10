---
title: Ekstre hesaplama işlemi için mağaza hareketlerini doğrulama
description: Bu konuda, Microsoft Dynamics 365 Commerce uygulamasında mağaza hareketlerini doğrulama işlevi açıklanır.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: f51b1f39aa212fe8587761721194db7791bec5bc
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087461"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Ekstre hesaplama işlemi için mağaza hareketlerini doğrulama

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce uygulamasında mağaza hareketlerini doğrulama işlevi açıklanır. Doğrulama işlemi, ekstre deftere nakil işlemi tarafından alınmadan önce deftere nakil hatalarına neden olacak hareketleri tanımlar ve işaretler.

Bir ekstreyi deftere nakletmeyi denediğinizde ticari hareket tablolarındaki tutarsız veriler nedeniyle doğrulama işlemi başarısız olabilir. Aşağıda bu tutarsızlıklara neden olabilecek bazı etkenlere örnekler verilmiştir:

- Üst bilgi tablosundaki hareket toplamı, satırlardaki hareket toplamıyla eşleşmiyordur.
- Üst bilgi tablosunda belirtilen madde sayısı, hareket tablosundaki madde sayısıyla eşleşmiyordur.
- Üst bilgi tablosundaki vergiler, satırlardaki vergi tutarıyla eşleşmiyordur. 

Ekstre deftere nakil işlemi tarafından tutarsız hareketler alınırsa, oluşturulan satış faturaları ve ödeme günlükleri, ekstre deftere nakil işleminin başarısız olmasına neden olabilir. **Mağaza hareketlerini doğrula** işlemi, yalnızca hareket doğrulama kurallarını geçen hareketlerin hareket ekstresi hesaplama işlemine geçirilmesini sağlayarak bu sorunları önler.

Aşağıdaki şekilde, hareketleri yüklemek, doğrulamak ve hareket ekstrelerini hesaplayıp deftere nakletmek için yinelenen gün içi işlemler ile mali tabloların hesaplanması ve deftere nakledilmesine yönelik gün sonu işlemler gösterilmektedir.

![Hareketleri yüklemek, doğrulamak ve hareket ekstrelerini hesaplayıp deftere nakletmek için yinelenen gün içi işlemler ile mali tabloların hesaplanması ve deftere nakledilmesine yönelik gün sonu işlemleri gösteren şekil](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Mağaza hareketi doğrulama kuralları

**Mağaza hareketlerini doğrula** toplu işlemi, aşağıdaki doğrulama kurallarını temel alarak ticari hareket tablolarının tutarlılığını denetler.

> [!NOTE]
> Doğrulama kuralları, sonraki sürümlere eklenmeye devam eder.

### <a name="transaction-header-validation-rules"></a>Hareket üst bilgisi doğrulama kuralları

Aşağıdaki tabloda, bu hareketler ekstre deftere nakil işlemine geçirilmeden önce perakende hareketlerinin üst bilgisine göre denetlenen hareket üst bilgisi doğrulama kuralları listelenmektedir.

| Kural | Açıklama |
|-------|-------------|
| İş tarihi | Bu kural, hareketin iş tarihinin genel muhasebede açık bir mali dönemle ilişkilendirildiğini doğrular. |
| Para birimi yuvarlama | Bu kural, hareket tutarlarının para birimi yuvarlama kuralına göre yuvarlandığını doğrular. |
| Müşteri hesabı | Bu kural, harekette kullanılan müşterinin, veritabanında mevcut olduğunu doğrular. |
| İskonto tutarı | Bu kural, üst bilgideki iskonto tutarının, satırların iskonto tutarlarının toplamına eşit olduğunu doğrular. |
| Mali belge deftere nakli durumu (Brezilya) | Bu kural, mali belgenin başarıyla deftere nakledilebileceğini doğrular. |
| Brüt tutar | Bu kural, hareket üst bilgisindeki brüt tutarın, hareket satırlarının vergi dahil net tutarı artı masraflarla eşleştiğini doğrular. |
| Net | Bu kural, hareket üst bilgisindeki net tutarın, hareket satırlarının vergi hariç net tutarı artı masraflarla eşleştiğini doğrular. |
| Net + vergi | Bu kural, hareket üst bilgisindeki brüt tutarın, hareket satırlarının vergi hariç net tutarı artı tüm vergiler ve masraflarla eşleştiğini doğrular. |
| Madde sayısı | Bu kural, hareket üst bilgisinde belirtilen madde sayısının, hareket satırlarındaki miktarların toplamıyla eşleştiğini doğrular. |
| Ödeme tutarı | Bu kural, hareket üst bilgisindeki ödeme tutarının, tüm ödeme hareketlerinin toplamıyla eşleştiğini doğrular. |
| Vergi muafiyeti hesaplaması | Bu kural, masraf satırlarının hesaplanan tutarı ile muaf tutulan vergi tutarının toplamının, hesaplanan orijinal tutara eşit olduğunu doğrular. |
| Vergi dahil fiyatlandırma | Bu kural, **Vergi fiyata dahildir** bayrağının, hareket üst bilgisi ve vergi hareketleri arasında tutarlı olduğunu doğrular. |
| Hareket boş değil | Bu kural, hareketin satırlar içerdiğini ve en az bir satırın hükümsüz kılınmadığını doğrular. |
| Eksik/fazla ödeme | Bu kural, brüt tutar ile ödeme tutarı arasındaki farkın, maksimum eksik ödeme/fazla ödeme yapılandırmasından fazla olmadığını doğrular. |

### <a name="transaction-line-validation-rules"></a>Hareket satırı doğrulama kuralları

Aşağıdaki tabloda, bu hareketler ekstre deftere nakil işlemine geçirilmeden önce perakende hareketlerinin satır ayrıntılarına göre denetlenen hareket satırı doğrulama kuralları listelenmektedir.

| Kural | Açıklama |
|-------|-------------|
| Barkod | Bu kural, hareket satırlarında kullanılan tüm madde barkodlarının, veritabanında mevcut olduğunu doğrular. |
| Masraf satırları | Bu kural, masraf satırlarının hesaplanan tutarı ile muaf tutulan vergi tutarının toplamının, hesaplanan orijinal tutara eşit olduğunu doğrular. |
| Hediye kartı iadeleri | Bu kural, harekette hediye kartı iadesi olmadığını doğrular. |
| Madde çeşidi | Bu kural, hareket satırlarında kullanılan tüm maddeler ve tüm çeşitlerin, veritabanında mevcut olduğunu doğrular. |
| Satır iskontosu | Bu kural, satır iskonto tutarının, iskonto hareketlerinin toplamıyla eşleştiğini doğrular. |
| Satır vergisi | Bu kural, satır vergisi tutarının, vergi hareketlerinin toplamıyla eşleştiğini doğrular. |
| Negatif fiyat | Bu kural, hareket satırlarında negatif fiyatların kullanılmadığını doğrular. |
| Seri numarası denetlendi | Bu kural, seri numarası denetlenen maddelere ait hareket satırında seri numarasının bulunduğunu doğrular. |
| Seri numarası boyutu | Bu kural, maddenin seri numarası boyutu etkin değilse seri numarasının sağlanmadığını doğrular. |
| İşaret uyumsuzluğu | Bu kural, tüm hareket satırlarında miktar ve net tutar işaretinin aynı olduğunu doğrular. |
| Vergiden muaf | Bu kural, satır maddesi fiyatı ile muaf tutulan vergi tutarının toplamının orijinal fiyata eşit olduğunu doğrular. |
| Vergi grubu ataması | Bu kural, satış vergisi grubu ile madde vergisi grubu birleşiminin, geçerli bir vergi kesişimi oluşturduğunu doğrular. |
| Ölçü birimi dönüşümleri | Bu kural, tüm satırların ölçü biriminin, stok ölçü birimine geçerli bir şekilde dönüştürüldüğünü doğrular. |

## <a name="enable-the-store-transaction-validation-process"></a>Mağaza hareketi doğrulama işlemini etkinleştir

Commerce genel merkezinde düzenli aralıklarla çalıştırılacak **Mağaza hareketlerini doğrula** işini yapılandırın (**Retail ve Commerce \> Retail ve Commerce BT \> POS deftere nakli**). Toplu iş, mağazanın kuruluş hiyerarşisine göre zamanlanır. Bu toplu işlemi, **P İşi** ve **Hareket ekstresi hesaplaması** toplu işlerinizle aynı sıklıkta çalışacak şekilde yapılandırmanızı öneririz.

## <a name="results-of-the-validation-process"></a>Doğrulama işleminin sonuçları

**Mağaza hareketlerini doğrula** toplu işleminin sonuçları, her perakende mağaza hareketinde görüntülenebilir. Hareket kaydındaki **Doğrulama durumu** alanı **Başarılı**, **Hata** veya **Hiçbiri** olarak ayarlanır. **Son doğrulama saati** alanı, son doğrulama çalıştırmasının tarihini gösterir.

Aşağıdaki tabloda, her bir doğrulama durumu açıklanmaktadır.

| Doğrulama durumu | Açıklama |
|-------------------|-------------|
| Başarılı | Tüm etkin doğrulama kuralları geçildi. |
| Hata | Etkinleştirilmiş bir doğrulama kuralında hata belirlendi. Eylem Bölmesi'nde **Doğrulama hataları**'nı seçerek hatayla ilgili daha fazla ayrıntıyı görüntüleyebilirsiniz. |
| Hiçbiri | Hareket türü için doğrulama kurallarının uygulanması gerekmez. |

![Doğrulama durumu alanını ve Doğrulama hataları düğmesini gösteren mağaza hareketleri sayfası.](./media/valid-checker-validation-status-errors.png)

Yalnızca doğrulama durumu **Başarılı** olan hareketler, hareket ekstrelerine çekilir. **Hata** durumuna sahip hareketleri görüntülemek için **Mağaza mali öğeleri** çalışma alanında **Peşin satış doğrulama hataları** kutucuğunu inceleyin.

![Mağaza mali öğeleri çalışma alanındaki kutucuklar.](./media/valid-checker-cash-carry-validation-failures.png)

Peşin satış doğrulama hatalarını düzeltme hakkında daha fazla bilgi için bkz. [Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme](edit-cash-trans.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
