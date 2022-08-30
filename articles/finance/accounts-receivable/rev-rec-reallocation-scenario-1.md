---
title: Gelir kabulü yeniden tahsisatı - Senaryo 1
description: Bu makalede, iki satış siparişinin girildiği ancak yalnızca onaylandığı bir yeniden tahsisat senaryosu ele alınmaktadır. İkiden fazla satış siparişi onaylanmış durumdaysa aynı senaryo benzer sonuçlar doğurur.
author: bking
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 92af49d9446fd9ed3310d8d0d50af902e7a7e693
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348340"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Gelir kabulü yeniden tahsisatı – Senaryo 1

[!include [banner](../includes/banner.md)]

Bu makalede, iki satış siparişinin girildiği ancak yalnızca onaylandığı bir yeniden tahsisat senaryosu ele alınmaktadır. İkiden fazla satış siparişi onaylanmış durumdaysa aynı senaryo benzer sonuçlar doğurur.

Bu senaryoda **Genel muhasebe parametreleri** sayfasının (**Gelir kabulü \> Kurulum \> Genel muhasebe parametreleri**) **Gelir kabulü** sekmesinde **Fatura düzeltmelerini Alacak hesaplarına naklet** seçeneği **Hayır** olarak ayarlanmıştır.

[![Fatura düzeltmelerini Alacak hesaplarına deftere naklet seçeneği Hayır olarak ayarlı.](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

US\_SI\_0003 müşterisi için bir satış siparişi oluşturulur. Müşteri bir dizüstü bilgisayar (madde numarası S0012) ve destek planı (madde numarası S0008, "Sürekli Mühendislik Hizmeti") satın alır. Dizüstü bilgisayarın geliri hemen kabul edilir (gelir kabulü planı yoktur). Destek planının geliri, sözleşmedeki tarih aralığında tanımlandığı şekilde ertelenir ve 12 ay içinde kabul edilir.

[![Dizüstü bilgisayar ve destek planı için satış siparişi satırları.](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Satış siparişi onaylanır. Gelir fiyatı tahsisatı için her iki madde ayarlandığından, satış siparişi onaylandığında gelir fiyatı hesaplanır. Kabul edilecek geliri **Gelir fiyatı tahsisatı** sayfasında görüntüleyebilirsiniz (**Satış siparişi** sayfasında, Eylem bölmesi, **Yönet** sekmesi, **Gelir kabulü** grubunda, **Gelir fiyatı tahsisatı**'nı seçin). Dizüstü bilgisayar için gelir, Gelir hesabına 1008,01 dolar olarak nakledilir. Destek planı geliri Ertelenmiş gelir hesabına 190,99 dolar olarak nakledilir. Gelir fiyatlarının toplamı, gelir fiyatı tahsisatı (1.199,00 dolar) yakalamak için ayarlanan satırların toplamına eşit olmalıdır.

[![Gelir fiyatı tahsisatı sayfası.](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Müşteri, satış anında yükleme hizmetlerini (madde numarası S0001) satın almamayı seçmiştir ancak daha sonra fikir değiştirmiştir. Bu nedenle, aynı müşteri için ikinci bir satış siparişi girilir.

[![Yükleme hizmetleri için satış siparişi satırı.](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

İkinci satış siparişi onaylanır. Bu satış siparişi yalnızca bir satır içerdiğinden, satış siparişi onaylandığında gelir fiyatı tahsisatı yapılmaz. Gelir fiyatı tahsisatı, yalnızca iki veya daha fazla benzersiz madde olduğunda ve bu maddeler gelir fiyatı tahsisatı için ayarlanmışsa gerçekleştirilir.

Bu yeni satış siparişi müşterinin sözleşmesinde yapılan tek değişiklik ise yeniden tahsisat işlemi çalıştırılabilir. İki satış siparişinden birinde, **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'i seçerek **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et** sayfasını açın. Alternatif olarak **Gelir kabulü \> Periyodik görevler \> Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'e gidin. İki satış siparişini ve karşılık gelen satış siparişi satırlarını seçin ve **Yeniden tahsisatı güncelleştir**'i seçin. **Yeniden tahsis edilen tutar** sütunu, her satış siparişi satırının yeni gelir fiyatını gösterir.

[![Fiyatı yeni sipariş satırlarıyla yeniden tahsis et sayfasındaki yeni gelir fiyatları.](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

**Beklenen fiş**'i seçerseniz hiçbir fatura deftere nakledilmediği için hiçbir şey gösterilmez.

Yeniden tahsisatı tamamlamak için **İşlem**'i seçin. Deftere hiçbir şey deftere nakledilmemiş olsa bile bir deftere nakil tarihi sorulur. Yeniden tahsisat tamamlandıktan sonra, her satış siparişi için **Gelir fiyatı tahsisatı** sayfası, her iki satış siparişindeki tüm maddelerin fiyat tahsisatını gösterir. Başka bir deyişle, aynı sözleşmenin bir parçası olmasına rağmen farklı bir satış siparişinde olduğundan, her satış siparişinin **Gelir fiyatı tahsisatı** sayfası o satış siparişinde bulunmayan bir madde içerir.

> [!TIP]
> Bu ek maddelerin neden gösterildiğiyle ilgili bağlam sağlamak için kılavuza **Yeniden tahsisat kodu** ve **Satış siparişi** gibi başka sütunlar ekleyebilirsiniz.
> 
> [![Gelir fiyatı tahsisatları sayfasındaki ek sütunlar.](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
