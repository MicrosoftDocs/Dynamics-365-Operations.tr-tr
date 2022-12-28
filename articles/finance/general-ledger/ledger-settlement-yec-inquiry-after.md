---
title: Sorgu sayfası kullanılarak, yıl sonu kapanışından sonra genel muhasebe kapatma özelliği arasındaki tanıma
description: Bu makalede, Genel muhasebe yıl sonu kapanışı çalıştırıldıktan sonra yeni sorgu sayfası kullanılarak genel muhasebe kapatmaları arasındaki algılamanın nasıl kullanılacağı açıklanır.
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 921d2a17409ae10cd9c22eeca11557ba1248b9bc
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853149"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close-using-the-inquiry-page"></a>Sorgu sayfası kullanılarak, yıl sonu kapanışından sonra genel muhasebe kapatma özelliği arasındaki tanıma

**Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliğindeki (**Farkındalık** özelliği) büyük bir değişiklik, genel muhasebe kapatılması mali yıllar arasında yapılamaz. Bu çapraz yıl sınırlaması yalnızca genel muhasebe kapanışıyla ilgilidir, Alacak hesaplarına veya Borç hesaplarına ait hesap kapatmalarını desteklemez.

**Farkındalık** özelliğini etkinleştirmeden önce, yıl sonu kapanışının üzerine gitmesi gereken mali yılın mali yıllara göre kapatılan genel muhasebe hareketleri olmamalıdır. Özellikle, mali yılda deftere nakledilen tüm hareketlerin, farklı bir mali yılda deftere nakledilen hareketlerden kapatılmamış olması gerekir. Hareketler, aynı mali yıl içindeki hareketlere göre yeniden kapatılabilir.

Bu makalede, yıl boyunca kapatılan genel muhasebe hareketlerini tanımlamak, kapatmak ve yeniden kapatmak için gerekli adımlar açıklanır. Sağlanan örnekte, 2022 mali yılı kapatılmıştır. Odak, 2023 yıl sonu kapanışı çalıştırılmadan önce genel muhasebe kapatma hareketlerini hazırlamaktır.

Microsoft Dynamics 365 Finance 10.0.29 itibariyle, genel muhasebe hareketlerini, mevcut yeni bir sorgulama sayfası kullanarak tanımlayabilir, geri alabilir ve yeniden uygulayabilirsiniz. Microsoft Dynamics 365 Finance sürümü 10.0.29 veya daha ileri bir sürümde değilseniz, aşağıdaki makalelerde genel muhasebe hareketlerini tanımlama, kapatma ve yeniden kapatma adımlarını bulabilirsiniz:

- [Genel muhasebe kapatma özelliği ile yıl sonu öncesi kapanışı arasındaki farka duyarlılık](ledger-settle-yec.md)
- [Genel muhasebe kapatma özelliği ile yıl sonu sonrası kapanışı arasındaki farka duyarlılık](ledger-settle-yec-after.md)

Yeni sorgu penceresi hakkında daha fazla bilgi için bkz. [Kayıt defteri kapatma sorgusu](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Örnek kurulumu

Aşağıdaki şekilde, ana hesap 110200 için deftere nakledilen hareketler gösterilir. Yeşil renkteki hareketler, aynı mali yıl içinde genel muhasebede kapatılmıştır ve değiştirilmesi gerekmez. Kırmızı renkle yapılacak hareketler genel muhasebe ile kapatılmıştır, ancak hareket tarihleri farklı mali yıllara dahil edilir. Bu hareketler tanımlanmalıdır ve genel muhasebe kapanışının ters işlem yapılması gerekebilir.

![Deftere nakledilen genel muhasebe hareketleri.](./media/excel.png)

## <a name="example"></a>Örnek

Kuruluşunuz mali yıl 2022 için yıl sonu kapanışını çalıştırdıktan sonra **Farkındalık** özelliğini kullanmak isterse, bu adımları izleyin.

> [!NOTE]
> 2022 ve önceki mali yılların yıl sonu kapanışı, yalnızca mali yıl 2022 veya önceki sürümlerde yeni hareketler deftere nakledildiyse yeniden çalıştırılmalıdır. Aşağıdaki yordamı tamamladığınızda, 2022'ye hiçbir yeni hareket nakledilemez. Bu nedenle, yıl sonu kapatma işleminin yeniden çalıştırılması gerekmez.
>
> Mali yıllarda kapatılan genel muhasebe hareketleri, 2022 veya daha ileri bir sürümde deftere nakledilen bir harekete karşı kapatılmadığından, genel muhasebe kapatma olarak kalabilir. Örneğin, 2019 ve 2020 hareketlerini kapatmışsanız, bunlar kapatılmış durumda kalabilir.

1. **Farkındalık** özelliği etkin olmadan 2022 için yıl sonu kapanışını tamamlayın.
2. Diğer mali yıllara nakledilen, ancak 2023'e nakledilen hareketlere (kapatılacak bir sonraki mali yıl) karşı kapatılan tüm hareketleri tanımlayın.

    > [!NOTE]
    > 2022 hareketlerine karşı kapatılan 2021 hareketleri, 2022 için yıl zaten kapalı olduğundan ilgili değildir. Bu hareketler kapalı kalabilir.

    1. **Kayıt defteri kapatmaları** sayfasında **Yıllar arası kapatmayı incele**'yi seçin.
    2. Mali yıl 2023'ü seçin, yıl sonu kapanış süreci için çalıştırmak istediğiniz sonraki mali yıl.
    3. Genel muhasebe hesabı için görüntülemek istediğiniz mali boyutları göstermek üzere **Mali boyut kümesi** alanında bir değer seçin. Seçilen boyut kümesi bir ana hesap içermiyorsa dahi, ana hesap her zaman görüntülenir.
    4. **Hareketleri göster**'i seçin.

    Sorgulama sayfası, 2023 deftere nakledilen hareketlere karşı kapatılan diğer mali yıllardaki tüm hareketleri gösterir.

    ![2023 yıllar arası kapatmalar.](./media/2023-cross-settlement.png)

3. Kılavuzu seçin ve tutun (veya sağ tıklayın) ve sonra **Tüm satırları dışa aktar**'ı seçin. Bu satırlar, sonraki yılın yıl sonu kapanışından (2023) sonra, 2022 içindeki hareketlerden kaldırılması gereken tüm hareketlerdir. Bu hareketlerin bir kaydı olmasını istiyorsunuz.

    2022'den ayrıntılı hareketlerin tümü Excel'e verildikten sonra, sorgu sayfasını kullanarak hareketleri kapatmaya hazırsınız demektir.

4. Kılavuzdaki tüm kayıtları seçin ve sonra **İşaretli kayıtları tasfiye et**'i seçin. Kılavuzdaki tüm seçili hareketler tasfiye edilir.

    Hareketler kapatılmadan önce, hareket ayrıntılarının Excel'e aktarılmasını sağlamak için iki uyarı mesajı gösterilmektedir. Ayrıntıları Excel'e göndermeden önce genel muhasebe hareketlerini yanlışlıkla kapatmanız durumunda, kapatmanın geri çevrilme yolu yoktur.

    ![Yıllar arası kapatmaları tasfiye edin.](./media/revert-settlement.png)

5. 2023'teki hareketler için kapatılan toplam 2022 hareketleri miktarını bulmak için Excel verilerini kullanın. Bu örnekte, 2023 için olan hareketler toplamı $700'dür.
6. 2022 için açılış bakiyesini iki tutara bölmek üzere bir düzeltme genel günlüğünü deftere nakledin: 2022 mali yılı harekete ve henüz 2023 değiştirilmemiş olan bölüme göre kapatılan bölüm.

    - **Önceki yıla kapatılan açılış bakiyesi bölümü:** İlk tutar, 2021 ve 2022 genelinde kapatılan toplamlara göre ilk tutar $700'dür.
    - **Önceki yıla kapatılmayan açılış bakiyesinin bölümü:** İkinci tutar, açılış bakiyesi ile $700 kapatılan tutarı arasındaki farktır. Kalan tutar: $1.700 – $700 = $1.000.

    Bu şekilde, 2023 hareket işlemini, başlangıçta 2022 harekete karşı kapatılan $700 karşı değiştirebilirsiniz. Genel muhasebe kapatma için kısmi kapatma yapılmasına izin vermediği için bu adım gereklidir.

    1. Yevmiye defterine gidin ve ayarlamayı deftere nakledin. Kuruluşunuz, 2023'te açık olan dönemlere göre, hangi hareket tarihinin kullanılacağına karar vermeye çalışacaktır.
    2. **Ana hesap** sayfasında **El ile giriş yapma** parametresine izin verme özelliğini geçici olarak kapatmanız gerekebilir. Ana hesap el ile girişe izin vermiyorsa bu ayarlama deftere nakledilemez.

    ![Bir düzeltme yevmiye defterini deftere nakletme.](./media/no-manual4.png)

7. Kapatılmamış hareketleri yeniden tasfiye edebilirsiniz. **Genel muhasebe kapatma** sayfasına dön ve tarih aralığını 1 Ocak 31 Aralık 2023 olarak sınırlayın. Sonra, yeniden kapatılması gereken belirli hareketleri bulmak için Excel'e dışa aktarılan ayrıntılı hareketleri kullanın. Aşağıdaki çizimde artık mevcut olan kapatılmamış hareketler gösterilir.

    ![2023 Kapatılmamış hareketler.](./media/2023-unsettled5.png)

    - $1.700 açılış bakiyesi, -$1.700 için ayarlamaya kapatılabilir.
    - -$700 için kapatılmış olan ayrıntılı hareketler, $700,00 ayarlamasına karşı kapatılabilir.

8. **Farkındalık** özelliğini etkinleştirin. Artık yıl sonu kapanışını çalıştırabilirsiniz.

    - 2023 için yıl sonu kapanışını çalıştırmadan önce, genel muhasebe kapatma kurulumundaki tüm bilanço hesapları için **Ayrıntıları koru** seçeneğini belirlemeyi düşünebilirsiniz. Daha fazla bilgi için bkz. [Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık](awareness-between-ledger-settlement-year-end-close.md).
    - 2023 için yıl sonu kapanışını başlattığınızda, hareketler hala mali yıllar içinde kapatılmış durumda ise, yıl sonu kapatma işlemi hemen size bildirir. Bu durum, kullanıcılar **Farkındalık** özelliği etkinleştirilmeden önce mali yıllara ait hareketleri kapatılıyorsa ortaya çıkabilir.
    - 2022 ve 2023 hareketleri hala kapatılmışsa, **Farkındalık** özelliğini yeniden devre dışı bırakmanız ve daha sonra bu hareketlerin kapatılması için önceki adımları tekrarlamanız gerekir. Bu yaklaşım, 2022 kapalı olduğundan ve hareketler kapatılan mali yılda kapatılamayacak şekilde gereklidir.

2022 için yıl sonu kapatma başarıyla çalıştırıldıktan sonra, **Farkındalık** özelliğini şimdi etkin durumda bırakabilirsiniz.
