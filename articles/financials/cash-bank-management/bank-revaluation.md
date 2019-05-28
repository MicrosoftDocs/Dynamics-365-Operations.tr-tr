---
title: Banka yabancı para birimi yeniden değerleme işlemi
description: Bu konu, banka yabancı para birimi yeniden değerleme işlemine bir genel bakış sağlar. Kurulum, işlemi yürütme, işlem için hesaplama ve değerleme hareketlerinin tersine çevrilmesi hakkında bilgi içerir.
author: mikefalkner
manager: AnnBe
ms.date: 04/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4ec9814a4a35a1b3ba7ba05a04b53e5b150f4a04
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538644"
---
# <a name="bank-foreign-currency-revaluation"></a>Banka yabancı para birimi yeniden değerleme işlemi

[!include [banner](../includes/banner.md)]
[!include [preview-banner](../includes/preview-banner.md)]

Bu konu, banka yabancı para birimi yeniden değerleme işlemine bir genel bakış sağlar. İşlemi ayarlamayı ve yürütmeyi açıklar ve işlem için hesaplama hakkında bilgi sağlar. Tersine yeniden değerlendirme hareketlerini de açıklar, eğer tersine çevirme gerekliyse.

Dönem sonunun bir parçası olarak muhasebe uygulamaları farklı döviz kuru türleri (cari, geçmiş, ortalama vb.) kullanılarak yeniden değerlenen yabancı para birimlerinde banka hesabı bakiyelerini gerektirir. Banka yabancı para birimi yeniden değerleme özelliği, bir veya birden fazla banka hesabını yeniden değerlemede kullanılabilir. Bu özellik de bir genel özelliktir. Bu nedenle, tek bir sayfadan erişiminizin olduğu tüm tüzel varlıklardaki bankaları yeniden değerleyebilirsiniz.

> [!NOTE]
> Yeniden değerleme işlemini çalıştırdığınızda bir yabancı para birimine nakledilen her banka hesabındaki bakiye yeniden değerlenir. Yeniden değerleme işlemi sırasında oluşturulan gerçekleşmemiş kazanç veya zarar hareketleri sistem tarafından oluşturulur. Uygunsa, muhasebe para birimi için bir ve raporlama para birimi ilgiliyse raporlama para birimi için ikinci bir hareket oluşturulabilir. Her muhasebe girişi, gerçekleşmemiş kazanç veya zarar ve değerlendirilmekte olan ana muhasebe hesabına nakledilir.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme işlemini çalıştırmaya hazırlanma

Yeniden değerleme işlemini çalıştırmadan önce aşağıdaki kurulum gereklidir.

- **Genel muhasebe** sayfasından döviz kuru türünü belirleyin. Döviz kuru türü ana hesapta tanımlanmamışsa bu döviz kuru türü, yabancı para birimi yeniden değerleme işlemi sırasında kullanılır.
- **Genel muhasebe** sayfasında, para birimi yeniden değerleme işlemi için gerçekleşmiş kazanç, gerçekleşmiş kayıp, gerçekleşmemiş kazanç ve gerçekleşmemiş kayıp hesaplarını belirtin. Gerçekleşmiş kazanç ve gerçekleşmiş zarar hesapları, Alacak hesapları ve Borç hesapları hareketleri kapatıldığında kullanılır. Gerçekleşmemiş kazanç ve gerçekleşmemiş zarar hesapları, açık hesapları ve genel muhasebe ana hesaplarını yeniden değerlemekte kullanılır.
- **Para birimi yeniden değerleme hesapları** sayfasında, her bir para birimi ve şirket için farklı para birimi yeniden değerleme hesapları seçebilirsiniz. Hiçbir hesap tanımlanmazsa **Genel muhasebe** sayfasındaki hesaplar kullanılır.

## <a name="enable-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme işlemi etkinleştirme

Banka yabancı para birimi yeniden değerleme işlemi özelliğini, yabancı para birimi yeniden değerleme işlemlerini işlemeden önce açmanız gerekir.

1. **Nakit ve Banka yönetimi \> Kurulum \> Nakit ve Banka yönetim parametreleri**'ne gidin.
2. **Genel** sekmesinde, **yabancı para birimi yeniden değerleme işlemi** altında, **Banka yeniden değerlemesini etkinleştir** seçeneğini **Evet** olarak ayarlayarak geçerli tüzel varlık için özelliği açın. 
3. **Numara serileri** sekmesinde, yabancı para birimi yeniden değerleme işlemi için bir numara serisi ekleyin.
4. **Yabancı para birimi yeniden değerleme işlemi**'ni alan sayfasının **Periyodik görevler** sekmesinde görmek için tarayıcıyı yenileyin.

Yabancı para birimi yeniden değerleme işlemini kullanacak her tüzel kişilik için özelliği açmanız gerekir. Sistem Yöneticisi rolüne veya Özellik Yöneticisi rolüne atanırsanız **Özellik Yönetimi** çalışma alanındaki **Bir parametre olmadan banka yeniden değerlemeyi etkinleştir** adlı özelliği etkinleştirerek bu adımı giderebilirsiniz.

> [!NOTE]
> Tüzel varlığınız Rus, Polonya veya Macar ülke/bölge kodu kullanıyorsa, banka yabancı para birimi yeniden değerleme işlemini zaten yapabilirsiniz. Diğer ülkeler veya bölgelerde kullanılan yabancı para birimi yeniden değerlemeyi kullanamazsınız.

## <a name="process-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme işlemi gerçekleştirme

Kurulum tamamlandıktan sonra Nakit ve banka yönetimi içinde **yabancı para birimi yeniden değerleme işlemi** sayfasını kullanarak tüm tüzel varlıklardaki bir veya birden fazla banka hesabının bakiyelerini yeniden değerleyin. Süreci gerçek zamanlı olarak yürütebilir veya bir toplu işlem kullanarak yürütülmek üzere programlayabilirsiniz.

**Yabancı para birimi yeniden değerleme işlemi** sayfası, her bir yeniden değerleme işleminin geçmişini gösterir. Bu, işlemin ne zaman yürütüldüğünü ve hangi ölçütlerin tanımlandığını gösterir ve yeniden değerleme için oluşturulan fişe bağlantı sağlar. Önceki bir yeniden değerleme ters olup olmadığını gösterir. Yeniden değerleme işlemini yürütmek için **Yabancı para birimi yeniden değerleme işlemini** Eylem Panosu üzerinde **Banka - yabancı para birimi yeniden değerleme işlemi** iletişim kutusunu açın.

**Yeniden değerleme tarihi** alanı, yeniden değerlenecek yabancı para birimi bakiyesini hesaplamak için sonlandırma tarihini tanımlar. Bu tarihe kadar gerçekleşen tüm banka hareketlerinin toplamı yeniden değerlenir.

**Döviz kuru tarihi** alanı, para birimi bakiyelerini yeniden değerlemekte kullanılacak döviz kurunun tarihini tanımlar. Örneğin, bakiyeleri 31 Ocak tarihi itibariyle yeniden değerleyebilir ancak 1 Şubat için tanımlanmış döviz kurunu kullanabilirsiniz.

Yeniden değerleme işlemi bir veya daha fazla tüzel varlık için çalıştırılabilir. Bu arama, yalnızca erişiminiz olan tüzel varlıkları gösterir. Yabancı para birimi yeniden değerleme işlemi için uygun olan banka hesaplarını seçmek için tüzel varlıkları seçin. Bu tüzel varlıklar için tüm banka hesapları kılavuzda gösterilir.

Değerlemenin gözden geçirme sonuçlarını deftere nakletmeden önce görmek istiyorsanız **Deftere nakletmeden önce önizle** seçeneğini **Evet** olarak ayarlayın. Yabancı para birimi yeniden değerleme işlemi, deftere nakledilebilen bir önizlemeye sahiptir. Yeniden değerleme işlemini baştan çalıştırmanız gerekmez. Önizlemedeki sonuçları Microsoft Excel'e dışa aktararak tutarların nasıl hesaplandığına dair bir tarihçe tutabilirsiniz. Yeniden değerleme işleminin sonuçlarının önizlemesini görüntülemek istiyorsanız toplu işi kullanamazsınız.

Yabancı para birimi yeniden değerleme işlemini işlemek için **Tamam**'ı seçin. Her bir yürütmede geçmişi izlemek için bir kayıt oluşturulur. Her bir tüzel varlık ve deftere nakil katmanı için ayrı bir kayıt oluşturulur.

## <a name="calculate-unrealized-gainloss"></a>Gerçekleşmemiş kazancı/zararı hesaplama

Nakit ve banka yönetiminde, banka para birimi temel para birimi olarak değerlendirilir ve yeniden değerlenmez. Muhasebe para birimindeki banka hesabının bakiyesi, **Döviz kuru tarihi**'ndeki banka para birimi ve muhasebe para birimi arasındaki döviz kurları kullanılarak yeniden değerlenir. Raporlama para birimindeki banka hesabının bakiyesi, **Döviz kuru tarihi**'ndeki banka para birimi ve raporlama para birimi arasındaki döviz kurları da kullanılarak yeniden değerlenir.

Banka hesabının bakiyesi ve muhasebe para birimi için hesaplanan yeni bakiye arasındaki fark için yeni bir hareket oluşturulur. Banka hesabının bakiyesi ve raporlama para birimi için hesaplanan yeni bakiye arasındaki fark için başka bir hareket oluşturulur. Bu hareketler için girdiler mutabakat sağlama olarak işaretlenir. 

Banka para birimi muhasebe para birimiyle eşleşiyorsa, muhasebe para birimi için hiçbir giriş yapılmaz. Benzer şekilde, banka para birimi, raporlama para birimiyle eşleşiyorsa da hiçbir giriş yapılmaz.

Yabancı para birimi yeniden değerleme işlemi, banka hareketleri arasında bulunan boyutlar arasında da dağıtılır. Bölme, her bir boyut için bakiyeyi temel alır. Örneğin, toplam banka bakiyesi 10.000'dir ancak iş birimi 001 için bakiye 4.000'ken, iş birimi 002 için bakiye 6.000'dir. Bu durumda, yeniden değerleme tutarının yüzde 40'ı, iş birimi 001'i içeren yeniden değerleme hesabına nakledilir ve yüzde 60'ı iş birimi 002'ye sahip olan yeniden değerleme hesabına nakledilir. Hesap yapısı bir iş birimini içermiyorsa, tam tutar yeniden değerleme hesabına nakledilir.

## <a name="reverse-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme işlemini tersine çevir

Yeniden değerleme işlemi hareketini tersine çevirmeniz gerekiyorsa **Yabancı para birimi yeniden değerleme işlemi** sayfasında **Ters hareket** Eylem Panosunda seçin. Yeniden değerleme işlemi oluştuğunda veya tersine çevrildiğinde geçmiş hesap denetimi kılavuzunu düzenlemek için yeni bir yabancı para birimi yeniden değerleme işlemi geçmiş kaydı oluşturulur.

Birkaç yeniden değerlemeyi tersine çevirmek için en son yeniden değerleme ilk tersine çevirmeniz gerekir. Daha sonra, eski yeniden değerlemeleri tarih sırasında ters çevirmek için devam edin. Daha sonra tersine çevirdiğiniz dönemler için yeni yeniden değerlemeleri işleyebilirsiniz.
