---
title: Gelir kabulü yeniden tahsisatı - Senaryo 2
description: Bu konu, iki satış siparişinin girildiği ve ilk satış siparişi faturalandıktan sonra müşterinin sözleşmeye bir madde eklediği yeniden tahsisat senaryosunu ele alır. Bir sözleşmeye yeni bir madde eklendiğinde, yeni bir satış siparişine ya da var olan satış siparişine eklenebilir.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1fe195f171e8e343e9ce01b2ca0d4980d193a6fd3d9aa6f95efed66a29aa7d6d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770701"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Gelir kabulü yeniden tahsisatı – Senaryo 2

[!include [banner](../includes/banner.md)]

Bu konu, iki satış siparişinin girildiği ve ilk satış siparişi faturalandıktan sonra müşterinin sözleşmeye bir madde eklediği yeniden tahsisat senaryosunu ele alır. Bir sözleşmeye yeni bir madde eklendiğinde, yeni bir satış siparişine ya da var olan satış siparişine eklenebilir.

Bu senaryoda **Genel muhasebe parametreleri** sayfasının (**Gelir kabulü \> Kurulum \> Genel muhasebe parametreleri**) **Gelir kabulü** sekmesinde **Fatura düzeltmelerini Alacak hesaplarına naklet** seçeneği **Hayır** olarak ayarlanmıştır.

[![Fatura düzeltmelerini Alacak hesaplarına deftere naklet seçeneği Hayır olarak ayarlı.](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

US\_SI\_0003 müşterisi için bir satış siparişi oluşturulur. Müşteri yükleme hizmetleri (madde numarası S0001) ve dizüstü bilgisayar destek planı (madde numarası S0008) satın almaktadır ancak henüz dizüstü bilgisayarı seçmemiştir. Yükleme hizmetlerinin geliri, dizüstü bilgisayarın satın alınacağı tarihe kadar ertelenir. Destek planının geliri, sözleşmedeki tarih aralığında tanımlandığı şekilde ertelenir ve 12 ay içinde kabul edilir.

[![Yükleme hizmetleri ve destek planı için satış siparişi satırları.](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Satış siparişi onaylanır. Gelir fiyatı tahsisatı için her iki madde ayarlandığından, satış siparişi onaylandığında gelir fiyatı hesaplanır. Kabul edilecek geliri **Gelir fiyatı tahsisatı** sayfasında görüntüleyebilirsiniz (**Satış siparişi** sayfasında, Eylem bölmesi, **Yönet** sekmesi, **Gelir kabulü** grubunda, **Gelir fiyatı tahsisatı**'nı seçin). Yükleme hizmetleri geliri Ertelenmiş gelir hesabına 250,00 dolar olarak nakledilir. Destek planı geliri de Ertelenmiş gelir hesabına 150,00 dolar olarak nakledilir. Gelir fiyatlarının toplamı, gelir fiyatı tahsisatı (400,00 dolar) yakalamak için ayarlanan satırların toplamına eşit olmalıdır.

[![Gelir fiyatı tahsisatı sayfası.](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Satış siparişi tamamen faturalanmıştır. Aşağıdaki şekilde, fatura için deftere nakledilen muhasebe girişi gösterilmektedir.

[![Tamamen faturalanan satış siparişi için muhasebe girişi.](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Gelir kabulü planı da oluşturulur ancak henüz hiçbir gelir kabul edilmemiştir.

[![Gelir kabulü planı sayfası.](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Birkaç gün sonra, müşteri bir dizüstü bilgisayar seçer. Müşteri için ikinci bir satış siparişi girilir.

[![Dizüstü bilgisayar için satış siparişi satırı.](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

İkinci satış siparişi onaylanır. Bu satış siparişi yalnızca bir satır içerdiğinden, satış siparişi onaylandığında gelir fiyatı tahsisatı yapılmaz. Gelir fiyatı tahsisatı, yalnızca iki veya daha fazla benzersiz madde olduğunda ve bu maddeler gelir fiyatı tahsisatı için ayarlanmışsa gerçekleştirilir.

Bu yeni satış siparişi müşterinin sözleşmesinde yapılan tek değişiklik ise yeniden tahsisat işlemi çalıştırılabilir. İki satış siparişinden birinde, **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'i seçerek **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et** sayfasını açın. Alternatif olarak **Gelir kabulü \> Periyodik görevler \> Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'e gidin. İki satış siparişini ve karşılık gelen satış siparişi satırlarını seçin ve **Yeniden tahsisatı güncelleştir**'i seçin. **Yeniden tahsis edilen tutar** sütunu, her satış siparişi satırının yeni gelir fiyatını gösterir.

[![Fiyatı yeni sipariş satırlarıyla yeniden tahsis et sayfasındaki yeni gelir fiyatları.](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Ardından, yalnızca Genel muhasebeye nakledilecek olan muhasebe girişlerini görüntülemek için **Beklenen fiş** seçeneğini belirleyin. **Fatura düzeltmelerini Alacak hesaplarına naklet** seçeneği, **Genel muhasebe parametreleri** sayfasında **Hayır** olarak ayarlandığından, yeniden tahsisat işlemi yapıldığında Alacak hesaplarında hiçbir değişiklik yapılmaz.

[![Beklenen fiş sayfasındaki muhasebe girişleri.](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

**Beklenen fiş** sayfasında, son üç satır deftere nakledilen faturadaki özgün muhasebe girişini tersine çevirir. İlk dört satır, fatura için deftere nakledilen yeni muhasebe girişini oluşturur. Müşteriye yeni bir fatura sunulmayacağını lütfen unutmayın. Yeniden tahsisat tamamlandıktan sonra, müşteri halen 426,00 dolar borçludur. Bu miktar, yeni muhasebe girişinde Alacak hesaplarına nakledilmesi gereken tutardır. Mahsup edilen vergi ve ertelenen gelir eşittir 188,69 dolar + 314,48 dolar + 26,00 = 529,17 dolar. Ertelenen gelir tutarı yeniden tahsisat nedeniyle değişmiştir. 103,17 dolarlık fark, Kısmi fatura geliri kliring hesabı defterine nakledilir. Fatura yeniden tahsisata dahil edilen ikinci satış siparişi için deftere nakledildiğinde, bu bakiye temizlenecektir.

Yeniden tahsisatı tamamlamak için **İşlem**'i seçin. Deftere hiçbir şey deftere nakledilmemiş olsa bile bir deftere nakil tarihi sorulur. Yeniden tahsisat tamamlandıktan sonra, her satış siparişi için **Gelir fiyatı tahsisatı** sayfası, her iki satış siparişindeki tüm maddelerin fiyat tahsisatını gösterir. Başka bir deyişle, aynı sözleşmenin bir parçası olmasına rağmen farklı bir satış siparişinde olduğundan, her satış siparişinin **Gelir fiyatı tahsisatı** sayfası o satış siparişinde bulunmayan bir madde içerir.

> [!TIP]
> Bu ek maddelerin neden gösterildiğiyle ilgili bağlam sağlamak için kılavuza **Yeniden tahsisat kodu** ve **Satış siparişi** gibi başka sütunlar ekleyebilirsiniz.
> 
> [![Gelir fiyatı tahsisatları sayfasındaki ek sütunlar.](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

00036 numaralı satış siparişinde, gelir kabulü planı da yeni gelir yeniden tahsisat fiyatına göre güncelleştirilmiştir. Bu satış siparişinde, **Gelir kabulü planı** sayfasını açın. Daha önce, madde S0008 için 13 satır bulunuyordu (bu maddeye 12 aylık bir çizelge atanmıştır). Artık 39 satır vardır: 13 özgün çizelge satırı, 13 ters işlem çizelgesi satırı ve yeni gelir fiyatını temel alan 13 satır.

[![S0008 maddesi için 39 satırla güncelleştirilmiş gelir kabulü planı sayfası.](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Benzer şekilde, madde S0001 için daha önce iki satır vardı ancak artık altı satır bulunuyor.

[![S0001 maddesi için altı satırla güncelleştirilmiş gelir kabulü planı sayfası.](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

000036 numaralı satış siparişinde **Fiş**'i seçtiğinizde, fatura günlüğü özgün muhasebe girişini gösterir. Ters işlem girişini ve satış siparişindeki yeni muhasebe girişini görüntülemek için Eylem Bölmesinde **Gelir ayarlamaları**'nı ve ardından **Fiş**'i seçin.

[![000036 numaralı satış siparişi.](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Daha sonra, **Tüm müşteriler** sayfasını açın (**Alacak hesapları \> Müşteriler \> Tüm müşteriler**), **US\_SI\_0003** müşterisini ve ardından **Hareketler**'i seçin. 000036 numaralı satış siparişinin açık faturası gösterilir. Fişi seçerseniz yeniden tahsisat için yeni muhasebe girişini değil, orijinal muhasebe girişini görürsünüz. Ters işlem girişi ve yeni muhasebe girişi, Alacak hesaplarından görüntülenemez.

İkinci satış siparişi artık faturalandırılır. Müşteriye sunulan toplam fatura 1099,00 dolar + 71,44 dolar vergi = 1170,44 dolar olur. Aşağıdaki şekilde, deftere nakledilen muhasebe girişi gösterilmektedir.

[![Deftere nakledilen muhasebe girişini içeren fiş hareketleri sayfası.](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Gelir ve satışın toplamı 1170,44 dolardan fazla olduğundan, -130,17 dolarlık fark deftere nakledilir. Bu tutar, Kısmi fatura geliri kliring hesabındaki bakiyeyi kapatır. Bu bakiye, yeniden tahsisat işleminden sonra yeni muhasebe girişinde deftere nakledilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]