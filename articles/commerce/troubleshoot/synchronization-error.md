---
title: Zaman uyumsuz sipariş eşitleme sorunları
description: Bu makalede, Microsoft Dynamics 365 Commerce'ta zaman uyumsuz sipariş oluşturma hatasının genel nedenleri açıklanmakta ve sistem kullanıcılarının ve iş ortaklarının sorunun nerede olduğunu anlamalarına yardımcı olan sorun giderme adımları sağlanmaktadır.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815769"
---
# <a name="asynchronous-order-synchronization-issues"></a>Zaman uyumsuz sipariş eşitleme sorunları

[!include [banner](../../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'ta zaman uyumsuz sipariş oluşturma hatasının genel nedenleri açıklanmakta ve sistem kullanıcılarının ve iş ortaklarının sorunun nerede olduğunu anlamalarına yardımcı olan sorun giderme adımları sağlanmaktadır.

## <a name="symptom"></a>Belirti

Dynamics 365 Commerce e-ticaretten veya satın noktasından oluşturulan zaman uyumsuz siparişler Commerce headquarters'ta yansıtılmaz.

## <a name="troubleshooting"></a>Sorun Giderme

Sipariş oluşturma işleminin başarısız olduğu aşamaya bağlı olarak, sipariş oluşturma Headquarters'da farklı nedenlerle başarısız olabilir. Aşağıdaki sorun giderme adımları olası kök nedenlerin ayrıntılarına iner.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Zaman uyumsuz siparişle ilgili hareketin Headquarters'a ulaştığından emin olun

E-ticaret siparişleri için, headquarters'da **Retail ve Commerce \> Sorgulamalar ve raporlar \> Çevrimiçi mağaza hareketleri**'ne gidin. Sipariş için bir onay numaranız varsa, **Kanal referans kimliği**  alanına onay numarasını girerek hareketleri filtreleyin. Onay numarasına sahip değilseniz, müşteri hesap numarasını girerek hareketleri filtreleyin.

POS siparişleri için **Mağaza hareketleri** sayfasını açın ve kayıtları giriş numarasına veya müşteri hesap numarasına göre filtreleyin. Hareket bulunamazsa, kanaldaki hareketleri yönetim merkeziyle eşitleyen **P-0001** kanal hareketleri işini çalıştırın. **P-0001** işi başarısız olursa, iş hatası için bir destek bileti açın. **P-0001** işi başarılı olursa ancak hareketler hala yönetim merkezinde görünmezse ilgili bilgileri içeren bir destek bileti açın.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Hareket yönetim merkezinde bulunuyorsa ancak bir satış siparişiyle bağlantılı değilse, eşitleme durumunu denetleyin

Hareket yönetim merkezinde varsa ancak satış siparişi oluşturulmamışsa **Çevrimiçi mağaza hareketleri** sayfasını açın ve **Eşitleme durumu** hızlı sekmesini seçin.   **Siparişleri eşitle** işi bu hareketi eşitlemeye çalıştıysa **Bekleyen sipariş durumu** alanı **Başarılı** veya **Başarısız** durumunu göstermelidir. Durum **Başarılı** ise satış siparişi alanı bu harekette bulunmalıdır. Durum **Başarısız** ise, **Eşitleme durumu** hızlı sekmesindeki **Sipariş hatası ayrıntıları** alanında hata ayrıntılarını görüntüleyebilirsiniz. Bu durumlardan hiçbiri gösterilmiyorsa, hareketi işleme girişiminde bulunulmamıştır. Bu durumda, eşitleme işini çalıştırmak için sayfanın üst kısmında **Siparişi eşitle**'yi seçebilirsiniz.

Zaman uyumsuz hareketlerin genel merkezde sipariş olarak oluşturulabilmesi için **Siparişleri eşitle** işinin düzenli çalışacak şekilde zamanlandığından emin olun.

Aşağıdaki bölümlerde bazı genel hatalar ve önerilen düzeltmeler hakkında bilgi sağlanmaktadır.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Sipariş hatası ayrıntıları alanı aşağıdaki hata iletisini gösterir: "Numara sırası aşıldı"

Numara sıraları, genel merkezde satış siparişleri oluşturmak için kullanılır. Bir numara sırası için izin verilen tüm numaralar tükenirse, sistem bu hata iletisini oluşturur. Satış siparişleri oluşturmak için kullanılan numara sırası **Alacak hesapları parametreleri \> Numara sıraları \> Satış siparişi** bölümünde bulunabilir. Bu hatayı düzeltmek için, var olan numara sırasını düzeltin veya yeni bir numara sırasıyla değiştirin.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Sipariş hata ayrıntıları alanı şu hata iletisini gösterir: "Kredi kartı işlemlerini işlemek için varsayılan bir ödeme hizmeti olmalıdır"

Bu hatayı düzeltmek için, yönetim merkezinde varsayılan ödemenin tanımlandığını doğrulayın. Hiçbir varsayılan ödeme tanımlanmazsa, bir tane tanımlamanız gerekir. **Alacak hesapları \> Ödeme kurulumu \> Ödeme hizmetleri**'ne gidin ve **Yeni kredi kartları için varsayılan işleyici** seçeneğinin bir ödeme hizmeti için **Evet** olarak ayarlandığından emin olun.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Sipariş hatası ayrıntıları alanı bir hesap yapısı hata iletisi gösterir

Hesap yapısı hata iletisinin metni aşağıdaki örneklerde gösterildiği gibi değişebilir. Ancak hatalar, hesap yapısı yapılandırmasıyla ilgili ortak bir kök nedeni paylaşırlar.

- "Usrt şirketindeki ARP-000959899 fişine ilişkin Günlük toplu iş numarası 0009656328 Fiş ARP-000959899 1.00 için deftere nakil sonuçları, fazla ödeme veya eksik ödeme olarak deftere nakledilir"
- "618160 kombinasyonu için günlük toplu iş numarası 0009656328 Fiş ARP-000959899 Voucher ARP-000959901 Hesap yapısı için deftere nakil sonuçları,, genel muhasebe Paylaşılan Şirket Ana Hesabı için geçerli değil"
- "Günlük toplu iş numarası 0009656328 Fiş ARP-000959899 Fiş ARP-000959901 için deftere nakil sonuçları Şirket hesapları usrt'den bildirilen"
- "Günlük toplu iş numarası 0009656328 Fiş ARP-000959899 için deftere nakil sonuçları Deftere nakil iptal edildi"
    
Bu hataları düzeltmek için hesap yapılarını doğruluk açısından gözden geçirin. Daha fazla bilgi için bkz. [Hesap yapıları yapılandırma](/dynamics365/finance/general-ledger/configure-account-structures).
    
Hata giderildikten sonra, başarısız olan hareketi seçin ve sonra eşitleme işini çalıştırmak için sayfanın üst kısmında **Siparişi eşitle**'yi seçin.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Hareket verilerinin düzeltilmesini gerektirebilecek diğer hata türleri

Hareket verilerinin düzeltilmesini gerektirebilecek diğer hata türlerini düzeltmek için "hareketleri düzenle ve denetle" özelliğini kullanabilirsiniz. Daha fazla bilgi için bkz. [Hareketleri düzenleme ve denetleme](../edit-order-trans.md).
