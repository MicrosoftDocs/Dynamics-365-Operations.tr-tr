---
title: "Fişleri Yevmiye varlığını kullanarak almak için en iyi yöntemler"
description: "Bu konuda ipuçları genel kullanarak Yevmiye verileri almak için günlük varlığı sağlar."
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
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Fişleri Yevmiye varlığını kullanarak almak için en iyi yöntemler

Bu konuda ipuçları genel kullanarak Yevmiye verileri almak için günlük varlığı sağlar.  

Bir hesap veya mahsup hesap türü olan fiş almak için yevmiye defteri varlık kullanabilirsiniz **genel muhasebe, müşteri, satıcı veya banka**. Fişi her ikisini de kullanarak bir satır girilebilir **hesap** alan ve **mahsup hesabı** alan, veya çok satırlı olarak yalnızca nerede fiş **hesap** alanı kullanıldığında (ve **mahsup hesabı** her satırda boş bırakılır). Yevmiye Defteri varlık her hesap türünü desteklemiyor. Bunun yerine, hesap türlerinin farklı birleşimlerini gerektiren senaryolar için diğer varlıklar mevcuttur. Örneğin, bir proje hareket içe aktarmak için Proje gider günlüğü varlık kullanın. Her varlık, ek alanlar kullanılabilir varlıklar bu senaryoları için ancak varlıklar için farklı bir senaryo yani belirli senaryoları desteklemek için tasarlanmıştır.

## <a name="setup"></a>Kurulum
Yevmiye Defteri varlık kullanarak almadan önce aşağıdaki Kurulum doğrula:

-   **Günlük toplu iş numarası için bir numara sırası Kurulumu** - varsayılan olarak, günlük toplu iş numarası kullandığı yevmiye defteri varlık genel muhasebe parametrelerinde tanımlanan numara sırasını kullanarak alırken. Günlük toplu iş numarası için numara serisini **El ile** olarak ayarlarsanız varsayılan sayı uygulanmaz. Bu ayar desteklenmez.
-   **Mali Boyut yapılandırma** -varlık hareketleri içe aktarmak için kullanıldığında, her kuruluşun mali boyutları sırasını tanımlamanız gerekir. Sipariş için tanımlanan **muhasebe boyutlarını bütünleştirme** biçimi, en **genel muhasebe**&gt;**hesap planı**&gt;**boyutları**&gt;**uygulamaları tümleştirmek için mali boyut yapılandırma**&gt;**veri varlıkları seçin**. İçe aktarılan genel muhasebe hesabı parçaları aynı sıraya sahip olmalıdır. Aksi takdirde, içe aktarma sırasında hata oluşur.

## <a name="general-journal-entity-setup"></a>Yevmiye defteri varlığı ayarı
Veri Yönetimi'nde iki ayarları varsayılan günlük toplu iş numarasını veya fiş numarasını nasıl uygulandığını etkiler:

-   **Kümesi tabanlı işleme** (varlıkta veri)
-   **Otomatik olarak oluşturulan** (açık alan eşlemesi)

Aşağıdaki bölümlerde bu ayarların etkisi ve ayrıca günlük toplu iş numaraları ve fiş numaralarının nasıl oluşturulduğu açıklanır.

### <a name="journal-batch-number"></a>Günlük toplu iş numarası

-   Yevmiye defteri varlığı üzerindeki **Ayarlama tabanlı işlem** ayarı günlük toplu iş numarasının oluşturulma biçimini etkilemez.
-   **Günlük toplu iş numarası** alanı **Otomatik oluşturulan** olarak ayarlanırsa içe aktarılan her bir satır için yeni bir günlük toplu iş numarası oluşturulur. Bu davranış önerilmez. **Otomatik oluşturulan** ayarı içe aktarım projesi üzerinde **Eşleme detayları**, üzerindeki **Eşlemeyi görüntüle** sekmesinin altında bulunur.
-   **Günlük toplu iş numarası** alanı **Otomatik oluşturulan** olarak ayarlanmazsa günlük toplu iş numarası aşağıdaki gibi oluşturulur:
    -   Alınan dosyada tanımlanan günlük toplu iş numarası bir varolan, deftere nakledilmemiş günlük işlemler için Microsoft Dynamics 365 içinde eşleşirse, eşleşen bir günlük toplu iş numarası bulunan tüm satırları varolan günlüğe alınır. Satırlar hiçbir zaman nakledilmiş bir günlük toplu iş numarasına aktarılmaz. Bunun yerine yeni bir numara oluşturulur.
    -   Bir varolan, deftere nakledilmemiş günlük deftere Dynamics 365 işlemleri için alınan dosyada tanımlanan günlük toplu iş numarası eşleşmiyorsa, aynı günlük toplu iş numarasına sahip tüm satırları altında yeni bir günlük gruplandırılır. Örneğin, günlük toplu iş numarası 1 olan tüm satırlar yeni bir günlüğe aktarılır ve günlük toplu iş numarası 2 olan tüm satırlar ikinci bir yeni günlüğe aktarılır. Günlük toplu iş numarası, Genel muhasebe parametrelerinde tanımlanan numara serisi kullanılarak oluşturulur.

### <a name="voucher-number"></a>Fiş numarası

-   Yevmiye defteri varlığı üzerindeki **Ayarlama tabanlı işlem** ayarını kullandığınızda fiş numarası içe aktarılan dosyada sağlanmalıdır. Fiş dengeli değilse bile Yevmiye defterindeki her hareket içe aktarılan dosyada sağlanan fiş numarasına atanır. Bir düzeltme kümesi tabanlı işleme kullanmak istediğiniz, ancak ayrıca tanımlanan numara sırası Dynamics 365 işlemleri için fiş numaraları için kullanmak istediğiniz sağlanmış Şubat 2016 yayımı için. Düzeltme numarası 3170316 olup Lifecycle Services (LCS) altından indirilerek kullanılabilir. Daha fazla bilgi için bkz. [Lifecycle Services'den düzeltmeleri indirme](..\migration-upgrade\download-hotfix-lcs.md).
    -   İşlemleri için Dynamics 365 almalar için kullanılan günlük adı üzerinde bu işlevselliği etkinleştirmek için set **deftere nakil sırasında numara tahsisi** için **Evet**.
    -   Fiş numarası yine de içe aktarılan dosyada tanımlanmalıdır. Ancak, bu sayı geçicidir ve günlük deftere nakledildiğinde işlemleri fiş numarası için Dynamics 365 tarafından üzerine yazılır. Günlük satırlarının geçici fiş numarası ile doğru bir şekilde gruplandırıldığından emin olmanız gerekir. Örneğin, deftere nakil işlemi sırasında geçici fiş numarası 1 olan üç satır bulunur. Tüm üç satırlarının geçici fiş numarası, numara serisindeki bir sonraki numarayı üzerine yazılır. Bu üç satır dengeli giriş değilse, fiş nakledilmez. Geçici fiş numarası 2 olan satırlar varsa, daha sonra bu sayı sonraki fiş numarası ile numara serisi vb. üzerine yazılır.

<!-- -->

-   Yoksa kullandığınızda **kümesi tabanlı işleme** ayarı, içe aktarılan dosyadaki bir fiş numarası vermeniz gerekmez. Fiş numaraları günlük adı ayarına göre içe aktarım sırasında oluşturulur (**Yalnızca bir fiş**, **Bakiye ile bağlantılı olarak** vb). Örneğin, bir günlük adı **Bakiye ile bağlantılı olarak** tanımlanırsa ilk satır yeni bir varsayılan fiş numarası alır. Sistem daha sonra alacakların borçlara eşit olup olmadığını belirlemek için satırı değerlendirir. Satırda bir mahsup hesabı varsa içe aktarılan bir sonraki satır yeni bir fiş numarası alır. Hiçbir mahsup hesabı yoksa sistem her yeni satır içe aktarıldığında alacakların borçlara eşit olup olmadığını değerlendirir.
-   **Fiş numarası** alanı **Otomatik oluşturulan** olarak ayarlanırsa içe aktarma başarılı olmayacaktır. **Fiş numarası** alanı için **Otomatik oluşturulan** ayarı desteklenmez.

Varsayılan olarak, Yevmiye defteri varlığı ayarlama tabanlı işlemi kullanır. Kuruluşunuz için iş gereksinimlerini değerlendirdikten sonra **Ayarlama tabanlı işlem** ayarını **Veri yönetimi** çalışma alanındaki **Veri varlıkları** 'na tıklayarak değiştirebilirsiniz. Ayarlama tabanlı işlem içe aktarma işlemini hızlandırmak için kullanılır. Ayarlama tabanlı işlemi kullanmıyorsanız Yevmiye defteri varlığının içe aktarımı daha yavaş olacaktır.


