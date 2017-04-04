---
title: "Genel muhasebe için yabancı para birimi yeniden değerleme"
description: "Bu konu aşağıdaki genel muhasebe yabancı para birimi yeniden değerleme işlemi - Kurulum, gerekirse işlem hesaplama süreci ve nasıl yeniden değerleme hareketlerinin tersine çevirmek için çalışan için genel bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Genel muhasebe için yabancı para birimi yeniden değerleme

Bu konu aşağıdaki genel muhasebe yabancı para birimi yeniden değerleme işlemi - Kurulum, gerekirse işlem hesaplama süreci ve nasıl yeniden değerleme hareketlerinin tersine çevirmek için çalışan için genel bakış sağlar. 

Dönem sonunun bir parçası olarak muhasebe uygulamaları farklı döviz kuru türleri (cari, geçmiş, ortalama vb.) kullanılarak yeniden değerlenen yabancı para birimlerinde genel muhasebe hesabı bakiyelerini gerektirir. Örneğin, bir muhasebe uygulaması cari döviz kurunda yeniden değerlenecek aktifler ve pasiflere, geçmiş döviz kurundaki sabit kıymetlere ve aylık ortalama kar ve zarar hesaplarına gerek duyar. Yevmiye defteri yabancı para birimi yeniden değerleme işlemi, bilanço ile kar ve zarar hesaplarını yeniden değerlemek için kullanılabilir. 

> [!NOTE]
> Yabancı para birimi yeniden değerleme (AR) Alacak hesapları ve Borç hesapları (AP) de kullanılabilir. Bu modüllerde kullanıyorsanız, bekleyen hareketler bu modüllerde yabancı para birimi yeniden değerleme kullanarak yeniden değerlenmiş. AR ve AP yabancı para birimi yeniden değerleme işlemi, alt defterlerde ve genel muhasebede mutabakat sağlandığından emin olunarak gerçekleşmemiş kazancı ve zararı yansıtmak amacıyla genel muhasebede bir muhasebe girişi oluşturur. AR ve AP yabancı para birimi yeniden değerleme işlemi Genel Muhasebede muhasebe girişleri oluşturduğundan alacak hesapları ve borç hesapları ana hesapları Genel muhasebe yabancı para birimi değerleme işleminin dışında tutulmalıdır. 

Yeniden değerleme işlemini çalıştırdığınızda bir yabancı para birimine nakledilen her ana hesaptaki bakiye yeniden değerlenir. Yeniden değerleme işlemi sırasında oluşturulan gerçekleşmemiş kazanç veya zarar hareketleri sistem tarafından oluşturulur. İki hareket, bir hesap para birimi ve raporlama para birimi için ikinci bir uygunsa oluşturulmuş olabilir. Her hesap girişi gerçekleşmemiş kazanç veya kayıp ve Yeniden Değerlenmiş ana hesap için deftere nakleder.

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

**Oran tarihi** döviz kuru için varsayılan tarih tanımlamak için kullanılabilir. Örneğin, tarih aralığı, Ocak 1-31 Ocak arasında bakiyeleri yeniden değerlemek ancak 1 Şubat için tanımlanan döviz kuru kullanın. 

Hangi ana hesapların yeniden değerleneceğini seçin: Tümü, Bilanço veya Kar ve zarar. Yalnızca ana hesaplar için yeniden değerleme (sayfada ana hesap) işaretli değerlenir. Ana hesap aralığında daha fazla kısıtlamak istiyorsanız, kayıtları kullan **dahil etmek için** sekmesinde, ana firma ya da tek tek ana hesaplar bir aralık tanımlamak için. 

Yeniden değerleme işlemi, bir veya daha fazla tüzel kişilikler için çalıştırabilirsiniz. Arama yalnızca erişiminiz olan tüzel kişilikler görüntüler. Yeniden değerleme işlemi çalıştırmak istediğiniz yasal varlıkları seçin. 

Yeniden değerleme işlemi bir veya daha fazla yabancı para birimi için çalıştırılabilir. Arama tarih aralığı içinde yeniden değerlemek için seçilen tüzel kişilikler için ana hesap (bilanço veya kar ve zarar) türünün ilgili deftere nakledilen tüm para birimleri içerir. Hesap para birimi listede dahil edilecek, ancak hesap para seçilirse, hiçbir şey değerlenir. 

Set **deftere nakletmeden önce önizleme** için **Evet** genel muhasebe yeniden değerleme sonucu incelemek isterseniz. Önizleme genel muhasebe AR ve AP yabancı para birimi yeniden değerleme benzetim farklıdır. AR ve AP benzetim bir rapor, ancak genel muhasebe yeniden değerleme işlemi yeniden çalıştırmak zorunda kalmadan nakledilebilecek bir önizleme sahip. Tutarların nasıl hesaplandığına dair geçmişi tutmak için önizleme sonuçları Microsoft Excel'e aktarılabilir. Yeniden değerleme işleminin sonuçlarının önizlemesini görüntülemek istiyorsanız toplu işi kullanamazsınız. Kullanıcı, önizlemeden **Deftere naklet** düğmesini kullanarak tüm tüzel kişiliklerin sonuçlarını deftere nakletme seçeneğine sahiptir. Tüzel kişilik için sonuçlarla ilgili bir sorun varsa kullanıcı ayrıca **Deftere nakledilecek tüzel kişilikleri seç** düğmesini kullanarak tüzel kişiliklerin alt kümesini deftere nakletme seçeneğine de sahiptir. 

Yabancı para birimi yeniden değerleme işlemi tamamlandıktan sonra her çalışma geçmişini izlemek için bir kayıt oluşturulur.  Her bir tüzel kişilik ve deftere nakil katmanı için ayrı bir kayıt oluşturulur.

## <a name="calculate-unrealized-gainloss"></a>Gerçekleşmemiş kazancı/zararı hesaplama
Gerçekleşmemiş kazanç/zarar hareketleri Genel muhasebe yeniden değerleme işlemi ile AR ve AP yeniden değerleme işlemi arasında farklı bir şekilde oluşturulur. AR ve AP'de önceki yeniden değerleme işlemi tamamen tersine çevrilir (hareketin henüz kapatılmadığı varsayılarak) ve yeni bir döviz kuruna göre gerçekleşmemiş kazanç/zarar için yeni bir yeniden değerleme işlemi hareketi oluşturulur. Bunun nedeni AR ve AP'de her hareketi tek tek yeniden değerlememizdir. Genel muhasebedeki önceki yeniden değerleme ters değil. Bunun yerine, önceki tüm yeniden değerleme tutarları ve tarihi kuru, döviz kurunu temel alarak yeni bir değer de dahil olmak üzere ana hesap bakiyesi arasındaki aralığı için bir hareket oluşturulur. 

**Örnek** aşağıdaki bakiyeleri ana hesap 110110 mevcut.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Tarih**   | **Genel muhasebe hesabı** | **Hareket tutarı** | **Muhasebe tutarı** |
| 20 Ocak | 110110 (Nakit)      | 500 Euro (Borç)        | 1000 ABD Doları (Borç)      |

Kebir 31 Ocak Yeniden Değerlenmiş.  Gerçekleşmemiş Kazanç/Kayıp aşağıdaki gibi hesaplanır.

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

Şubat ayında hiçbir yeni hareketler deftere nakledilir.  Ana hesap 28 Şubat Yeniden Değerlenmiş.

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

Tarih sırası yeniden değerleme sonuçlarını ters kaydedebilirsiniz, ancak doğru değerleme her ana hesap bakiyesinin sağlamak için daha güncel bir yeniden değerleme de ters gerekebilir. Hangi ana hesapların değerlemeye denetlemek için bir yol ve ne zaman değerlemeye sıklığı olduğundan eski sipariş iptalleri oluşabilir. Örneğin, bir kuruluşun aylık üç aylık aralıklarla ana nakit hesaplarını, ancak diğer tüm ana hesap yeniden değerlemek seçebilirsiniz.


