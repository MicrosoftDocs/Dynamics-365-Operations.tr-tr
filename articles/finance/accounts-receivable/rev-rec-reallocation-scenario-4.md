---
title: Gelir kabulü yeniden tahsisatı - Senaryo 4
description: Bu makalede bir satırın var olan, kısmen faturalandırılmış bir satış siparişinden kaldırıldığı yeniden tahsisat senaryosu ele alınmaktadır. Bu senaryo, satırın satış siparişinden kaldırılıp kaldırılmadığına veya iptal edildi durumuna ayarlanmış olup olmamasına bakılmaksızın aynı sonucu verir.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 06e6322ff55259b5c59d570b73199591ab46c767
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891680"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Gelir kabulü yeniden tahsisatı – Senaryo 4

[!include [banner](../includes/banner.md)]

Bu makalede bir satırın var olan, kısmen faturalandırılmış bir satış siparişinden kaldırıldığı yeniden tahsisat senaryosu ele alınmaktadır. Bu senaryo, satırın satış siparişinden kaldırılıp kaldırılmadığına veya iptal edildi durumuna ayarlanmış olup olmamasına bakılmaksızın aynı sonucu verir.

Bu senaryoda **Genel muhasebe parametreleri** sayfasının (**Gelir kabulü \> Kurulum \> Genel muhasebe parametreleri**) **Gelir kabulü** sekmesinde **Fatura düzeltmelerini Alacak hesaplarına naklet** seçeneği **Hayır** olarak ayarlanmıştır.

[![Fatura düzeltmelerini Alacak hesaplarına deftere naklet seçeneği Hayır olarak ayarlı.](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

US\_SI\_0003 müşterisi için bir satış siparişi oluşturulur. Müşteri bir dizüstü bilgisayar (madde numarası S0012), yükleme hizmetleri (madde numarası S0001) ve dizüstü bilgisayar destek planı (madde numarası S0008, "Sürekli Mühendislik Hizmeti") satın alıyorsa. Dizüstü bilgisayar ve yükleme hizmetlerinin geliri hemen tanınır. Destek planının geliri, sözleşmedeki tarih aralığında tanımlandığı şekilde ertelenir ve 12 ay içinde kabul edilir.

[![Dizüstü bilgisayar, yükleme hizmetleri ve destek planı için satış siparişi satırları.](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Satış siparişi onaylanır. Gelir fiyatı tahsisatı için üç maddenin tümü ayarlandığından, satış siparişi onaylandığında gelir fiyatı hesaplanır. Kabul edilecek geliri **Gelir fiyatı tahsisatı** sayfasında görüntüleyebilirsiniz (**Satış siparişi** sayfasında, Eylem bölmesi, **Yönet** sekmesi, **Gelir kabulü** grubunda, **Gelir fiyatı tahsisatı**'nı seçin). Dizüstü bilgisayar için gelir, Gelir hesabına 995,84 dolar olarak nakledilir. Yükleme hizmetleri geliri de Gelir hesabına 314,47 dolar olarak nakledilir. Destek planı geliri Ertelenmiş gelir hesabına 188,69 dolar olarak nakledilir. Gelir fiyatlarının toplamı, gelir fiyatı tahsisatı (1499,00 dolar) yakalamak için ayarlanan satırların toplamına eşit olmalıdır.

[![Gelir fiyatı tahsisatı sayfası.](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Müşteriye dizüstü bilgisayar ve destek planı için fatura kesilir ancak yükleme hizmetleri için kesilmez. Aşağıdaki şekilde, fatura için deftere nakledilen muhasebe girişi gösterilmektedir.

[![Faturalanan satış siparişi için muhasebe girişi.](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Muhasebe girişi, Alacak hesaplarına 1276,94 dolar olarak nakledilir. Ancak, bu fatura kısmi fatura olduğundan gelir veya ertelenen gelir artı vergi, Alacak hesapları tutarına eşit değildir. -14,47 dolarlık fark, Kısmi fatura geliri kliring hesabı defterine nakledilir.

Gelir kabulü planı da oluşturulur.

[![Kısmi fatura için gelir kabulü planı sayfası.](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Daha sonra müşteri, yükleme hizmetlerini satın almamaya karar verir. Bu nedenle, satır satış siparişinden çıkarılır. Satış siparişinde yalnızca faturalanan satırlar kaldığı için satış siparişinin yeniden onaylanamayacağını unutmayın.

[![Yükleme hizmetleri satırı kaldırıldıktan sonra satış siparişi.](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Satış siparişi onaylanamasa da yeniden tahsis edilebilir. Satış siparişinde, **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'i seçerek **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et** sayfasını açın. Kalan iki satış siparişi satırını seçin ve **Yeniden tahsisatı güncelleştir**'i seçin. **Yeniden tahsis edilen tutar** sütunu, kalan her satış siparişi satırının yeni gelir fiyatını gösterir.

[![Fiyatı yeni sipariş satırlarıyla yeniden tahsis et sayfasındaki yeni gelir fiyatları.](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Ardından, muhasebe girişlerini görüntülemek için **Beklenen fiş**'i seçin.

[![Beklenen fiş sayfasındaki muhasebe girişleri.](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

**Beklenen fiş** sayfasında, son beş satır deftere nakledilen faturadaki orijinal muhasebe girişini tersine çevirir. İlk dört satır, fatura için deftere nakledilen yeni muhasebe girişleridir. Müşteriye yeni bir fatura sunulmayacağını lütfen unutmayın. Yeniden tahsisat tamamlandıktan sonra, müşteri halen 1276,94 dolar borçludur. Bu miktar, yeni muhasebe girişinde Alacak hesaplarına nakledilmesi gereken tutardır. Yeni gelir veya ertelenen gelir artı vergi, eşittir 1276,94 dolardır. Bu nedenle, Kısmi fatura geliri kliring hesabına deftere nakil yapmanız gerekmez.

Yeniden tahsisatı tamamlamak için **İşlem**'i seçin. Bir deftere nakil tarihi girilir. Yeniden tahsisat tamamlandıktan sonra, **Gelir fiyatı tahsisatı** sayfası kalan iki madde için fiyat yeniden tahsisatını gösterir.

[![Gelir fiyatı tahsisatı sayfasında kalan maddeler için fiyat yeniden tahsisatı.](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Gelir kabulü planı da yeni gelir yeniden tahsisat fiyatına göre güncelleştirilmiştir. Satış siparişinde, **Gelir kabulü planı** sayfasını açın. Daha önce, madde S0008 için 13 satır bulunuyordu (bu maddeye 12 aylık bir çizelge atanmıştır). Artık 39 satır vardır: 13 özgün çizelge satırı, 13 ters işlem çizelgesi satırı ve yeni gelir fiyatını temel alan 13 satır.

[![S0008 maddesi için 39 satırla güncelleştirilmiş gelir kabulü planı sayfası.](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

**Fiş**'i seçtiğinizde, fatura günlüğü özgün muhasebe girişini gösterir. Ters işlem girişini ve satış siparişindeki yeni muhasebe girişini görüntülemek için Eylem Bölmesinde **Gelir ayarlamaları**'nı ve ardından **Fiş**'i seçin.

Daha sonra, **Tüm müşteriler** sayfasını açın (**Alacak hesapları \> Müşteriler \> Tüm müşteriler**), **US\_SI\_0003** müşterisini ve ardından **Hareketler**'i seçin. **Müşteri hareketleri** sayfası, orijinal muhasebe girişiyle birlikte yalnızca orijinal faturayı (000008) gösterir. **Faturayı düzeltmelerini Alacak hesaplarına naklet** seçeneği, **Genel muhasebe parametreleri** sayfasında **Hayır** olarak ayarlandığından, yalnızca Genel muhasebe güncelleştirilir. Bu nedenle, ters işlem ve güncelleştirilmiş muhasebe girişleri gösterilmez. [Senaryo 3](rev-rec-reallocation-scenario-3.md)'te oluşturulan gelir ayarlama hareketlerinin gösterildiğini unutmayın.

[![Müşteri hareketleri sayfasındaki orijinal muhasebe girişi.](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
