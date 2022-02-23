---
title: Dynamics 365 Supply Chain Management 10.0.6'daki yenilikler veya değişiklikler (Kasım 2019)
description: Bu konuda, Dynamics 365 Supply Chain Management 10.0.6'daki yeni veya değişen özellikler açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439347"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Dynamics 365 Supply Chain Management 10.0.6'daki yenilikler veya değişiklikler (Kasım 2019)

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.6'daki yeni veya değişen özellikler açıklanmaktadır. Bu sürümün derleme numarası 10.0.234'tür. Genel kullanılabilirlik tarihi Kasım ayında olmasına karşın Ekim ayındaki erken sürüm için yeni özellikler bulunmaktadır. 10.0.6 sürümü hakkında daha fazla bilgi için bkz. [Ek kaynaklar](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Ürün yapılandırma modelleri V2 veri varlığı

"Ürün yapılandırma modelleri" veri varlığının ikinci sürümü yayınlandı ("ürün yapılandırma modelleri V2" olarak adlandırılmıştır). "418-ürün yapılandırma modelleri" varsayılan şablonunun da içe aktarma/dışa aktarma çerçevesi şablonlarında yeni "ürün yapılandırma modelleri V2" veri varlığını kullanması gerekmektedir. Şablon otomatik olarak güncelleştirilmez, bu nedenle şablonu varsayılan olarak el ile yüklemeniz gerekir. V2 varlığı, V1 varlığının boyut sınırlamalarını çözmek amacıyla bir satırı satır içi yerine ekli ayrı bir dosya olarak dışa aktarır. 
 
Bu değişikliği yapmak için ne yapmanız gerekir?
-    V1 varlığı kullanım dışı bırakıldığından, V1'den V2'ye geçişi başlatmanız gerekir. "418-ürün yapılandırma modelleri" şablonunu kullanıyorsanız, "varsayılan şablonları yükle" düğmesine tıklayabilir ve "418 – ürün yapıladırma modelleri" şablonunu yeniden yükleyebilirsiniz
-    Varolan sistemlerle uyumluluğu korumak istiyorsanız, tümleştirmeleri yeni şablona taşııncaya kadar varolan şablonu ve (kullanım dışı) V1 varlığını kullanmaya devam edebilirsiniz. 

## <a name="feature-management-enhancements"></a>Özellik yönetimi geliştirmeleri
Özellik yönetimi şimdi tüm yeni özellikleri varsayılan olarak etkinleştirmenize, bir özelliği etkinleştirmek için onay gerektirmenize ve önceden etkinleştirilmemiş olan tüm özellikleri etkinleştirmenize olanak tanır. 


## <a name="purchase-agreement-responsible-party"></a>Satınalma sözleşmesi sorumlu taraf
Artık, Satınalma sözleşmesi sınıflandırma formunda ve sonuçta elde edilen Satınalma sözleşmelerinde birincil ve ikincil sorumlu tarafları tanımlama olanağınız vardır.  Bu, kullanıcıya sözleşmeleri denetleyenlere erişim olanağı sağlar.

## <a name="rfq-link-on-the-purchase-order-line"></a>Satınalma siparişi satırındaki RFQ bağlantısı
Satınalma siparişi satırlarından, oluşturuldukları karşılık gelen RFQ satırlarına bir referans bağlantısı ekleyebilirsiniz; bu, kullanıcıya destekleyen teklif talebi belgesinin kolaylıkla sunulmasını sağlar.

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="bug-fixes"></a>Hata düzeltmeleri
10.0.6'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) görüntüleyin.

### <a name="platform-update-30"></a>Platform update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 Platform update 30 içerir. Platform update 30 hakkında daha fazla bilgi edinmek için bkz. [Platform update 30'daki yenilikler veya değişiklikler](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 sürüm dalgası 2 planı
İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365: 2019 sürüm dalgası 2 planını](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/) inceleyin. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.
