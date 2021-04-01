---
title: Satınalma girişlerinde proje maliyet tahakkuku
description: Bu konuda satın alma girişlerinden tahakkuk eden proje maliyetlerinin Microsoft Dynamics 365 Finance'da nasıl izlenebileceği açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c2b92f1f5caf34bf798b86380b73c2dcc7de17b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231652"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Satınalma girişlerinde proje maliyet tahakkuku

[!include [banner](../includes/banner.md)]

Bu konuda satın alma girişlerinden tahakkuk eden proje maliyetlerinin Microsoft Dynamics 365 Finance'da nasıl izlenebileceği açıklanmaktadır. 

Bir proje için fatura genellikle mallar ve hizmetler teslim edildikten daha sonra gelir; bu durumun projenin temel performans göstergeleri (KPI'ler) üzerinde önemli bir etkisi olabilir. Bu hareketleri hem mali hem de proje raporlarından izleyebilmek önemlidir.

Aşağıdaki örnek senaryoda bu gösterilmektedir. 

Contoso Danışmanlık yeni bir bulut dağıtım projesi başlatmıştır. Proje için bir bilgisayar satın almak üzere bir satınalma siparişi oluşturulur. Bilgisayar maliyeti $1500 ve yükleme hizmetleri maliyeti $150 olacaktır. Satıcı bilgisayarı teslim eder ve kurulumunu yapar ancak fatura henüz Contoso Danışmalığa ulaşmamıştır. Proje yöneticisi, fatura teslim edilmeden önce tahakkuk eden $1650 tutarındaki proje maliyetini görmek ister. Bu maliyetin şirketin ay sonu mali tablosuna da yansıtılması gerekmetedir. 

Tahakkuk eden maliyetin hem mali düzeyde hem de raporlama amacıyla proje düzeyinde kaydedilmesi gerekir. Ürün girişinin mali güncelleştirmesi, madde ve tedarik kategorileri için izlenebilir. 

Maddeler için **Borç hesapları parametreleri** sayfasında, **Ürün girişlerini genel muhasebeye naklet** seçeneğini seçin.
[![Borç hesapları parametreleri sayfası](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Tedarik kategorileri için **Kategori ilke kuralı** sayfasında, **Satınalma** ilkelerini ve ardından her tedarik kategorisi için **Satınalma alış irsaliyesindeki gideri tahakkuk et** öğesini seçin.
[![Kategori ilke kuralı sayfası](./media/accruals2-1024x569.png)](./media/accruals2.png) 

**Deftere nakil ayarı**'ndaki **Faturalanmamış satınalma harcaması** ve **Satınalma tahakkuk** ürün girişiyle ilgili fişler deftere nakledildiğinde kullanılacaktır.

Bu aynı senaryoyu kullanarak, bir ürün girişini deftere nakletmenin Genel muhasebeyi ve Proje bilgilerini nasıl etkileyeceğini görelim. 

**Adım 1:** Bilgisayar satın alma için $1500 ve kurulum hizmetleri için $150 kaydetmek üzere proje için yeni bir satınalma siparişi oluşturun ve kaydedin.
[![Yeni satınalma siparişi oluşturma](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Satınalma siparişi teyit edildiğinde, proje için taahhüt edilen maliyet hareketleri oluşturulur. 
[![Oluşturulan hareketler](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Taahhüt edilen maliyet hareketlerinin **Hareket Kaynağı** alanı **Satınalma Siparişi** olarak ayarlanmış olmalıdır. Bir satınalma siparişi oluşturma ve onaylama proje için hareketler oluşturmaz. 

**Adım 2:** Mallar ve hizmetler teslim edilir ve ürün girişi kaydedilir. 

Ürün girişini deftere nakletmek bir fiş oluşturur ve fişi genel muhasebe defterine nakleder. Fiş borç satınalma harcamasını, faturalanmamış hesabını borçlandırır ve satınalma tahakkuk hesabını alacaklandırır. 
[![Fiş hareketleri](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Bir ürün girişini deftere nakletme işlemi, proje kategorileri için deftere nakil ayarını değil tedarik kategorileri ve ürünler için deftere nakil ayarını kullanır. Satınalma tahakkukların mali etkisini doğru biçimde yansıtmak için bu kurulum uyumlu hale getirilmesi gerekir. 

**Tedarik kategorisi** sayfasında tedaril kategorilerini proje kategorileriyle eşleştirmek mümkündür.
[![Tedarik kategorisi sayfası](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Adım 3:** Taslak bir satıcı faturası oluşturma 

Ürün girişinin deftere nakledilmesi proje bilgilerini etkilemez. Geçici bir çözüm olarak, satınalma girişini deftere naklettikten sonra taslak bir satıcı faturası oluşturabilirsiniz. **Satınalma Siparişi** sayfasında &gt; **Fatura sekmesi** &gt; **Generate** &gt; **Fatura** öğesine gidin. Bu, proje bilgilerini güncelleştiren bir bekleyen fatura belgesi oluşturur. 

Taslak satıcı faturası oluşturma bekleyen proje hareketleri oluşturur. 
[![Bekleyen proje hareketleri](./media/accruals8-1024x225.png)](./media/accruals8.png) 

**Taahhüt edilen maliyet** sayfasında, 1. adımda oluşturulan kayıtlar kapatılır ve bekleyen satıcı faturasından gelen maliyet taahhüdünü yansıtmak üzere yeni kayıtlar oluşturulur. Taahhüt edilen maliyet için **Hareket kaynağı** alanı **Satıcı faturası** olarak ayarlanır.
[![Taahhüt edilen maliyetler sayfası](./media/accruals9-1024x200.png)](./media/accruals9.png)

Satıcı faturası gerçek satıcı faturası gelene kadar bekleme durumunda kalır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]