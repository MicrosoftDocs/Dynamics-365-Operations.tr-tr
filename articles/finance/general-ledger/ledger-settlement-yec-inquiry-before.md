---
title: Sorgu sayfası kullanılarak, yıl sonu kapanışından önce genel muhasebe kapatma özelliği arasındaki tanıma
description: Bu makalede, Genel muhasebe yıl sonu kapanışı çalıştırıldıktan önce yeni sorgu sayfası kullanılarak genel muhasebe kapatmaları arasındaki algılamanın nasıl kullanılacağı açıklanır.
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
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853166"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>Sorgu sayfası kullanılarak, yıl sonu kapanışından önce genel muhasebe kapatma özelliği arasındaki tanıma

**Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliğindeki (**Farkındalık** özelliği) büyük bir değişiklik, genel muhasebe kapatılması mali yıllar arasında yapılamaz. Bu çapraz yıl sınırlaması yalnızca genel muhasebe kapanışıyla ilgilidir, Alacak hesaplarına veya Borç hesaplarına ait hesap kapatmalarını desteklemez.

**Farkındalık** özelliğini etkinleştirmeden önce, yıl sonu kapanışının üzerine gitmesi gereken mali yılın mali yıllara göre kapatılan genel muhasebe hareketleri olmamalıdır. Özellikle, mali yılda deftere nakledilen tüm hareketlerin, farklı bir mali yılda deftere nakledilen hareketlerden kapatılmamış olması gerekir. Hareketler, aynı mali yıl içindeki hareketlere göre yeniden kapatılabilir.

Bu makalede, mali yıl boyunca kapatılan genel muhasebe hareketlerini tanımlamak, kapatmak ve yeniden kapatmak için gerekli adımlar açıklanmaktadır. Sağlanan örnekte, 2021 mali yılı kapatılmıştır ve mali yıl 2022 yıl sonu kapanışını çalıştırmaya hazırlanıyorsunuz.

Microsoft Dynamics 365 Finance 10.0.29 itibariyle, genel muhasebe hareketlerini, mevcut yeni bir sorgulama sayfası kullanarak tanımlayabilir, geri alabilir ve yeniden uygulayabilirsiniz. Finance sürümü 10.0.29 veya daha ileri bir sürümde değilseniz, aşağıdaki makalelerde genel muhasebe hareketlerini tanımlama, kapatma ve yeniden kapatma adımlarını bulabilirsiniz:

- [Genel muhasebe kapatma özelliği ile yıl sonu öncesi kapanışı arasındaki farka duyarlılık](ledger-settle-yec.md)
- [Genel muhasebe kapatma özelliği ile yıl sonu sonrası kapanışı arasındaki farka duyarlılık](ledger-settle-yec-after.md)

Yeni sorgu penceresi hakkında daha fazla bilgi için bkz. [Kayıt defteri kapatma sorgusu](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Örnek kurulumu

Aşağıdaki şekilde, ana hesap 110200 için deftere nakledilen hareketler gösterilir. Yeşil renkteki hareketler, aynı mali yıl içinde genel muhasebede kapatılmıştır ve değiştirilmesi gerekmez. Kırmızı renkle yapılacak hareketler genel muhasebe ile kapatılmıştır, ancak hareket tarihleri farklı mali yıllara dahil edilir. Bu hareketler tanımlanmalıdır ve genel muhasebe kapanışının ters işlem yapılması gerekebilir.

![Deftere nakledilen genel muhasebe hareketleri.](./media/ledgersettlement.png)

## <a name="example"></a>Örnek

Kuruluşunuz mali yıl 2022 için yıl sonu kapanışını çalıştırdıktan önce **Farkındalık** özelliğini kullanmak isterse, bu adımları izleyin.

> [!NOTE]
> 2021 ve önceki mali yılların yıl sonu kapanışı, yalnızca mali yıl 2021 veya önceki sürümlerde yeni hareketler deftere nakledildiyse yeniden çalıştırılmalıdır. Aşağıdaki yordamı tamamladığınızda, 2021'ye hiçbir yeni hareket nakledilemez. Bu nedenle, yıl sonu kapatma işleminin yeniden çalıştırılması gerekmez.
>
> Mali yıllarda kapatılan genel muhasebe hareketleri, 2022 (kapatılan yıl) veya daha ileri bir sürümde deftere nakledilen bir harekete karşı kapatılmadığından, genel muhasebe kapatma olarak kalabilir. Örneğin, 2019 ve 2020 hareketlerini kapatmışsanız, bunlar kapatılmış durumda kalabilir.

1. **Farkındalık** özelliğini yeniden **etkinleştirmeyin**.
2. **Kayıt defteri kapatmaları** sayfasında **Yıllar arası kapatmayı incele**'yi seçin.
3. Diğer mali yıllara nakledilen, ancak 2022'e nakledilen hareketlere karşı kapatılan tüm hareketleri tanımlayın.

    1. Mali yıl 2022'ü seçin, yıl sonu kapanış süreci için çalıştırmak istediğiniz mali yıl.
    2. Genel muhasebe hesabı için görüntülemek istediğiniz mali boyutları göstermek üzere **Mali boyut kümesi** alanında bir değer seçin. Seçilen boyut kümesi bir ana hesap içermiyorsa dahi, ana hesap her zaman görüntülenir.
    3. **Hareketleri göster**'i seçin.

    Sorgulama sayfası, tüm genel muhasebe hesapları için (genel muhasebe kapatma kurulumunda artık olmasalar dahi), 2022'ye nakledilen hareketlere karşı kapatılan tüm diğer mali yıllara ait tüm hareketleri gösterir. Üç farklı genel muhasebe hesabı gösterilir.

    ![2022 yıllar arası kapatmalar.](./media/review-cross-year.png)

3. Kılavuzu seçin ve tutun (veya sağ tıklayın) ve sonra **Tüm satırları dışa aktar**'ı seçin. Bu satırlar, yıl sonu kapanışından sonra, 2022 içindeki hareketlerden kaldırılması gereken tüm hareketlerdir. Hareketleri daha sonra doğru şekilde yeniden kapatmak için ayrıntılı hareket listesi istiyorsunuz.
4. Hareketlerin deftere nakledildiği mali yılları kaydedin. Bu örnekte 2021 ve 2023 için hareketler vardır.
5. Sorgu sayfasında, 2022 harekete karşı kapatılan hareketleri içeren ilk mali yıl olan mali yılı 2021 olarak değiştirin.
6. **Hareket tarihi** sütununa filtre uygulamak için yalnızca 2022'ye nakledilen hareketler dahil edilir. Bu hareketler, 2022'de hareketlere karşı kapatılan 2021'den alınan ayrıntılı hareketlerdir.
7. Kılavuzu seçin ve tutun (veya sağ tıklayın) ve sonra **Tüm satırları dışa aktar**'ı seçin.

    > [!IMPORTANT]
    > Aşağıdaki adımlarda, bu hareketler kapatılamayacak ve 2022 içindeki hareketlere karşı yeniden kapatılacaktır. Bu ayrıntıyı Excel'de yapmanız gereklidir.

    ![2021 yıllar arası kapatmalar.](./media/review-cross-year.png)

8. Sorgu sayfasında, 2022 harekete karşı kapatılan hareketleri içeren sonraki mali yıl olan mali yılı 2023 olarak değiştirin. 
9. **Hareket tarihi** sütununa filtre uygulamak için yalnızca 2022'ye nakledilen hareketler dahil edilir. Bu hareketler, 2023'de hareketlere karşı kapatılan 2022'den alınan ayrıntılı hareketlerdir. 
10. Kılavuzu seçin ve tutun (veya sağ tıklayın) ve sonra **Tüm satırları dışa aktar**'ı seçin.

    > [!IMPORTANT]
    > Aşağıdaki adımlarda, bu hareketler kapatılamayacak ve 2022 içindeki hareketlere karşı yeniden kapatılacaktır. Bu ayrıntıyı Excel'de yapmanız gereklidir.

    ![2023 yıllar arası kapatmalar.](./media/filter-transactions.png)

11. 2022 içindeki hareketlere karşı kapatılan hareketler içeren her bir mali yıl için önceki adımları yineleyin. Ayrıntılı hareketleri her zaman Excel'e aktarın.

    2021 ve 2023'den ayrıntılı hareketlerin tümü Excel'e verildikten sonra, yeni sorgu sayfasını kullanarak hareketleri kapatmaya hazırsınız demektir.

12. Mali yılını 2022 olarak değiştirin.
13. Kılavuzdaki tüm kayıtları seçin ve sonra **İşaretli kayıtları tasfiye et**'i seçin. Kılavuzdaki tüm seçili hareketler tasfiye edilir.

    Hareketler kapatılmadan önce, hareket ayrıntılarının Excel'e aktarılmasını sağlamak için iki uyarı mesajı gösterilmektedir. Ayrıntıları Excel'e göndermeden önce genel muhasebe hareketlerini yanlışlıkla kapatmanız durumunda, kapatmanın geri çevrilme yolu yoktur.

    ![Çapraz kapatma hareketlerinin kapatılması geri alınıyor.](./media/revert-unsettle.png)

14. 2022'deki hareketler için kapatılan toplam 2021 ve 2023 hareketleri miktarını bulmak için Excel verilerini kullanın. Bu örnekte, 2021 toplam $525 hareketi ve 2023 toplam $700 hareketleri vardır.
15. 2022 için açılış bakiyesini iki tutara bölmek üzere bir düzeltme genel günlüğünü deftere nakledin: 2021 mali yılı ve henüz 2022 değiştirilmemiş olan bölüme göre kapatılan bölüm.

    - **Önceki yıla kapatılan açılış bakiyesi bölümü:** İlk tutar, 2021 ve 2022 genelinde kapatılan toplamlara göre ilk tutar $525'dür.
    - **Önceki yıla kapatılmayan açılış bakiyesinin bölümü:** İkinci tutar, açılış bakiyesi ile $525 kapatılan tutarı arasındaki farktır. Kalan tutar: $1025 – $525 = $500.

    Bu şekilde, 2022 hareket işlemini, başlangıçta 2021 harekete karşı kapatılan $525 karşı değiştirebilirsiniz. Genel muhasebe kapatma için kısmi kapatma yapılmasına izin vermediği için bu adım gereklidir.

    1. Yevmiye defterine gidin ve ayarlamayı deftere nakledin. Kuruluşunuz, açık olan dönemlere göre, hangi hareket tarihinin kullanılacağına karar vermeye çalışacaktır. Bu hareketler 2022 Ocak veya Şubat kapatma tarihi kullanılarak kapatılmış olabilir, ancak bu tek açık dönem ise ayarlamanın Aralık ayında deftere nakledilmesi gerekebilir.
    2. 110200 hesabı için **Ana hesap** sayfasında **El ile giriş yapma** parametresine izin verme özelliğini geçici olarak kapatmanız gerekebilir. Ana hesap el ile girişe izin vermiyorsa bu ayarlama deftere nakledilemez.

    ![Bir düzeltme yevmiye defterini deftere nakletme.](./media/not-post.png)

16. Kapatılmamış hareketleri yeniden tasfiye edebilirsiniz. **Genel muhasebe kapatma** sayfasına dönün, 110200 ana hesapta 1 Ocak 31 Aralık 2022 tarih aralığını belirtin ve filtre uygulayın. Sonra, yeniden kapatılması gereken belirli hareketleri bulmak için Excel'e dışa aktarılan ayrıntılı hareketleri kullanın. Aşağıdaki çizimde artık mevcut olan kapatılmamış hareketler gösterilir.

    ![Kapatılmamış hareketler.](./media/updated-unsettled.png)

    - $1.025 açılış bakiyesi, -$1.025 için ayarlamaya kapatılabilir.
    - -$400, -$50 ve -$75 için kapatılmış olan ayrıntılı hareketler, $25 ayarlamasına karşı kapatılabilir.

17. **Farkındalık** özelliğini etkinleştirin. Artık yıl sonu kapanışını çalıştırabilirsiniz.

    - Yıl sonu kapanışını çalıştırmadan önce, genel muhasebe kapatma kurulumundaki tüm bilanço hesapları için **Ayrıntıları koru** seçeneğini belirlemeyi düşünebilirsiniz. Daha fazla bilgi için bkz. [Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık](awareness-between-ledger-settlement-year-end-close.md).
    - 2022 için yıl sonu kapanışını başlattığınızda, hareketler hala mali yıllar içinde kapatılmış durumda ise, yıl sonu kapatma işlemi hemen size bildirir. Bu durum, önceki adımları tamamladıktan sonra mali yıllara ait hareketleri kapatılıyorsa ortaya çıkabilir.
    - 2021 ve 2022 hareketleri hala kapatılmışsa, **Farkındalık** özelliğini yeniden devre dışı bırakmanız ve daha sonra bu hareketlerin kapatılması için önceki adımları tekrarlamanız gerekir. Bu yaklaşım, 2021 kapalı olduğundan ve hareketler kapatılan mali yılda kapatılamayacak şekilde gereklidir.
    - 2022 ve 2023 hareketleri hala kapatılmışsa, **Farkındalık** özelliğini devre dışı bırakmanıza gerek yoktur. 2022 veya 2023 hiçbirisi kapanmadığı için, önceki adımları kullanarak hareketleri geri alabilirsiniz.

18. 2023'ten $700 hareketi, 2023'te açılış bakiyesi olarak devredilen ayrıntılı hareketlere karşı kapatabilirsiniz. Bu hareket, 2022 içindeki orijinal harekete göre kapatılmaz.

2022 için yıl sonu kapatma başarıyla çalıştırıldıktan sonra, **Farkındalık** özelliğini şimdi etkin durumda bırakabilirsiniz.
