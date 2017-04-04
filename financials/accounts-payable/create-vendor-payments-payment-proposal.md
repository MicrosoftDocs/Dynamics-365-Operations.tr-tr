---
title: "Ödeme teklifi kullanarak satıcı ödemeleri oluşturma"
description: "Bu konu, ödeme teklifi seçeneklerine genel bir bakış sağlar ve ödeme tekliflerinin nasıl çalıştığına dair bazı örnekler içerir. Ödeme teklifleri, çoğunlukla satıcı ödemeleri oluşturmak için kullanılır çünkü sorgu ödeme için satıcı faturalarını vade tarihi ve nakit indirimi gibi kriterlere dayalı olarak hızla seçmek için kullanılabilir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: b46037b9509f329e18f0da69d530f6b1f88c8888
ms.lasthandoff: 03/31/2017


---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Ödeme teklifi kullanarak satıcı ödemeleri oluşturma

Bu konu, ödeme teklifi seçeneklerine genel bir bakış sağlar ve ödeme tekliflerinin nasıl çalıştığına dair bazı örnekler içerir. Ödeme teklifleri, çoğunlukla satıcı ödemeleri oluşturmak için kullanılır çünkü sorgu ödeme için satıcı faturalarını vade tarihi ve nakit indirimi gibi kriterlere dayalı olarak hızla seçmek için kullanılabilir. 

Ödeme teklifi sorgusu vade tarihi, nakit iskontosu ve diğer ölçütlere göre ödenecek satıcı faturalarının hızlı şekilde seçilmesine olanak tanıdığından kuruluşlar satıcı ödemeleri oluşturmak için genellikle ödeme tekliflerini kullanır. 

Ödeme teklifi sorgusu, her birinde ödenecek faturayı seçmek için farklı seçenekler bulunan çeşitli seklemeler içerir. **Parametresi** çoğu kuruluşun en sık kullandığınız seçenekleri sekmesi içerir. Üzerinde **kayıtları dahil etmek için** hızlı, hangi faturaları veya aralıkları için çeşitli özelliklerini tanımlayarak ödeme için dahil edilecek satıcılar belirtebilirsiniz. Örneğin, yalnızca belirli bir aralık satıcıların ödeme yapmak istiyorsanız, satıcı aralığı için filtre tanımlayabilirsiniz. Bu işlev genellikle faturalar için belirli bir ödeme yöntemi seçmek için kullanılır. Örneğin, bir filtre tanımlamak burada **ödeme yöntemi** = **kontrol**, onların da sorguda belirtilen diğer ölçütleri karşılaması koşuluyla, bu ödeme yöntemi olan fatura ödeme için seçilir. **Gelişmiş parametreler** sekmesi, bazıları kuruluşunuzla ilgili olmayabilecek ek seçenekler içerir. Örneğin, bu sekme merkezi ödemeler için fatura ödeme seçeneklerini içerir.

## <a name="parameters"></a>Parametreler
-   **Tarafından faturaları seçin** – tarafından belirtilen tarih aralığındaki faturaları **tarihinden** ve **tarihine** alanları seçilebilir tarafından tarihi, nakit iskontosu tarihi veya hem de. Nakit iskonto tarihini kullanırsanız, sistem ilk arasında bir nakit iskontosu tarihine sahip faturaları arar başlangıç tarihi ve bitiş tarihi. Sistem, nakit iskontosu tarihinin geçmemiş olduğundan emin olmak için oturum tarihini kullanarak faturanın nakit iskontosu için uygun olup olmadığını belirler.
-   **Başlangıç tarihi** ve** Bitiş tarihi** – Vade tarihi veya nakit iskontosu tarihi bu aralıkta olan faturalar ödeme için seçilir.
-   **Ödeme tarihi** – Bir tarih belirlenirse, tüm ödemeler tüm tarihte oluşturulur. **Minimum ödeme tarihi** alanı göz ardı edilir.
-   **Minimum ödeme tarihi** – Minimum ödeme tarihini girin. Örneğin, **tarihinden** ve **tarihine** alanlar 10 Eylül 1 Eylül'den bir aralık belirtmek ve minimum ödeme tarihi 5 Eylül. Bu durumda, bir ödeme tarihi 5 Eylül 1 Eylül 5 Eylül için bir son tarih sahip tüm faturaları vardır. Ancak, her bir fatura vade tarihine eşit olan bir ödeme tarihi 5 Eylül 10 Eylül için bir son tarih sahip tüm faturaları vardır.
-   **Tutar limiti** – Tüm ödemeler için maksimum toplam tutarı girin.
-   **Ödemeler fatura Önizleme olmadan oluşturmak** – bu seçenek ayarlanırsa **Evet**, ödemeler oluşturulacak hemen üzerinde **satıcı ödemelerini** sayfa. **Ödeme teklifi** sayfası atlanacak. Bu nedenle, ödemeler daha hızlı oluşturulur. Ödemeler hala **Satıcı ödemeleri** sayfasından değiştirilebilir. Alternatif olarak, **Seçili ödeme için faturaları düzenle** düğmesini kullanarak **Ödeme teklifi** sayfasına geri dönebilirsiniz.

## <a name="advanced-options"></a>Gelişmiş seçenekler
-   **Satıcı bakiyesini kontrol et** – Bu seçenek **Evet** olarak ayarlanırsa, sistem herhangi bir fatura ödenmeden önce bir satıcının borç bakiyesi bulunmadığını doğrular. Bir satıcı bir borç bakiyesi varsa, hiçbir ödeme oluşturulur. Örneğin, satıcıya iade faturaları veya nakledilmiş ancak henüz tasfiye henüz ödeme olabilir. Bu gibi durumlarda, satıcıya ödeme yapılmaması gerekir. Bunun yerine, alacak makbuzları veya ödemeler bekleyen faturalara karşı kapatılmalıdır.
-   **Negatif ödemeleri sil** – Bu seçenek, ödemelerin ayrı faturalar için yapılıp yapılmadığına veya ödeme ölçütünü karşılayan faturaların toplamına göre farklı şekilde işlev görür. Bu davranış, ödeme yönteminde tanımlanır.
-   **Her fatura için ödeme** – **Negatif ödemeleri sil** seçeneği **Evet** olarak ayarlanırsa ve satıcı için kapatılmamış bir fatura ve ödeme varsa, sadece fatura ödeme için seçilir. Mevcut ödeme faturaya karşılık kapatılmaz. **Negatif ödemeleri sil** seçeneği **Hayır** olarak ayarlanırsa ve bir fatura ile bir ödeme kapatılmadıysa, hem ödeme hem de fatura ödeme için seçilir. Ödeme için bir ödeme ve bir para iadesi (negatif ödeme) oluşturulur.
-   **Faturaların toplamı için ödeme** – **Negatif ödemeleri sil** seçeneği **Evet** olarak ayarlanırsa ve satıcı için kapatılmamış bir fatura ve ödeme varsa, hem kapatılmamış fatura hem de ödeme ödeme için seçilir ve tutarlar toplam ödeme tutarını oluşturmak üzere birlikte eklenir. Tek istisna toplamın bir para iadesine yol açması durumunda söz konusudur. Bu durumda, ne fatura ne de ödeme seçilir. Varsa ** Eksi ödemeleri Sil ** seçeneği ayarlanmış **No**, fatura ve ödeme kapatılan değil, hem fatura ve ödeme için ödeme seçilir ve tutarları eklenir birlikte toplam ödeme tutarı üretmesine yönelik.
-   **Yalnızca rapor yazdır** – Ödeme teklifinin sonuçlarını raporda görüntülemek ancak herhangi bir ödeme oluşturmamak istiyorsanız bu seçeneği **Evet** olarak ayarlayın.
-   **Diğer tüzel kişiliklerden satıcı faturaları ekle** – Kuruluşunuz ödeme için merkezi işlem kullanıyorsa ve ödeme teklifinin arama ölçütüne dahil edilen diğer tüzel kişiliklerin faturalarını da içermesi gerekiyorsa bu seçeneği **Evet** olarak ayarlayın.
-   **Her tüzel kişilik için ayrı satıcı ödemesi öner** – Bu seçenek **Evet** olarak ayarlanırsa, satıcı başına her tüzel kişilik için ayrı ödeme oluşturulur. Ödemedeki satıcı, her tüzel kişilikten gelen faturadaki satıcıdır. Bu seçenek **Hayır** olarak ayarlanırsa ve aynı satıcının birden fazla tüzel kişilikte faturası varsa, seçili faturaların toplam tutarı için bir ödeme oluşturulur. Ödemedeki satıcı, geçerli tüzel kişilikteki satıcıdır. Satıcı hesabı geçerli tüzel kişilikte mevcut değilse, ödenmesi gereken ilk faturadaki satıcı hesabı kullanılır.
-   **Ödeme para birimi** – Bu alan içinde oluşturulan tüm ödemelerin para birimi belirtir. Bir para birimi tanımlanmamış ise, her bir fatura Fatura para birimi cinsinden ödenir.
-   **Ödeme günü** – Ödemenin yapılması gereken günü girin. Bu alan yalnızca ödeme yöntemi, haftanın belirli bir günündeki ödeme için tüm faturalar olarak ayarlandıysa kullanılır.
-   **Mahsup hesap türü** ve **mahsup hesabı** – özel hesap türünü tanımlamak için bu alanları ayarlayın (gibi **defter** veya **banka**) ve mahsup hesabı (örneğin, belirli bir banka hesabı). Varsayılan mahsup hesap tipi ve mahsup fatura için ödeme yöntemini tanımlar, ancak varsayılan değerleri geçersiz kılmak için bu alanları kullanabilirsiniz.
-   **Ek filtreler** – On **kayıtları dahil etmek için** hızlı, ek ölçüt aralıkları tanımlayabilirsiniz. Örneğin, yalnızca bir aralıktaki satıcılarına ödeme yapmak istiyorsanız, satıcı aralığı için filtre tanımlayabilirsiniz. Bu işlev genellikle faturalar için belirli bir ödeme yöntemi seçmek için kullanılır. Örneğin, bir filtre tanımlamak burada **ödeme yöntemi** = **kontrol**, onların da sorguda belirtilen diğer ölçütleri karşılaması koşuluyla, bu ödeme yöntemi olan fatura ödeme için seçilir.

## <a name="scenarios"></a>Senaryolar
| Satıcı | Fatura | Fatura tarihi | Fatura tutarı | Vade tarihi | Nakit iskontosu tarihi | Nakit iskontosu tutarı |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15 Haziran      | 500,00         | 15 Temmuz  | 29 Haziran            | 10,00                |
| 3050   | 1002    | 20 Haziran      | 600,00         | 20 Temmuz  | 4 Temmuz             | 12,00                |
| 3075   | 1003    | 15 Haziran      | 250,00         | 29 Haziran  |                    | 0,00                 |
| 3100   | 1004    | 17 Haziran      | 100,00         | 17 Temmuz  | 1 Temmuz             | 1,00                 |

1 Temmuz'da April satıcılara ödeme yapar. Bu görevi daha etkin şekilde tamamlamak için bir ödeme teklifi kullanır.

### <a name="option-1-by-cash-discount"></a>Seçenek 1: Nakit iskontosuna göre

April teklif türü olarak **Nakit iskontosu**'nu seçer. Filiz bir tarih aralığı, Haziran 26 Temmuz 10 girer. Aşağıdaki fatura teklifinde yer:

-   1002; çünkü iskonto tarihi olan 4 Temmuz ödeme tarihi aralığında bulunur.
-   1004; çünkü iskonto tarihi olan 1 Temmuz ödeme tarihi aralığında bulunur.

Aşağıdaki faturalar teklife dahil edilmez:

-   1001; çünkü iskonto tarihi olan 29 Haziran geçtiğinden bu fatura artık nakit iskontosuna uygun değildir.
-   1003; çünkü bu faturada bir iskonto tarihi yoktur.

### <a name="option-2-by-due-date"></a>Seçenek 2: Vade tarihine göre

April teklif türü olarak **Vade tarihine göre**'yi seçer. Filiz bir tarih aralığı, Haziran 26 Temmuz 10 girer. Aşağıdaki fatura teklifinde yer:

-   1003; çünkü vade tarihi olan 29 Haziran ödeme tarihi aralığındadır.

Aşağıdaki faturalar teklife dahil edilmez:

-   1001; çünkü vade tarihi olan 15 Temmuz ödeme tarihi aralığı dışındadır.
-   1002; çünkü vade tarihi olan 20 Temmuz ödeme tarihi aralığı dışındadır.
-   1004; çünkü vade tarihi olan 17 Temmuz ödeme tarihi aralığı dışındadır.

### <a name="option-3-by-due-date-and-cash-discount"></a>Seçenek 3: Vade tarihine ve nakit iskontosuna göre

April teklif türü olarak **Vade tarihi ve nakit iskontosu**'nu seçer. Filiz bir tarih aralığı, Haziran 26 Temmuz 10 girer. Aşağıdaki fatura teklifinde yer:

-   1003; çünkü vade tarihi olan 29 Haziran ödeme tarihi aralığındadır.
-   1002; çünkü iskonto tarihi olan 4 Temmuz ödeme tarihi aralığında bulunur.
-   1004; çünkü iskonto tarihi olan 1 Temmuz ödeme tarihi aralığında bulunur.

Aşağıdaki faturalar teklife dahil edilmez:

-   1001; çünkü iskonto tarihi olan 29 Haziran geçmiştir, bu nedenle bu fatura artık nakit iskontosuna uygun değildir ve vade tarihi olan 15 Temmuz da belirtilen tarih aralığı dışındadır.

## <a name="country-specific-considerations"></a>Ülkeye özgü hususlar
### <a name="norway"></a>Norveç

#### <a name="dimension-control"></a>Boyut kontrolü

Boyut kontrolü, oluşturulan satırları ödeme tekliflerine göre gruplamayı kontrol etmenizi ve kesilen faturalar için mali boyutları temel alarak varsayılan boyutları ayarlamanızı sağlar. Norveç ülke bağlamına göre her ödeme yöntemi için boyut kontrolünü ve her boyut için gruplamayı etkinleştirebileceğiniz mali boyut sekmesi bulunur. Mümkün olan seçenekler şunlardır:

-   **Boyut kontrolü** alanı devre dışı bırakılır. Ödeme teklifi diğer ülkelerde olduğu gibi davranır.
-   **Boyut kontrolü** alanı boyutlar daha ayrıntılı tanımlanmadan etkinleştirilir. Ödeme teklifi, boyutlar dikkate alınmadan oluşturulur. Oluşturulan işlem uygulanan girişten hiçbir boyutu devralmaz.
-   **Boyut kontrolü** alanı ve ayrıntılı boyutlar etkinleştirilir. Şimdi boyutların günlüğe nasıl kopyalanacağını tanımlarsınız. Örneğin: • seçin **departmanı** bir ödeme teklifi iş birimi başına yöntemi için ödeme, • seçin oluşturmak için bu onay kutusunu **CostCenter** bir ödeme teklifi başına maliyet merkezi yöntemi için ödeme oluşturmak için onay kutusunu

**Not:** Üçünü seçenekte birden çok boyut seçerseniz boyut birleşimi için bir ödeme teklifi oluşturulur.

#### <a name="bank-account-selection"></a>Banka hesabı seçimi

Ülke bağlamından bağımsız olarak her ödeme yöntemi için standart bir borçlandırma ödeme hesabı tanımlayabilirsiniz. Bu, bir teklif tarafından oluşturulan ödeme satırlarında ayarlanır. Banka hesabı özelliğiyle boyut ve para birimi veya her bir birleşime bağlı olarak farklı borçlandırma banka hesabı kullanmak için bunların bir birleşimi tarafından yönetilen birden çok borçlandırma banka hesabı tanımlayabilirsiniz. Bu birleşimler ayarlayabilirsiniz **ödeme yöntemleri** kullanarak sayfayı **banka hesaplarını** düğmesini her yöntemi ile ödeme için kullanılabilir **hesap türü deftere nakil** = **banka**.


