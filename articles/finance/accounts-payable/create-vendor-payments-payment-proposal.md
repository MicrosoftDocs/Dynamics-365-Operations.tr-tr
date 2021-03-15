---
title: Ödeme teklifi kullanarak satıcı ödemeleri oluşturma
description: Bu konu, ödeme teklifi seçeneklerine genel bir bakış sağlar ve ödeme tekliflerinin nasıl çalıştığına dair bazı örnekler içerir.
author: abruer
manager: AnnBe
ms.date: 04/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b047a1abaa6b19096740f589281c837643d796b9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003540"
---
# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Ödeme teklifi kullanarak satıcı ödemeleri oluşturma

[!include [banner](../includes/banner.md)]

Bu konu, ödeme teklifi seçeneklerine genel bir bakış sağlar ve ödeme tekliflerinin nasıl çalıştığına dair bazı örnekler içerir. Ödeme teklifleri, çoğunlukla satıcı ödemeleri oluşturmak için kullanılır çünkü sorgu ödeme için satıcı faturalarını vade tarihi ve nakit indirimi gibi kriterlere dayalı olarak hızla seçmek için kullanılabilir. 

Ödeme teklifi sorgusu vade tarihi, nakit iskontosu ve diğer ölçütlere göre ödenecek satıcı faturalarının hızlı şekilde seçilmesine olanak tanıdığından kuruluşlar satıcı ödemeleri oluşturmak için genellikle ödeme tekliflerini kullanır. 

Ödeme teklifi sorgusu, her birinde ödenecek faturayı seçmek için farklı seçenekler bulunan çeşitli seklemeler içerir. **Parametresi** sekmesi çoğu kuruluşun en sık kullandığı seçenekleri içerir. **Dahil edilecek kayıtlar** hızlı sekmesinde, hangi faturaların veya hangi satıcıların ödem için dahil edileceğini, çeşitli özellikler için aralıklar belirleyerek belirtebilirsiniz. Örneğin, yalnızca belirli bir aralıktaki satıcılara ödeme yapmak istiyorsanız, satıcı aralığı için filtre tanımlayabilirsiniz. Bu işlev genellikle belirli bir ödeme yöntemi için faturalar seçmek için kullanılır. Örneğin, **Ödeme yöntemi** = **Çek** olan bir filtre tanımlarsanız, sadece bu ödeme yöntemini seçmiş olan faturalar ödeme için seçilir, sorguda belirtilen diğer ölçütlere uymaları şartıyla. **Gelişmiş parametreler** sekmesi, bazıları kuruluşunuzla ilgili olmayabilecek ek seçenekler içerir. Örneğin, bu sekme merkezi ödemeler için fatura ödeme seçeneklerini içerir.

## <a name="parameters"></a>Parametreler
-   **Şuna göre faturaları seç** – **Başlangıç tarihi** ve **Bitiş tarihi** alanları tarafından tanımlanmış aralıkta bulunan faturalar vade tarihi, nakit iskonto tarihi veya her ikisine göre seçilebilir. Nakit iskonto tarihini kullanırsanız, sistem önce başlangıç tarihinden bitiş tarihine bir nakit iskonto tarihine sahip faturalara bakacaktır. Sistem, nakit iskontosu tarihinin geçmemiş olduğundan emin olmak için oturum tarihini kullanarak faturanın nakit iskontosu için uygun olup olmadığını belirler.
-   **Başlangıç tarihi** ve **Bitiş tarihi** – Vade tarihi veya nakit iskontosu tarihi bu aralıkta olan faturalar ödeme için seçilir.
-   **Minimum ödeme tarihi** – Minimum ödeme tarihini girin. Örneğin, **Başlangıç tarihi** ve **Bitiş tarihi** alanları 1 Eylül - 10 Eylül arasında olsun ve minimum ödeme tarihi 5 Eylül olsun. Bu durumda, 1 Eylül - 5 Eylül arasında vade tarihi olan tüm faturalar, 5 Eylül'de ödeme tarihine sahip olurlar. Ancak, 5 Eylül - 10 Eylül arasında vade tarihi bulunan tüm faturalar, her bir faturanın vade tarihine eşit olan bir ödeme tarihine sahip olurlar.
-   **Tutar limiti** – Tüm ödemeler için maksimum toplam tutarı girin.
-   **Ödemeleri fatura önizleme olmadan oluştur** – Bu seçeneği **Evet** olarak ayarlarsanız ödemeler anında **Satıcı ödemeleri** sayfasında oluşturulur. **Ödeme teklifi** sayfası atlanır. Bu nedenle, ödemeler daha hızlı oluşturulur. Ödemeler hala **Satıcı ödemeleri** sayfasından değiştirilebilir. Alternatif olarak, **Seçili ödeme için faturaları düzenle** düğmesini kullanarak **Ödeme teklifi** sayfasına geri dönebilirsiniz.

## <a name="advanced-options"></a>Gelişmiş seçenekler
- **Satıcı bakiyesini kontrol et** – Bu seçenek **Evet** olarak ayarlanırsa, sistem herhangi bir fatura ödenmeden önce bir satıcının borç bakiyesi bulunmadığını doğrular. Bir satıcının bir borç bakiyesi varsa, hiçbir ödeme oluşturulmaz. Örneğin, faturanın borç uyarları veya nakledilmiş ama henüz kapatılmamış ödemeleri bulunabilir. Bu gibi durumlarda, satıcıya ödeme yapılmaması gerekir. Bunun yerine, alacak makbuzları veya ödemeler bekleyen faturalara karşı kapatılmalıdır.
- **Negatif ödemeleri sil** – Bu seçenek, ödemelerin ayrı faturalar için yapılıp yapılmadığına veya ödeme ölçütünü karşılayan faturaların toplamına göre farklı şekilde işlev görür. Bu davranış, ödeme yönteminde tanımlanır.
- **Her fatura için ödeme** – **Negatif ödemeleri sil** seçeneği **Evet** olarak ayarlanırsa ve satıcı için kapatılmamış bir fatura ve ödeme varsa, sadece fatura ödeme için seçilir. Mevcut ödeme faturaya karşılık kapatılmaz. **Negatif ödemeleri sil** seçeneği **Hayır** olarak ayarlanırsa ve bir fatura ile bir ödeme kapatılmadıysa, hem ödeme hem de fatura ödeme için seçilir. Ödeme için bir ödeme ve bir para iadesi (negatif ödeme) oluşturulur.
- **Faturaların toplamı için ödeme** – **Negatif ödemeleri sil** seçeneği **Evet** olarak ayarlanırsa ve satıcı için kapatılmamış bir fatura ve ödeme varsa, hem kapatılmamış fatura hem de ödeme ödeme için seçilir ve tutarlar toplam ödeme tutarını oluşturmak üzere birlikte eklenir. Tek istisna toplamın bir para iadesine yol açması durumunda söz konusudur. Bu durumda, ne fatura ne de ödeme seçilir. **Negatif ödemeleri sil** seçeneği **Hayır** olarak ayarlanırsa ve bir fatura ve ödeme kapatılmadıysa, hem ödeme hem de fatura ödeme için seçilir ve tutarlar toplam ödeme tutarını oluşturmak için birlikte eklenir.
- **Yalnızca rapor yazdır** – Ödeme teklifinin sonuçlarını raporda görüntülemek ancak herhangi bir ödeme oluşturmamak istiyorsanız bu seçeneği **Evet** olarak ayarlayın.
- **Diğer tüzel kişiliklerden satıcı faturaları ekle** – Kuruluşunuz ödeme için merkezi işlem kullanıyorsa ve ödeme teklifinin arama ölçütüne dahil edilen diğer tüzel kişiliklerin faturalarını da içermesi gerekiyorsa bu seçeneği **Evet** olarak ayarlayın.
- **Her tüzel kişilik için ayrı satıcı ödemesi öner** – Bu seçenek **Evet** olarak ayarlanırsa, satıcı başına her tüzel kişilik için ayrı ödeme oluşturulur. Ödemedeki satıcı, her tüzel kişilikten gelen faturadaki satıcıdır. Bu seçenek **Hayır** olarak ayarlanırsa ve aynı satıcının birden fazla tüzel kişilikte faturası varsa, seçili faturaların toplam tutarı için bir ödeme oluşturulur. Ödemedeki satıcı, geçerli tüzel kişilikteki satıcıdır. Satıcı hesabı geçerli tüzel kişilikte mevcut değilse, ödenmesi gereken ilk faturadaki satıcı hesabı kullanılır.
- **Ödeme para birimi** – Bu alan içinde oluşturulan tüm ödemelerin para birimini belirtir. Bir para birimi tanımlanmamış ise, her bir fatura faturanın para birimi cinsinden ödenir.
- **Ödeme günü** – Ödemenin yapılması gereken günü girin. Bu alan yalnızca ödeme yöntemi, haftanın belirli bir günündeki ödeme için tüm faturalar olarak ayarlandıysa kullanılır.
- **Mahsup hesap türü** ve **Mahsup hesap** – Bu alanları belirli bir hesap türünü ve mahsup hesabı (örneğin **Defter** veya **Banka**) ve tanımlamak için ayarlayın. Fatura için ödeme yöntemi varsayılan mahsup hesap türünü ve mahsup hesabı tanımlar, ancak bu alanları, varsayılan değerleri geçersiz kılmak için kullanabilirsiniz.
- **Özetlenmiş ödeme tarihi** – Bu yalnızca ödeme yöntemi üzerindeki **Dönem** alanı **Toplam** olarak ayarlanmışsa kullanılır. Bir tarih belirlenirse, tüm ödemeler tüm tarihte oluşturulur. **Minimum ödeme tarihi** alanı göz ardı edilir.
- **Ek filtreler** – **Dahil edilecek kayıtlar** hızlı sekmesinde, ek ölçüt aralıkları tanımlayabilirsiniz. Örneğin, yalnızca bir aralıktaki satıcılara ödeme yapmak istiyorsanız, satıcı aralığı için filtre tanımlayabilirsiniz. Bu işlev genellikle belirli bir ödeme yöntemi için faturalar seçmek için kullanılır. Örneğin, **Ödeme yöntemi** = **Çek** olan bir filtre tanımlarsanız, sadece bu ödeme yöntemini seçmiş olan faturalar ödeme için seçilir, sorguda belirtilen diğer ölçütlere uymaları şartıyla.

## <a name="scenarios"></a>Senaryolar

| Satıcı | Fatura | Fatura tarihi | Fatura tutarı | Vade tarihi | Nakit iskontosu tarihi | Nakit iskontosu tutarı |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15 Haziran      | 500,00         | 15 Temmuz  | 29 Haziran            | 10,00                |
| 3050   | 1002    | 20 Haziran      | 600,00         | 20 Temmuz  | 4 Temmuz             | 12,00                |
| 3075   | 1003    | 15 Haziran      | 250,00         | 29 Haziran  |                    | 0,00                 |
| 3100   | 1004    | 17 Haziran      | 100,00         | 17 Temmuz  | 1 Temmuz             | 1,00                 |

1 Temmuz'da April satıcılara ödeme yapar. Bu görevi daha etkin şekilde tamamlamak için bir ödeme teklifi kullanır.

### <a name="option-1-by-cash-discount"></a>Seçenek 1: Nakit iskontosuna göre

April teklif türü olarak **Nakit iskontosu**'nu seçer. 26 Haziran - 10 Temmuz tarih aralığı girer. Aşağıdaki faturalar teklife dahil edilir:

-   1002; çünkü iskonto tarihi olan 4 Temmuz ödeme tarihi aralığında bulunur.
-   1004; çünkü iskonto tarihi olan 1 Temmuz ödeme tarihi aralığında bulunur.

Aşağıdaki faturalar teklife dahil edilmez:

-   1001; çünkü iskonto tarihi olan 29 Haziran geçtiğinden bu fatura artık nakit iskontosuna uygun değildir.
-   1003; çünkü bu faturada bir iskonto tarihi yoktur.

### <a name="option-2-by-due-date"></a>Seçenek 2: Vade tarihine göre

April teklif türü olarak **Vade tarihine göre**'yi seçer. 26 Haziran - 10 Temmuz tarih aralığı girer. Aşağıdaki faturalar teklife dahil edilir:

-   1003; çünkü vade tarihi olan 29 Haziran ödeme tarihi aralığındadır.

Aşağıdaki faturalar teklife dahil edilmez:

-   1001; çünkü vade tarihi olan 15 Temmuz ödeme tarihi aralığı dışındadır.
-   1002; çünkü vade tarihi olan 20 Temmuz ödeme tarihi aralığı dışındadır.
-   1004; çünkü vade tarihi olan 17 Temmuz ödeme tarihi aralığı dışındadır.

### <a name="option-3-by-due-date-and-cash-discount"></a>Seçenek 3: Vade tarihine ve nakit iskontosuna göre

April teklif türü olarak **Vade tarihi ve nakit iskontosu**'nu seçer. 26 Haziran - 10 Temmuz tarih aralığı girer. Aşağıdaki faturalar teklife dahil edilir:

-   1003; çünkü vade tarihi olan 29 Haziran ödeme tarihi aralığındadır.
-   1002; çünkü iskonto tarihi olan 4 Temmuz ödeme tarihi aralığında bulunur.
-   1004; çünkü iskonto tarihi olan 1 Temmuz ödeme tarihi aralığında bulunur.

Aşağıdaki faturalar teklife dahil edilmez:

-   1001; çünkü iskonto tarihi olan 29 Haziran geçmiştir, bu nedenle bu fatura artık nakit iskontosuna uygun değildir ve vade tarihi olan 15 Temmuz da belirtilen tarih aralığı dışındadır.

## <a name="country-specific-considerations"></a>Ülkeye özgü hususlar
### <a name="norway"></a>Norveç

#### <a name="dimension-control"></a>Boyut kontrolü

Boyut kontrolü, oluşturulan satırları ödeme tekliflerine göre gruplamayı kontrol etmenizi ve kesilen faturalar için mali boyutları temel alarak varsayılan boyutları ayarlamanızı sağlar. Norveç ülke/bölge bağlamına göre her ödeme yöntemi için boyut kontrolünü ve her boyut için gruplamayı etkinleştirebileceğiniz mali boyut sekmesi bulunur. Mümkün olan seçenekler şunlardır:

-   **Boyut kontrolü** alanı devre dışı bırakılır. Ödeme teklifi diğer ülkelerde olduğu gibi davranır.
-   **Boyut kontrolü** alanı boyutlar daha ayrıntılı tanımlanmadan etkinleştirilir. Ödeme teklifi, boyutlar dikkate alınmadan oluşturulur. Oluşturulan işlem uygulanan girişten hiçbir boyutu devralmaz.
-   **Boyut denetimi** alanı ve ayrıntılı boyutlar etkinleştirilir. Şimdi boyutların günlüğe nasıl kopyalanacağını tanımlarsınız. Örneğin: • **BusinessUnit** onay kutusunu, ödeme yöntemi için bir ödeme teklifi oluşturmak üzere seçin. • **CostCenter** onay kutusunu, ödeme yöntemi için bir ödeme teklifine göre maliyet merkezi oluşturmak için seçin

> [[!NOTE]
> Üçünü seçenekte birden çok boyut seçerseniz boyut birleşimi için bir ödeme teklifi oluşturulur.

#### <a name="bank-account-selection"></a>Banka hesabı seçimi

Ülke bağlamından bağımsız olarak her ödeme yöntemi için standart bir borçlandırma ödeme hesabı tanımlayabilirsiniz. Bu, bir teklif tarafından oluşturulan ödeme satırlarında ayarlanır. Banka hesabı özelliğiyle boyut ve para birimi veya her bir birleşime bağlı olarak farklı borçlandırma banka hesabı kullanmak için bunların bir birleşimi tarafından yönetilen birden çok borçlandırma banka hesabı tanımlayabilirsiniz. Bu bileşenleri **Deftere nakil hesabı türü** = **Banka** olan her ödeme yöntemi için kullanılabilir **Banka hesapları**'nı kullanarak **Ödeme yöntemleri**'nde ayarlayabilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]