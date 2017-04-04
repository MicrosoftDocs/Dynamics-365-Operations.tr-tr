---
title: "Satınalma alış irsaliyelerini üzerinde Proje Maliyet tahakkuku"
description: "Bu konu, satınalma alış irsaliyelerini Microsoft Dynamics 365 işlemleri için de izlenebilir nasıl tahakkuk eden maliyetler proje açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Satınalma alış irsaliyelerini üzerinde Proje Maliyet tahakkuku

Bu konu, satınalma alış irsaliyelerini Microsoft Dynamics 365 işlemleri için de izlenebilir nasıl tahakkuk eden maliyetler proje açıklar. 

Fatura projesi için ulaşması genellikle daha sonraki mal ve hizmetler, projenin anahtar performans göstergeleri (APG) önemli bir etkisi olabilir teslim edilir. Bu hem mali işlemleri izlemek ve proje yapabilmek önemli rapor.

Aşağıdaki örnek senaryoyu bunu göstermektedir. 

Contoso danışmanlık yeni bir bulut dağıtım projesi başladı. Proje için bir bilgisayar satın almak için bir satınalma siparişi oluşturulur. Bilgisayar $1500 maliyeti ne olacak ve $150 Yükleme Hizmetleri maliyeti. Satıcının teslim ve bilgisayarda yüklü, ancak faturayı Contoso danışmanlık henüz ulaşmamış. Proje Yöneticisi Proje maliyet tahakkuk $1650, faturayı teslim edilmeden önce görmek ister misiniz. Bu maliyet şirketin ay sonu finansal raporlarda da yansıtılması. 

Tahakkuk eden maliyeti mali düzeyi ve proje düzeyi üzerinde raporlama amaçları için kaydedilmesi gerekir. İşlemler için Dynamics 365 madde ve tedarik kategoriler için mali güncelleştirme ürün giriş izlenebilir. 

Maddeler, üzerinde **hesaplarına borç parametreleri** sayfa, seçme **ürün girişleri genel muhasebeye nakletmek** seçeneği.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Tedarik kategorileri için üzerinde **kategori ilke kuralına** sayfa, seçme **satınalma** ilkeleri ve seçin **alış irsaliyesindeki satınalma gideri tahakkuk** tedarik her kategori için.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

**Harcamayı takip faturalanmamış satınalma** ve **satınalma tahakkuk** hesapları **deftere nakil kurulumu** ürün alış irsaliyesiyle ilgili fişleri deftere naklederken kullanılacak.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Bu aynı senaryoyu kullanarak, nasıl bir ürün alış irsaliyesini deftere nakil genel muhasebe ve proje bilgilerini etkiler görelim. 

**Adım 1:** oluşturma ve $150 için $1500 ve Yükleme Hizmetleri için bir bilgisayar satın kaydetmek proje için yeni bir satınalma siparişi onayla.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Satınalma siparişi teyit edildiğinde, hareketler için taahhüt edilen maliyet projesi için oluşturulur. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Taahhüt edilen maliyet hareketlerini olur **hareket kaynağı** alanı ayarlamak **satınalma siparişi**. Oluşturma ve bir satınalma siparişi teyit eden bir proje için hareketleri oluşturmaz. 

**Adım 2:**, mal ve hizmetlerin teslim ve ürün bilgisi kaydedilir. 

Ürün alış irsaliyesini deftere nakil oluşturmak ve deftere nakletmek için genel muhasebe fiş. Fiş borç satınalma harcamayı takip, faturalanmamış hesabı ve satınalma tahakkuk hesabını alacaklandırın. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Ürün alış irsaliyesi deftere nakile tedarik kategoriler ve ürünler ve değil Proje kategorileri için nakil ayarını kullanır. Satınalma tahakkukların mali etkisini doğru biçimde yansıtmak için bu kurulum hizalanması gerekir. 

Üzerinde Proje kategorileri tedarik kategorileriyle eşleyin mümkündür **tedarik kategori** sayfa.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Adım 3:** bir taslak satıcı faturası oluşturun. 

İşlemler için Dynamics 365 içinde ürün alış irsaliyesini deftere nakil proje bilgilerini etkilemez. Geçici bir çözüm, doğrudan satınalma alış irsaliyesini deftere nakledildikten sonra taslak satıcı faturası oluşturabilir. Git **satınalma siparişi** sayfası &gt;**Fatura sekmesi**&gt;**Generate**&gt;**fatura**. Bu proje bilgilerini güncelleştiren bir bekleyen fatura belgesi oluşturur. 

Taslak satıcı faturası oluşturma bekleyen proje hareketleri oluşturur. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

İçinde **taahhüt edilen maliyet** sayfa, 1. adımda oluşturulan kayıtları kapatılır ve yeni kayıtlar bekleyen satıcı fatura gelen maliyet taahhüt yansıtacak şekilde oluşturulacaktır. **Hareket kaynağı** için taahhüt edilen maliyet ayarlanacak alan **satıcı faturası**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Satıcı Fatura gerçek satıcı fatura gelene kadar bekleme durumunda kalır.


