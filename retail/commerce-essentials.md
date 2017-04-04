---
title: "Ticaret essentials genel bakış"
description: "Bu makalede, bir perakende noktası (POS) satış ve e-ticaret işlemleri için Microsoft Dynamics 365 için yapılandırma seçeneği olan ticaret essentials hakkında bilgi sağlar. Ticaretle ilgili temel bilgiler, Microsoft Dynamics tabanlı perakende çözümü ile perakendecilerin hızlıca faaliyete geçmesine yardımcı olan ve onların perakende faaliyetlerine yoğunlaşmalarına yardımcı olan, kullanıma hazır bir perakende iş yükü sağlamaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16121
ms.assetid: 61dced3e-8b6b-4c1f-af39-d20f4ab48659
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6d16a0ebf84b217df0c2cd022ba5bf46e5ca61b2
ms.lasthandoff: 03/31/2017


---

# <a name="commerce-essentials-overview"></a>Ticaret essentials genel bakış

Bu makalede, bir perakende noktası (POS) satış ve e-ticaret işlemleri için Microsoft Dynamics 365 için yapılandırma seçeneği olan ticaret essentials hakkında bilgi sağlar. Ticaretle ilgili temel bilgiler, Microsoft Dynamics tabanlı perakende çözümü ile perakendecilerin hızlıca faaliyete geçmesine yardımcı olan ve onların perakende faaliyetlerine yoğunlaşmalarına yardımcı olan, kullanıma hazır bir perakende iş yükü sağlamaktadır. 

<a name="overview"></a>Özet
--------

İş yazılım ortamları genellikle birçok sistemi, her biri çok özel işlevleri içerir. Genellikle, Perakendeciler işlemleri için Microsoft Dynamics 365'ın Perakende Yönetimi özelliklerinden yararlanmak istiyorsanız, ancak kendi mali varolan veya İnsan Kaynakları (HR) sistemini değiştirmek istemiyorum. Bu Perakendeciler için Perakende için belirli bir iş yükü gereklidir. Ticaret essentials Dynamics 365 işlemleri için bir yapılandırma seçeneği olarak bu özel perakende yetenekleri sunar. Yapılandırma tamamlandıktan sonra çözümün tüm perakende olmayan yönleri görünümden gizlenir böylece odak önemli olan üzerine konabilir. Ticaretle ilgili temel bilgiler Microsoft Dynamics AX 2012 R3 CU8'de ilk olarak bir yapılandırma seçeneği olarak kullanılmıştır Bundan sonra yalnızca tuğla dibek organizasyonlar için omni-kanal Perakendeciler için çalışan bir çözüm sağlamak için birçok geliştirme yapılmıştır.

## <a name="configuration"></a>Yapılandırma
Ticaret essentials yapılandırmak için aşağıdaki adrese gidin **Sistem Yönetimi**&gt;**Kurulum**&gt;**lisans yapılandırma**ve aşağı kaydırma **perakende**. **Perakende** düğümünü genişletin ve **Ticaret temel bilgileri** onay kutusunu seçin. **Kaydet**'i tıklatın, değişiklikleri gözden geçirin ve sonra sayfayı yenileyin. Tam çözüme geçmeyi Git **ticaret essentials**&gt;**Headquarters Kurulumu**&gt;**lisans yapılandırma**ve aşağı kaydırma **perakende**. **Perakende** düğümünü genişletin ve **Ticaret temel bilgileri** onay kutusunu temizleyin. **Kaydet**'i tıklatın, değişiklikleri gözden geçirin ve sonra sayfayı yenileyin.

## <a name="what-is-included"></a>Ne dahildir?
Ticaret essentials çekirdek Dynamics 365 işlemlerini perakende çözüm için çağrı merkezi özellikleri dışında yerleşik tüm perakende arka ofis yetenekleri içerir. Tüm kanal, işçi, ürün, mağaza, kayıt ve aygıt yönetimi yetenekleri tek bir gezinti düğümünde bulunur. Ayrıca, tüm tam perakende çalışma out-of-box role özgü giriş sayfaları sağlamak için eklenmiştir. Ticaret essentials perakende Modern POS (MPOS) ve e-ticaret kanallardan yararlanabilir Tuğla Dibek veya mobil bir senaryonuz varsa Perakendeciler hedefler. Perakendeciler, ticaret temel bilgilerini kullanarak, tek bir yerde bu kanalları yönetebilir ve bu nedenle doğru omni-kanal yetenekleri kazanabilir.

## <a name="how-is-commerce-essentials-different"></a>Ticaret temel bilgileri farkı nedir?
Birleştirilmiş gezinti ve yalnızca perakende sayfaları sağlamanın yanı sıra, ticaret temel bilgileri, alanlar ve denetimler gibi tüm perakende olmayan sayfa öğelerini gizler. Sonuç perakendecilere Göreve odaklanmanıza yardımcı olacak kullanışlı kullanıcı arabirimidir. Tam ürün lisansına sahip Perakendeciler ticaret essentials daha fazla perakende odaklı kullanıcılar için bir başlangıç noktası olarak kullanabilirsiniz. Gerekli olduğu gibi gelişmiş HR yetenekleri gibi diğer öğeleri yerinde olduğundan Lisans Sözleşmesi'nin hükümlerine uygun ticaret essentials için eklenebilir. Hızlandırma ve basitleştirme kapsamında ticaret temel bilgileri Perakendeciler mevcut muhasebe sistemlerine ticaret temel bilgileri için hesap numaraları, tahakkuk toplamlarını eşleme hesap verme yeteneği sağlar. Perakende sistem finansal verileri oluşturduğu için bu veriler kolayca ticaret temel bilgilerinden perakendecinin muhasebe sistemine verilebilir. Daha gelişmiş tümleştirme yeteneklerini gerekliyse, ticaret essentials de içerir Dynamics 365 işlemleri için içerdiği tam alma/verme framework. Varsayılan olarak dahil edilen yüzlerce veri varlıkları ticaret temel bilgilerine birden fazla uzmanlaşmış sistemlerin kullanıldığı bir çok katmanlı ortama rahatlıkla sığacak şekilde esneklik sağlar.


