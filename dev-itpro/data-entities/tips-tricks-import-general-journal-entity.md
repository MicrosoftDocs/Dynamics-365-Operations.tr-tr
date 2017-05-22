---
title: "Yevmiye defteri varlığını kullanarak fişleri içe aktarmak için en iyi uygulamalar"
description: "Bu konuda, Yevmiye defteri varlığı kullanılarak Yevmiye defterine veri aktarmak için ipuçları verilmektedir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3f13e07a1adf74982a8b220296ae72d71075e0e3
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Yevmiye defteri varlığını kullanarak fişleri içe aktarmak için en iyi uygulamalar

[!include[banner](../includes/banner.md)]


Bu konuda, Yevmiye defteri varlığı kullanılarak Yevmiye defterine veri aktarmak için ipuçları verilmektedir.  

**Genel Muhasebe, Müşteri, Satıcı veya Banka** türünde hesabı veya mahsup hesabı olan fişleri içe aktarmak için Yevmiye defteri varlığını kullanabilirsiniz. Fiş **Hesap** alanı ve **Mahsup hesap** alanı birlikte kullanılarak tek satır halinde girilebileceği gibi, yalnızca **Hesap** alanı kullanılarak (ve **Mahsup hesap** alanı her satırda boş bırakılarak) çok satırlı fiş halinde girilebilir. Yevmiye defteri varlığı her hesap türünü desteklemez. Bunun yerine, hesap türlerinin farklı birleşimlerini gerektiren senaryolar için diğer varlıklar mevcuttur. Örneğin, bir proje hareketini içe aktarmak için Proje gider günlüğü varlığını kullanın. Her bir varlık belirli senaryoları desteklemek üzere tasarlanmıştır. Bu, bazı senaryolar için varlıklarda kullanılabilen ek alanların farklı bir senaryonun varlıklarında kullanılamayabileceği anlamına gelir.

## <a name="setup"></a>Kurulum
Yevmiye defteri varlığını kullanarak içe aktarmadan önce aşağıdaki ayarı doğrulayın:

-   **Günlük toplu iş numarası için numara serisi ayarı** - Varsayılan olarak Yevmiye defteri varlığını kullanarak içe aktardığınızda günlük toplu iş numarası Genel muhasebe parametrelerinde tanımlanan numara serisini kullanır. Günlük toplu iş numarası için numara serisini **El ile** olarak ayarlarsanız varsayılan sayı uygulanmaz. Bu ayar desteklenmez.
-   **Mali boyut yapılandırması** - Varlıklar hareketleri içe aktarmak için kullanıldığında her organizasyon mali boyutların sırasını tanımlamalıdır. Sıra, **Genel muhasebe boyutları entegrasyonu biçimi** için, **Genel muhasebe**'de &gt; **Hesap planı** &gt; **Boyutlar** &gt; **Uygulamaları tümleştirmek için mali boyut yapılandırması** &gt; **Veri varlıklarını seç** şeklinde tanımlanır. İçe aktarılan genel muhasebe hesabı parçaları aynı sıraya sahip olmalıdır. Aksi takdirde, içe aktarma sırasında hata oluşur.

## <a name="general-journal-entity-setup"></a>Yevmiye defteri varlığı ayarı
Veri yönetimindeki iki ayar varsayılan günlük toplu iş numarasının veya fiş numarasının uygulanışını etkiler:

-   **Ayarlama tabanlı işlem** (veri varlığında)
-   **Otomatik oluşturulan** (alan eşlemesinde)

Aşağıdaki bölümlerde bu ayarların etkisi ve ayrıca günlük toplu iş numaraları ve fiş numaralarının nasıl oluşturulduğu açıklanır.

### <a name="journal-batch-number"></a>Günlük toplu iş numarası

-   Yevmiye defteri varlığı üzerindeki **Ayarlama tabanlı işlem** ayarı günlük toplu iş numarasının oluşturulma biçimini etkilemez.
-   **Günlük toplu iş numarası** alanı **Otomatik oluşturulan** olarak ayarlanırsa içe aktarılan her bir satır için yeni bir günlük toplu iş numarası oluşturulur. Bu davranış önerilmez. **Otomatik oluşturulan** ayarı içe aktarım projesi üzerinde **Eşleme detayları**, üzerindeki **Eşlemeyi görüntüle** sekmesinin altında bulunur.
-   **Günlük toplu iş numarası** alanı **Otomatik oluşturulan** olarak ayarlanmazsa günlük toplu iş numarası aşağıdaki gibi oluşturulur:
    -   İçe aktarılan dosyada tanımlanan günlük toplu iş numarası Microsoft Dynamics 365 for Operations'taki nakledilmemiş mevcut günlük defterle eşleşiyorsa günlük toplu iş numarasıyla eşleşen tüm satırlar mevcut günlüğe aktarılır. Satırlar hiçbir zaman nakledilmiş bir günlük toplu iş numarasına aktarılmaz. Bunun yerine yeni bir numara oluşturulur.
    -   İçe aktarılan dosyada tanımlanan günlük toplu iş numarası Microsoft Dynamics 365 for Operations'taki nakledilmemiş mevcut günlük defterle eşleşmiyorsa aynı günlük toplu iş numarasına sahip tüm satırlar yeni bir günlük altında gruplanır. Örneğin, günlük toplu iş numarası 1 olan tüm satırlar yeni bir günlüğe aktarılır ve günlük toplu iş numarası 2 olan tüm satırlar ikinci bir yeni günlüğe aktarılır. Günlük toplu iş numarası, Genel muhasebe parametrelerinde tanımlanan numara serisi kullanılarak oluşturulur.

### <a name="voucher-number"></a>Fiş numarası

-   Yevmiye defteri varlığı üzerindeki **Ayarlama tabanlı işlem** ayarını kullandığınızda fiş numarası içe aktarılan dosyada sağlanmalıdır. Fiş dengeli değilse bile Yevmiye defterindeki her hareket içe aktarılan dosyada sağlanan fiş numarasına atanır. Ayarlama tabanlı işlemi kullanmak istiyor ancak ayrıca Microsoft Dynamics 365 for Operations'ta fiş numaraları için tanımlanan numara serisini de kullanmak istiyorsanız Şubat 2016 sürümü için bir düzeltme sağlanmıştır. Düzeltme numarası 3170316 olup Lifecycle Services (LCS) altından indirilerek kullanılabilir. Daha fazla bilgi için bkz. [Lifecycle Services'den düzeltmeleri indirme](..\migration-upgrade\download-hotfix-lcs.md).
    -   Microsoft Dynamics 365 for Operations'taki içe aktarmalar için kullanılan günlük adı üzerinden bu işlevleri etkinleştirmek için **Deftere nakil sırasında numara tahsisi** için **Evet** ayarını yapın.
    -   Fiş numarası yine de içe aktarılan dosyada tanımlanmalıdır. Ancak bu sayı geçicidir ve günlük nakledildiğinde Microsoft Dynamics 365 for Operations fiş numarası ile üzerine yazılır. Günlük satırlarının geçici fiş numarası ile doğru bir şekilde gruplandırıldığından emin olmanız gerekir. Örneğin, deftere nakil işlemi sırasında geçici fiş numarası 1 olan üç satır bulunur. Üç satırın hepsinin geçici fiş numarası, numara serisindeki sonraki numarayla değiştirilir. Bu üç satır dengeli giriş değilse, fiş nakledilmez. Geçici fiş numarası 2 olan satırlar varsa, daha sonra bu sayı sonraki fiş numarası ile numara serisi vb. üzerine yazılır.

<!-- -->

-   **Ayarlama tabanlı işlem** ayarını kullanmadığınızda içe aktarılan dosyada fiş numarası sağlamanız gerekmez. Fiş numaraları günlük adı ayarına göre içe aktarım sırasında oluşturulur (**Yalnızca bir fiş**, **Bakiye ile bağlantılı olarak** vb). Örneğin, bir günlük adı **Bakiye ile bağlantılı olarak** tanımlanırsa ilk satır yeni bir varsayılan fiş numarası alır. Sistem daha sonra alacakların borçlara eşit olup olmadığını belirlemek için satırı değerlendirir. Satırda bir mahsup hesabı varsa içe aktarılan bir sonraki satır yeni bir fiş numarası alır. Hiçbir mahsup hesabı yoksa sistem her yeni satır içe aktarıldığında alacakların borçlara eşit olup olmadığını değerlendirir.
-   **Fiş numarası** alanı **Otomatik oluşturulan** olarak ayarlanırsa içe aktarma başarılı olmayacaktır. **Fiş numarası** alanı için **Otomatik oluşturulan** ayarı desteklenmez.

Varsayılan olarak, Yevmiye defteri varlığı ayarlama tabanlı işlemi kullanır. Kuruluşunuz için iş gereksinimlerini değerlendirdikten sonra **Ayarlama tabanlı işlem** ayarını **Veri yönetimi** çalışma alanındaki **Veri varlıkları** 'na tıklayarak değiştirebilirsiniz. Ayarlama tabanlı işlem içe aktarma işlemini hızlandırmak için kullanılır. Ayarlama tabanlı işlemi kullanmıyorsanız Yevmiye defteri varlığının içe aktarımı daha yavaş olacaktır.



