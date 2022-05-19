---
title: Gelir kabulü yeniden tahsisatı - Senaryo 3
description: Bu konu, yeni bir satırın var olan, faturalandırılmış bir satış siparişine eklendiği yeniden tahsisat senaryosunu ele alır. Bir sözleşmeye yeni bir madde eklendiğinde, yeni bir satış siparişine ya da var olan satış siparişine eklenebilir.
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
ms.openlocfilehash: 3b3b41b09cc9f4c56fdb04f6a2c4156bc1637699
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726591"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Gelir kabulü yeniden tahsisatı – Senaryo 3

[!include [banner](../includes/banner.md)]

Bu konu, yeni bir satırın var olan, faturalandırılmış bir satış siparişine eklendiği yeniden tahsisat senaryosunu ele alır. Bir sözleşmeye yeni bir madde eklendiğinde, yeni bir satış siparişine ya da var olan satış siparişine eklenebilir. Bu senaryo, yeniden tahsisat nedeniyle Alacak hesapları güncelleştirildiğinde ne olacağını da gösterir.

Bu senaryoda **Genel muhasebe parametreleri** sayfasının (**Gelir kabulü \> Kurulum \> Genel muhasebe parametreleri**) **Gelir kabulü** sekmesinde **Fatura düzeltmelerini Alacak hesaplarına naklet** seçeneği **Evet** olarak ayarlanmıştır.

[![Fatura düzeltmelerini Alacak hesaplarına deftere naklet seçeneği Evet olarak ayarlı.](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

US\_SI\_0003 müşterisi için bir satış siparişi oluşturulur. Müşteri bir dizüstü bilgisayar (madde numarası S0012) ve destek planı (madde numarası S0008, "Sürekli Mühendislik Hizmeti") satın alır. Dizüstü bilgisayar geliri hemen tanınır. Destek planının geliri, sözleşmedeki tarih aralığında tanımlandığı şekilde ertelenir ve 12 ay içinde kabul edilir.

[![Dizüstü bilgisayar ve destek planı için satış siparişi satırları.](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Satış siparişi onaylanır. Gelir fiyatı tahsisatı için her iki madde ayarlandığından, satış siparişi onaylandığında gelir fiyatı hesaplanır. Kabul edilecek geliri **Gelir fiyatı tahsisatı** sayfasında görüntüleyebilirsiniz (**Satış siparişi** sayfasında, Eylem bölmesi, **Yönet** sekmesi, **Gelir kabulü** grubunda, **Gelir fiyatı tahsisatı**'nı seçin). Dizüstü bilgisayar geliri, Gelir hesabına 1008,01 dolar olarak nakledilir. Destek planı geliri Ertelenmiş gelir hesabına 190,99 dolar olarak nakledilir. Gelir fiyatlarının toplamı, gelir fiyatı tahsisatı (1.199,00 dolar) yakalamak için ayarlanan satırların toplamına eşit olmalıdır.

[![Gelir fiyatı tahsisatı sayfası.](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Satış siparişi tamamen faturalanmıştır. Aşağıdaki şekilde, fatura için deftere nakledilen muhasebe girişi gösterilmektedir.

[![Tamamen faturalanan satış siparişi için muhasebe girişi.](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Gelir kabulü planı da oluşturulur. Bir süre geçtikten sonra, ayların ikisinde destek planı için kabul edilen gelir bulunur.

[![İki ay geçtikten sonra gelir kabulü planı sayfası.](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Bu aşamada müşteri, yükleme hizmetlerini (madde numarası S0001) eklemeye karar verir. Bu madde var olan satış siparişine eklenir. Müşteriden, tamamen faturalanmış satış siparişini değiştirmek istediğini onaylaması istenir ve müşteri **Evet**'i seçer.

[![Yükleme hizmetleri satırı eklendikten sonra satış siparişi.](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Bu yeni madde müşterinin sözleşmesinde yapılan tek değişiklik ise yeniden tahsisat işlemi çalıştırılabilir. Satış siparişinde, **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et**'i seçerek **Fiyatı yeni sipariş satırlarıyla yeniden tahsis et** sayfasını açın. Bu satış siparişinin tüm satış siparişi satırlarını seçin ve **Yeniden tahsisatı güncelleştir**'i seçin. **Yeniden tahsis edilen tutar** sütunu, her satış siparişi satırının yeni gelir fiyatını gösterir.

[![Fiyatı yeni sipariş satırlarıyla yeniden tahsis et sayfasındaki yeni gelir fiyatları.](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Ardından, muhasebe girişlerini görüntülemek için **Beklenen fiş**'i seçin. **Genel muhasebe parametreleri** sayfasında **Fatura düzeltmelerini Alacak hesaplarına deftere naklet** seçeneğini **Evet** olarak ayarlandığı için bu muhasebe girişleri alacak belgesi üzerinden Genel muhasebeye nakledilir ve Alacak hesaplarında yeni bir fatura oluşturulur.

[![Beklenen fiş sayfasındaki muhasebe girişleri.](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

**Beklenen fiş** sayfasında, son dört satır deftere nakledilen faturadaki orijinal muhasebe girişini tersine çevirir. İlk beş satır, fatura için deftere nakledilen yeni muhasebe girişleridir. Müşteriye yeni bir fatura sunulmayacağını lütfen unutmayın. Yeniden tahsisat tamamlandıktan sonra, müşteri halen 1276,94 dolar borçludur. Bu miktar, yeni muhasebe girişinde Alacak hesaplarına nakledilmesi gereken tutardır. Mahsup edilen vergi ve gelir ya da ertelenen gelir eşittir 995,83 dolar + 188,69 dolar + 77,94 = 1262,46 dolar. Gelir veya ertelenen gelir tutarı yeniden tahsisat nedeniyle değişmiştir. -14,48 dolarlık fark, Kısmi fatura geliri kliring hesabı defterine nakledilir. Fatura satış siparişine eklenen yeni madde için deftere nakledildiğinde, bu bakiye temizlenecektir.

Yeniden tahsisatı tamamlamak için **İşlem**'i seçin. Bir deftere nakil tarihi girilir. Yeniden tahsisat tamamlandıktan sonra, **Gelir fiyatı tahsisatı** sayfası tüm üç madde için fiyat yeniden tahsisatını gösterir.

[![Gelir fiyatı tahsisatı sayfasında üç maddenin tamamı için fiyat yeniden tahsisatı.](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Gelir kabulü planı da yeni gelir yeniden tahsisat fiyatına göre güncelleştirilmiştir. Satış siparişinde, **Gelir kabulü planı** sayfasını açın. Daha önce, madde S0008 için 13 satır bulunuyordu (bu maddeye 12 aylık bir çizelge atanmıştır). Artık 39 satır vardır: 13 özgün çizelge satırı, 13 ters işlem çizelgesi satırı ve yeni gelir fiyatını temel alan 13 satır.

[![S0008 maddesi için 39 satırla güncelleştirilmiş Gelir kabulü planı sayfası.](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

**Fiş**'i seçtiğinizde, fatura günlüğü özgün muhasebe girişini gösterir. Ters işlem girişini ve satış siparişindeki yeni muhasebe girişini görüntülemek için Eylem Bölmesinde **Gelir ayarlamaları**'nı ve ardından **Fiş**'i seçin.

Daha sonra, **Tüm müşteriler** sayfasını açın (**Alacak hesapları \> Müşteriler \> Tüm müşteriler**), **US\_SI\_0003** müşterisini ve ardından **Hareketler**'i seçin. **Müşteri hareketleri** sayfasında, özgün fatura (000006), ters işlem belgesi (000006-1) ve yeni fatura (000006-2) gösterilir. Özgün fatura ve ters işlem belgesi birbiriyle kapatılır ve bakiyeleri 0 (sıfır) olur. Genel muhasebedeki etkiyi görmek için her belgenin fişini görüntüleyin.

[![Müşteri hareketleri sayfasındaki özgün fatura, ters işlem belgesi ve yeni fatura.](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Satış siparişi eklenen madde için yeniden faturalanır. Müşteriye sunulan toplam fatura 300,00 dolar + 19,50 dolar vergi = 319,50 dolar olur. Aşağıdaki şekilde, deftere nakledilen muhasebe girişi gösterilmektedir.

[![Deftere nakledilen muhasebe girişini içeren fiş hareketleri sayfası.](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Gelir ve satışın toplamı 319,50 dolardan fazla olduğundan, 14,48 dolarlık fark deftere nakledilir. Bu tutar, Kısmi fatura geliri kliring hesabındaki bakiyeyi kapatır. Bu bakiye, yeniden tahsisat işleminden sonra deftere nakledilen yeni muhasebe girişinde güncelleştirilmiştir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
