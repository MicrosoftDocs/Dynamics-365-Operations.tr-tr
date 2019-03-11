---
title: Genel muhasebe için yabancı para birimi yeniden değerleme
description: Bu konu, kurulum, işlemi çalıştırma, işlem için hesaplama ve gerekirse yeniden değerleme işlemi hareketlerinin nasıl tersine çevrildiği de dahil olmak üzere genel muhasebe yabancı para birimi yeniden değerleme işlemine genel bir bakış sunar.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb04c5a9e7db1a6c6a8d8c7126bfa80208d1fd53
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "315556"
---
# <a name="foreign-currency-revaluation-for-general-ledger"></a>Genel muhasebe için yabancı para birimi yeniden değerleme

[!include [banner](../includes/banner.md)]

Bu konu, kurulum, işlemi çalıştırma, işlem için hesaplama ve gerekirse yeniden değerleme işlemi hareketlerinin nasıl tersine çevrildiği de dahil olmak üzere genel muhasebe yabancı para birimi yeniden değerleme işlemine genel bir bakış sunar. 

Dönem sonunun bir parçası olarak muhasebe uygulamaları farklı döviz kuru türleri (cari, geçmiş, ortalama vb.) kullanılarak yeniden değerlenen yabancı para birimlerinde genel muhasebe hesabı bakiyelerini gerektirir. Örneğin, bir muhasebe uygulaması cari döviz kurunda yeniden değerlenecek aktifler ve pasiflere, geçmiş döviz kurundaki sabit kıymetlere ve aylık ortalama kar ve zarar hesaplarına gerek duyar. Yevmiye defteri yabancı para birimi yeniden değerleme işlemi, bilanço ile kar ve zarar hesaplarını yeniden değerlemek için kullanılabilir. 

> [!NOTE]
> Yabancı para birimi yeniden değerleme işlemi, Alacak hesapları (AR) ve Borç hesapları (AP) içerisinde de kullanılabilir. Bu modülleri kullanıyorsanız, bekleyen hareketler bu modüller içerisinde yabancı para birimi yeniden değerleme işlemi ile yeniden değerlenmelidir. AR ve AP yabancı para birimi yeniden değerleme işlemi, alt defterlerde ve genel muhasebede mutabakat sağlandığından emin olunarak gerçekleşmemiş kazancı ve zararı yansıtmak amacıyla genel muhasebede bir muhasebe girişi oluşturur. AR ve AP yabancı para birimi yeniden değerleme işlemi Genel Muhasebede muhasebe girişleri oluşturduğundan alacak hesapları ve borç hesapları ana hesapları Genel muhasebe yabancı para birimi değerleme işleminin dışında tutulmalıdır. 

Yeniden değerleme işlemini çalıştırdığınızda bir yabancı para birimine nakledilen her ana hesaptaki bakiye yeniden değerlenir. Yeniden değerleme işlemi sırasında oluşturulan gerçekleşmemiş kazanç veya zarar hareketleri sistem tarafından oluşturulur. Uygunsa, biri muhasebe para birimi biri diğeri de raporlama para birimi için iki hareket oluşturulabilir. Her muhasebe girişi, gerçekleşmemiş kazanç veya zarar ve değerlendirilmekte olan ana muhasebe hesabına nakledilir.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme işlemini çalıştırmaya hazırlanma
Yeniden değerleme işlemini çalıştırmadan önce aşağıdaki kurulum gereklidir.

-   **Ana hesap** sayfasında:
-   Ana hesabın Genel muhasebede yeniden değerlemesi gerekiyorsa **Yabancı para birimi yeniden değerleme işlemi**'ni seçin. Ana hesabın yeniden değerlemesi gerekmiyorsa (örneğin, AR ve AP için alt defterlerde yeniden değerleme varsa) seçeneği temizleyin.
-   Ana hesap yeniden değerleme için işaretlenmişse **Döviz kuru türü**'nü girin. Bu döviz kuru türü, ana hesabı yeniden değerlemek için kullanılır. Mali raporlama için ayrı bir alan olan **Mali raporlama döviz kuru türü** kullanılabilir. Yeniden değerleme ve mali raporlama için kullanılmak üzere farklı döviz kuru türlerine izin veren iki alan eş zamanlı tutulmaz.

-   **Genel Muhasebe** sayfasında:
-   **Döviz kuru türü**'nü belirtin. Döviz kuru türü ana hesapta tanımlanmamışsa bu döviz kuru türü, yabancı para birimi yeniden değerleme işlemi sırasında kullanılır.
-   Para birimi yeniden değerleme işlemi için gerçekleşmiş kazanç, gerçekleşmiş zarar, gerçekleşmemiş kazanç ve gerçekleşmemiş zarar hesaplarını belirtin. Gerçekleşmiş kazanç ve gerçekleşmiş zarar hesapları, AR ve AP hareketleri kapandığında kullanılırken, gerçekleşmemiş kazanç ve gerçekleşmemiş kayıp hesapları açık hareketleri yeniden değerlemek ve genel muhasebe ana hesapları için kullanılır.

-   **Para birimi yeniden değerleme hesapları** sayfasında:
-   Her para birimi ve şirket için farklı para birimi yeniden değerleme işlemi hesaplarını seçin. Hiçbir hesap tanımlanmazsa **Genel muhasebe** sayfasındaki hesaplar kullanılır.

## <a name="process-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme işlemi gerçekleştirme
Kurulum tamamlandıktan sonra ana hesapların bakiyelerini yeniden değerlemek için **Yabancı para birimi yeniden değerleme işlemi** sayfasını kullanın. Süreci gerçek zamanlı olarak yürütebilir veya bir toplu işlem kullanarak yürütülmek üzere programlayabilirsiniz. 

**Yabancı para birimi yeniden değerleme işlemi** sayfası, işlemin çalıştırılma zamanı, hangi kriterlerin tanımlandığı, yeniden değerleme işlemi için oluşturulan fişe bağlantı ve önceki yeniden değerleme tersine çevrilmişse bir kayıt da dahil olmak üzere her bir yeniden değerleme işleminin geçmişini görüntüler. Yeniden değerleme işlemini yürütmek için **Yabancı para birimi yeniden değerleme işlemi** düğmesini seçin. 

**Başlangıç tarihi** ve **Bitiş tarihi** değerleri yeniden değerlenecek yabancı para birimi bakiyesini hesaplamak için tarih aralığını tanımlar. Kar ve kayıp hesaplarını yeniden değerlediğinizde tarih aralığında meydana gelen tüm hareketlerin toplamı yeniden değerlenir. Bilanço hesaplarını yeniden değerlediğinizde, Başlangıç tarihi göz ardı edilir. Bunun yerine, yeniden değerlemesi yapılacak bakiye mali yılın başlangıcından Bitiş tarihine kadar gelerek belirlenir. 

**Oran tarihi**, döviz kurunun varsayılan tarihini belirlemek için kullanılabilir. Örneğin, 1 Ocak ile 31 Ocak tarih aralığındaki bakiyeleri yeniden değerlendirebilirsiniz, ancak 1 Şubat'taki döviz kurunu kullanabilirsiniz. 

Hangi ana hesapların yeniden değerleneceğini seçin: Tümü, Bilanço veya Kar ve zarar. Yalnızca (Ana hesap sayfasında) yeniden değerlenmek üzere işaretlenmiş ana hesaplar yeniden değerlenir. Ana hesapların aralığını daha da kısıtlamak istiyorsanız, **dahil edilecek** sekmesi kayıtlarını ana hesap veya tekil ana hesap aralığını tanımlamak için kullanın. 

Yeniden değerleme işlemi bir veya daha fazla tüzel varlık için çalıştırılabilir. Arama yalnızca erişiminizin olduğu tüzel varlıkları görüntüler. Yeniden değerleme işlemini çalıştırmak istediğiniz tüzel varlıkları seçin. 

Yeniden değerleme işlemi bir veya daha fazla yabancı para birimi için çalıştırılabilir. Arama, yeniden değerlenecek tüzel varlıklar için ana hesap türü (Bilanço veya Kar ve Zarar) ile ilgili zaman aralığında deftere nakledilen tüm para birimlerini içerecektir. Muhasebe para birimi listeye dahil edilir, ancak muhasebe para birimi seçilirse hiçbir şey yeniden değerlenmez. 

Genel muhasebe değerlemesinin sonucunu önizlemek istiyorsanız, **Deftere nakletmeden önce önizle**'yi **Evet** olarak ayarlayın. Genel muhasebedeki önizleme, AR ve AP yabancı para birimi yeniden değerleme işlemindeki benzetimden farklıdır. AR ve AP içindeki benzetim bir rapordur, ancak genel muhasebedekinin, deftere nakletmeden önce yeniden değerleme yapmayı gerektirmeyen bir önizlemesi vardır. Tutarların nasıl hesaplandığına dair geçmişi tutmak için önizleme sonuçları Microsoft Excel'e aktarılabilir. Yeniden değerleme işleminin sonuçlarının önizlemesini görüntülemek istiyorsanız toplu işi kullanamazsınız. Kullanıcı, önizlemeden **Deftere naklet** düğmesini kullanarak tüm tüzel kişiliklerin sonuçlarını deftere nakletme seçeneğine sahiptir. Tüzel kişilik için sonuçlarla ilgili bir sorun varsa kullanıcı ayrıca **Deftere nakledilecek tüzel kişilikleri seç** düğmesini kullanarak tüzel kişiliklerin alt kümesini deftere nakletme seçeneğine de sahiptir. 

Yabancı para birimi yeniden değerleme işlemi tamamlandıktan sonra, her çalıştırmanın kaydını tutmak için bir kayıt oluşturulur.  Her bir tüzel varlık ve deftere nakil katmanı için ayrı bir kayıt oluşturulur.

## <a name="calculate-unrealized-gainloss"></a>Gerçekleşmemiş kazancı/zararı hesaplama
Gerçekleşmemiş kazanç/zarar hareketleri Genel muhasebe yeniden değerleme işlemi ile AR ve AP yeniden değerleme işlemi arasında farklı bir şekilde oluşturulur. AR ve AP'de önceki yeniden değerleme işlemi tamamen tersine çevrilir (hareketin henüz kapatılmadığı varsayılarak) ve yeni bir döviz kuruna göre gerçekleşmemiş kazanç/zarar için yeni bir yeniden değerleme işlemi hareketi oluşturulur. Bunun nedeni AR ve AP'de her hareketi tek tek yeniden değerlememizdir. Genel muhasebede, önceki yeniden değerleme tersine çevrilmez. Bunun yerine, herhangi bir önceki yeniden değerleme tutarları ve Oran Tarihi için döviz kurunu temel alan yeni değer de dahil olmak üzere ana hesabın bakiye farkı için bir hareket oluşturulur. 

**Örnek** Aşağıdaki bakiyeler 110110 ana hesabı için mevcuttur.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Tarih**   | **Genel muhasebe hesabı** | **Hareket tutarı** | **Muhasebe tutarı** |
| 20 Ocak | 110110 (Nakit)      | 500 Euro (Borç)        | 1000 ABD Doları (Borç)      |

Ana hesap 31 Ocak'ta yeniden değerlenir.  Gerçekleşmemiş kazanç/zarar, aşağıdaki şekilde hesaplanır.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Hareket para birimi cinsinden mevcut bakiye** | **Muhasebe para birimi cinsinden mevcut bakiye** | **Yeniden değerleme işlemi sırasında döviz kuru** | **Yeni muhasebe para birimi tutarı** | **Gerçekleşmemiş kazanç/zarar**    |
| 500 Euro                                     | 1000 ABD Doları                                   | 166,6667                         | 833,33 Euro (500 x 1,666667)        | 166,67 zarar (833,33 – 1000) |

Aşağıdaki muhasebe girişi oluşturulur.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Tarih**   | **Genel muhasebe hesabı**       | **Borç** | **Alacak** |
| 31 Ocak | 110110 (Nakit)            |           | 166,67     |
| 31 Ocak | 801400 (Gerçekleşmemiş zarar) | 166,67    |            |

Şubat ayı için yeni hiçbir hareket nakledilmez.  Ana hesap, 28 Şubat'ta yeniden değerlenir.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Hareket para birimi cinsinden mevcut bakiye** | **Muhasebe para birimi cinsinden mevcut bakiye** | **Yeniden değerleme işlemi sırasında döviz kuru** | **Yeni muhasebe para birimi tutarı** | **Gerçekleşmemiş kazanç/zarar**    |
| 500 Euro                                     | 833,33 ABD Doları (1000 - 166,67)                 | 250,0000                         | 1250 ABD Doları (500 x 2,5)               | 416,67 kazanç (1.250 – 833,33) |

Aşağıdaki muhasebe girişi oluşturulur.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Tarih**    | **Genel muhasebe hesabı**       | **Borç** | **Alacak** |
| Şubat 28 | 110110 (Nakit)            | 416,67    |            |
| Şubat 28 | 801600 (Gerçekleşmemiş kazanç) |           | 416,67     |

## <a name="reverse-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme işlemini tersine çevirme
Yeniden değerleme işlemi hareketini tersine çevirmeniz gerekiyorsa **Yabancı para birimi yeniden değerleme işlemi** sayfasında **Ters hareket** düğmesini seçin. Yeniden değerleme işlemi oluştuğunda veya tersine çevrildiğinde geçmiş hesap denetimi kılavuzunu düzenlemek için yeni bir yabancı para birimi yeniden değerleme işlemi geçmiş kaydı oluşturulur. 

Tarih sırasına göre değerlendirme sonuçlarını terse çevirebilirsiniz, ancak her yeniden değerlenen ana hesap için doğru bakiyeleri sağlamak için daha güncel bir yeniden değerlemeyi de tersine çevirmeniz gerekebilir. Bu tersine çevirmeler, tarih sırasının dışında gerçekleşebilir çünkü hangi ana hesapların yeniden değerleneceğinin ve ne zaman yeniden değerleneceklerinin sıklığını denetlemenin bir yolu yoktur. Örneğin, bir kuruluş nakit ana hesaplarını üç ayda bir, diğer ana hesaplarını ise ayda bir yeniden değerlemeyi seçebilir.



