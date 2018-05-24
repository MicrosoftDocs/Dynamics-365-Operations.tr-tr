---
title: "Döngü sayımı"
description: "Bu makalede, sayım döngüsünü Ambar yönetiminde bulunan ambar çözümü ile birlikte nasıl kullanabileceğiniz açıklanmaktadır. Bu makale, Stok yönetiminde bulunan ambar çözümü için geçerli değildir."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9da40e90982d9d4aca38890ed121782f4236712d
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="cycle-counting"></a>Döngü sayımı

[!include [banner](../includes/banner.md)]

Bu makalede, sayım döngüsünü Ambar yönetiminde bulunan ambar çözümü ile birlikte nasıl kullanabileceğiniz açıklanmaktadır. Bu makale, Stok yönetiminde bulunan ambar çözümü için geçerli değildir.

Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir. Döngü sayım işlemi üç adımda açıklanabilir:

1.  **Döngü sayım işi oluşturma** – Döngü sayım işi, maddeler için eşik parametrelerine dayalı olarak veya bir döngü sayım planı kullanılarak otomatik olarak oluşturulabilir. Alternatif olarak, **Maddeye göre döngü sayım işi** sayfası veya **Konuma göre döngü sayım işi** sayfasındaki madde veya ambar parametrelerini kullanarak döngü sayım işini el ile de oluşturabilirsiniz.
2.  **Döngü sayımını işleme** – Döngü sayım işi oluşturduktan sonra, döngü sayım işini bir ambar konumundaki maddeleri sayıp sonucu bir mobil cihaz kullanarak Microsoft Dynamics 365 for Finance and Operations'a girerek gerçekleştirirsiniz. Alternatif olarak, döngü sayım işi oluşturmadan bir ambar konumundaki maddeleri sayabilirsiniz. Bu süreç, *nokta döngü sayımı* olarak bilinmektedir.
3.  **Sayılan değerdeki farkları düzeltme** – Bir döngü sayımından sonra, sayılan değerde farklılık olan tüm maddeler **Tüm işler** sayfasında **Gözden geçirilmeyi bekliyor** şeklinde bir iş durumuna sahip olacaktır. Bu farkları **Gözden geçirilmeyi bekleyen döngü sayım işi** sayfasında düzeltebilirsiniz.

Aşağıdaki çizimde döngü sayım işlemi gösterilmiştir. ![Döngü sayımı için süreç akışı](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Döngü sayım öngereklilikleri
Aşağıdaki tabloda, döngü sayımını kullanmadan önce yerine getirilmesi gereken öngereklilikler gösterilmiştir.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Madde</td>
<td>Madde mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir.</td>
</tr>
<tr class="even">
<td>Ambar</td>
<td>Ambar mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir. Ambarı ambar yönetim süreçleri için etkinleştirmek üzere, <strong>Ambarlar</strong> sayfasında ambarı seçin, ardından <strong>Ambar yönetim süreçlerini kullan</strong> seçeneğini belirleyin. Bir döngü sayımı sırasında işçilerin paletleri taşımasına imkan vermek için, <strong>Ambar yönetimi</strong> FastTab'inde <strong>Paletlerin döngü sayımı sırasında taşınmasına izin ver</strong> seçeneğini belirleyin.</td>
</tr>
<tr class="odd">
<td>İş havuzları</td>
<td>İsteğe bağlı: Ambar işini iş türüne göre ayrıştırmak için bir iş havuzu oluşturun (bu durumda, döngü sayım işi).</td>
</tr>
<tr class="even">
<td>Konumlar</td>
<td>Konumlar için döngü sayımını etkinleştirin. Bir ambar konumu için döngü sayımına izin vermek üzere, <strong>Konum profilleri</strong> sayfasında <strong>Döngü sayımına izin ver</strong> seçeneğini belirleyin.</td>
</tr>
<tr class="odd">
<td>Ambar yönetim parametreleri</td>
<td>Döngü sayımı için parametreleri ayarlayın. <strong>Ambar yönetim parametreleri</strong> sayfasında, döngü sayımı için varsayılan ayar türü kodunu, iş sınıfı kimliğini ve iş önceliğini belirleyin.</td>
</tr>
<tr class="even">
<td>Mobil cihaz</td>
<td><ul>
<li>Aşağıdaki yöntemlerden biri için <strong>Mobil cihaz menü öğeleri</strong> sayfasında bir menü öğesi oluşturun:
<ul>
<li>Kullanıcı tarafından yönlendirilen döngü sayımı</li>
<li>Sistem tarafından yönlendirilen döngü sayımı</li>
<li>Döngü sayımı gruplandırma</li>
<li>Nokta döngü sayımı</li>
</ul>
</li>
<li>Mobil aygıt için bir menü oluşturun.</li>
<li>Bir iş kullanıcı hesabı oluşturun ve iş kullanıcı kimliğine bir mobil cihaz menüsü atayın.</li>
</ul></td>
</tr>
<tr class="odd">
<td>İlgili kurulum görevi</td>
<td>Bir ambar konumu için bir döngü sayımı planı oluşturun.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Döngü sayım işini otomatik olarak oluşturma
Döngü sayım işinin tekrarlı oluşturulmasının iki yolu vardır: döngü sayım eşikleri ayarlama veya döngü sayım planları ayarlama.

-   Bir döngü sayımı eşiği stok maddelerinin miktar veya yüzde sınırını belirtir. Döngü sayımı işi, eşik sınırına ulaşıldığında otomatik olarak oluşturulur.
-   Bir döngü sayım planı, döngü sayım işini ya hemen ya da bir toplu iş üzerinden periyodik olarak oluşturur. Döngü sayım işi oluşturulduğunda, sayım iş satırı sayılacak konum hakkında bilgi içerir. Bu konumla ilişkilendirilmiş olan eldeki stok durdurulmuş değil ve dolayısıyla açık sayım işi mevcut olsa bile rezervasyona ve giden işleme uygun.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Maddeler için eşik parametrelerine dayalı olarak döngü sayım işi oluşturma

Döngü sayım işi, bir konumdaki madde sayısının belirli bir eşik değerinin altına düşmesi durumunda oluşturulabilir. Örneğin, döngü sayımı eşiği 40 olan bir konumda 60 öğe vardır. Bir satış siparişi hareketi sırasında, 25 öğe konumdan alınır ve bir hazırlama konumuna koyulur. 35 olan yeni madde sayısı, eşik miktarından az olduğundan döngü sayım işi bu konum için otomatik olarak oluşturulur.

### <a name="schedule-cycle-counting-work"></a>Döngü sayım işi planlama

Hemen veya periyodik olarak döngü sayım işi oluşturmak için döngü sayım planları yapabilirsiniz. Döngü sayım planları ayarlayarak, döngü sayım işinin oluşturulduğu iş havuzunu, farklı konumlardaki maddeler için oluşturulan döngü sayımlarının maksimum sayısını ve bir ambar konumu yeniden sayılmadan önce geçecek gün sayısını kontrol edebilirsiniz. Örneğin, bir madde ambarda üç konumda mevcut ve maksimum döngü sayımı sayısı **2** olarak ayarlı. Bu durumda, döngü sayımı planını çalıştırdığınızda iki döngü sayımı maddenin mevcut olduğu iki konum için oluşturulur. Başka bir örnek olarak, döngü sayımları arasındaki gün sayısını **5** olarak ayarlarsınız. Bu durumda, her beş günde bir döngü sayım işi oluşturulur. Ancak, döngü sayım işi üçüncü günde işleniyorsa, bir sonraki döngü sayım işi son döngü sayımı işlendikten beş gün sonra, sekizinci gün içinde oluşturulur.

## <a name="create-cycle-counting-work-manually"></a>Döngü sayım işini manuel olarak oluşturma
Döngü sayım işini el ile oluşturmak için, **Maddeye göre döngü sayım işi** veya **Konuma göre döngü sayım işi** sayfasını kullanabilirsiniz. Oluşturulacak maksimum döngü sayımı sayısını belirleyebilirsiniz. Örneğin ambar yöneticisi değeri **5** olarak belirlerse, madde 10 konumda olsa bile döngü sayım işi beş konum için oluşturulur. Oluşturulan döngü sayım işi kimliklerinin atandığı bir iş havuzu kimliği de seçebilirsiniz. Döngü sayımı için bir iş havuzu kimliği işlendiğinde, iş havuzuna atanan döngü sayım işi kimlikleri grup olarak işlenir.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Mobil cihaz kullanarak döngü sayımı gerçekleştirme
Bir mobil cihazda Dynamics 365 for Finance and Operations kullanarak döngü sayım işi işlemenin birçok yöntemi vardır:

-   **Kullanıcı yönlendirmeli** – İşçi, **Açık** durumuna sahip bir döngü sayım işi kimliği belirtebilir.
-   **Sistem yönlendirmesinde** – Finance and Operations işçiye bir döngü sayım işi kimliği atar.
-   **Döngü sayım gruplaması** – İşçi, belirli bir konuma, bölgeye veya iş havuzuna özgü döngü sayım işi kimliklerini gruplandırabilir.
-   **Nokta döngü sayımı** – İşçi, bir ambar konumundaki maddeleri döngü sayım işi oluşturmaksızın her zaman sayabilir. Bir konumda nokta döngü sayımı gerçekleştirmek için işçi konum kimliğini girer.

Aşağıdaki örneklerde, nokta döngü sayımını mobil cihaz kullanarak nasıl gerçekleştirebileceğiniz gösterilmektedir. İşçinin cihazda gördüğü yönergeler, nokta döngü sayımına yönelik menünün kurulumuna bağlı olarak değişebilir.

1.  Mobil aygıtta, nokta döngü sayım işini yürütmek için menü öğesini seçin.
2.  Nokta döngü sayımı gerçekleştirilecek konumu kaydettirin.
3.  Madde numarasını ve sayılan madde miktarını kaydettirin ve doğrulayın. **Not:** Döngü sayım işinin durumu **İşçi** sayfasında ayarlı parametrelere bağlı olarak **Tüm iş** sayfasında **Gözden geçirilmeyi bekliyor** ya da **Kapalı** olarak güncellenir.
4.  İsteğe bağlı: 3. adımı konumda kalan maddeler için tekrarlayın ve sayım için başka madde kalmadığını kontrol edin.

## <a name="resolve-cycle-counting-differences"></a>Döngü sayım farklarını düzeltme
Aşağıdaki senaryolarda, bir iş kullanıcısı kimliği için **Bir döngü sayım denetimi** seçeneği **Hayır** olarak ayarlı ise bir döngü sayım farkı ortaya çıkar:

-   Sayılan değer **İş kullanıcıları** sayfasındaki **Maksimum yüzde sınırı** veya **Maksimum miktar sınırı** alanlarında belirtilen sapma sınırları dahilinde değilse. Örneğin, bir konumdaki eldeki stok miktarı 50'dir ve iş kullanıcısı için sapma sınırı 10'dur. İş kullanıcısı, 40 ile 60 arasında olmayan bir değer girdiğinde, bir fark ortaya çıkar.
-   Sayılan döngü değeri, eldeki stok miktarından farklı olur ve ayarlanmış sapma sınırları yoktur.

Sayılan değerdeki farkları düzeltebilir ve ardından sayılan değeri **Gözden geçirilmeyi bekleyen döngü sayımı** sayfasında kabul edebilirsiniz. Madde miktarının değiştirilen sayısını **Konuma göre eldeki** sayfasında doğrulayabilirsiniz. Fark onaylanamıyorsa, sayılan değer reddedilir.

## <a name="additional-resources"></a>Ek kaynaklar
[Ambar işi için mobil cihazları yapılandırma](configure-mobile-devices-warehouse.md)




