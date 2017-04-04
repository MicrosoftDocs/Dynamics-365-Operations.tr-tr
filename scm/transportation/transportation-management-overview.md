---
title: "Taşıma yönetimine genel bakış"
description: "Bu konuda, Microsoft Dynamics 365 for Operations&quot;daki taşıma yönetimi işlevine genel bir bakış sunulur."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3136fd95c4c56495a391668d6c854a6ae1e36479
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-overview"></a>Taşıma yönetimine genel bakış

Bu konuda, Microsoft Dynamics 365 for Operations'daki taşıma yönetimi işlevine genel bir bakış sunulur.

Taşıma yönetimi, şirketinizin taşımalarını yönetmenize olanak tanır ve satıcı ile gelen ve giden siparişler için yönlendirme çözümlerini belirlemenizi sağlar. Örneğin bir sevkiyat için en hızlı yolu veya en ucuz oranı tanımlayabilirsiniz. Aşağıdaki tablo, Microsoft Dynamics 365 for Operations'daki Taşıma yönetiminin kullanılmasına ilişkin ana senaryoları açıklar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Senaryo</th>
<th>Taşıma yönetimi nasıl yardımcı olur?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Taşıma faaliyetleri için dış lojistik sağlayıcılarını kullanın.</td>
<td>Gelen ve/veya giden taşıma için Taşıma yönetimini kullanın.</td>
</tr>
<tr class="even">
<td>Şirketin teslimat/mal alımı için kullandığı kendi filosu vardır ve teslimat giderleri müşterilere aktarılır.</td>
<td>Giden işlemleri için, taşıma giderlerini belirlemek ve bunları müşterilere aktarmak için Taşıma yönetimini kullanabilirsiniz. Ancak, taşıyıcı fatura mutabakat işlemi gerekli değildir.</td>
</tr>
<tr class="odd">
<td>Teslimat/mal alımı için şirketin kendi filosu vardır ancak ürün fiyatı nakliyeyi içerdiğinden teslimat giderleri müşterilere aktarılmaz.</td>
<td>Çok sayıda Taşıma yönetimi işlevi gerekli değildir. Bununla birlikte, taşıma fiyatlarını belirlemek ve satış fiyatını buna göre ayarlamak için Taşıma yönetimini kullanabilirsiniz.</td>
</tr>
<tr class="even">
<td>Lojistik hizmeti aynı şirketteki başka bir tüzel kişilik tarafından sağlanır.</td>
<td><ul>
<li>Başka bir tüzel kişiliği herhangi bir sevkiyat yüklenicisi olarak kullanmak için Taşıma yönetimini kullanabilirsiniz. Tüzel kişilikler arasındaki ekonomik hareketleri otomatik hale getiremezsiniz. Bu nedenle, bu hareketleri el ile işlemeniz gerekir (örneğin, bir satınalma siparişi oluşturarak).</li>
<li>Lojistik hizmetler sunan tüzel kişilikte, Taşıma yönetimi taşıma ücretlerini belirlemek için kullanılabilir.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-dynamics-365-for-operations"></a>Dynamics 365 for Operations'da taşımayı planlama
Taşıma yönetiminde , taşıma planlaması için siparişler veya bu siparişlere göre oluşturulan sevkiyatlar temel alınır. Sevkiyatlar daima zaman içinde bir noktada bulunmaktadır ancak taşıma planlaması için gerekli değildir. Transfer emirleri giden senaryosunun bir parçasıdır ve satış siparişleriyle birlikte planlanabilir. 

![Yük çizme](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Gelen taşıma
Bir satıcıdan madde siparişi ve sizin ambarınıza maddeler teslim edilmelidir öğeleri taşıma kendiniz düzenlemek isteyebilirsiniz. Nakliye ve gelen yük alınması planlamak için Dynamics 365 işlemleri için kullanabilirsiniz. Aşağıdaki şekilde, gelen yük için taşıma planlamasına ilişkin iş süreci akışı gösterilmektedir. 

![Gelen yükün taşınmasına ilişkin iş süreci akışı](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Giden taşıma
Belirli maddeleri şirketin ambarından müşteriye sevk etmek için giden yük planlaması yapabilir ve işleme koyabilirsiniz. Giden yük için taşıma ve sevkiyat planlaması yapmak için Dynamics 365 for Operations kullanabilirsiniz. Aşağıdaki şekilde, giden yükün sevkiyat için planlaması ve işleme konmasına ilişkin iş süreci akışı gösterilmektedir. 

![Planlama ve giden işlem yükler](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Yapıyı yükle
Dynamics 365 for Operations, Hacim tabanlı yük oluşturma stratejisi olarak adlandırılan bir yük oluşturma stratejisi sunar. Bu strateji, yük şablonunda yükseklik ve ağırlık için belirtilen maksimum değerleri kullanmanıza olanak tanır; veya yeni değerler girerek ayarları geçersiz kılabilirsiniz. Kullanmak için **Yük oluşturma workbench'i** sayfasında bulunan **Ayar** Hızlı sekmesindeki **Yük oluşturma stratejisi** alanından bu stratejiyi seçebilirsiniz. Ayrıca, Uygulama Nesne Ağacı'nda (AOT) yeni bir sınıf oluşturarak kendi yük oluşturma stratejinizi ekleyebilirsiniz.


