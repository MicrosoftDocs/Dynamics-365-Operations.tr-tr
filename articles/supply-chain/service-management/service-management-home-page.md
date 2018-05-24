---
title: "Servis yönetimi"
description: "Servis Yönetimini servis sözleşmeleri ve servis abonelikleri ayarlamak, servis siparişlerini ve müşteri sorgularını işlemek ve servislerin müşterilere teslimini yönetmek ve incelemek için kullanın."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: tr-tr
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a>Servis yönetimi 

[!include [banner](../includes/banner.md)]


**Servis Yönetimini** servis sözleşmeleri ve servis abonelikleri ayarlamak, servis siparişlerini ve müşteri sorgularını işlemek ve servislerin müşterilere teslimini yönetmek ve incelemek için kullanın. Servis sözleşmelerini normal servis ziyaretinde kullanılan kaynakları tanımlamak için kullanabilirsiniz. Servis sözleşmelerini bu kaynakların müşteriye nasıl faturalandığını görüntülemek için de kullanabilirsiniz. Servis sözleşmesi standart yanıt sürelerini belirten ve gerçek zamanı kaydetmek için araçlar sunan bir hizmet düzeyi sözleşmesi de içerebilir.

Bir müşterinin tesisine servis teknisyeni tarafından yapılan zamanlanmış ve zamanlanmamış ziyaretlerle ilgili bilgileri yönetmek için servis siparişleri oluşturabilirsiniz. Servis siparişleri aşağıdaki gibi bilgileri içerir:

1.  Servis teknisyeninin gerçekleştireceği çalışma saatleri

2.  Servis veya onarım türü

3.  Belirtilen ve tanı ile ilgili bilgiler dahil olmak üzere onarılan madde

4.  Onarım veya hizmet ile ilişkili tüm gider ve masraflar

Enterprise Portal kullanarak müşteriler internet üzerinden servis istekleri gönderebilir. Bu talepleri alabilir, işleyebilir ve dağıtabilirsiniz. Bir servis siparişi oluşturduktan sonra ilerlemeyi izlemek için servis aşamalarını kullanabilir ve her aşamada hangi eylemlerin etkinleştirileceğini denetleyen kurallar belirleyebilirsiniz. Bir servis siparişi tamamlandıktan sonra tamamlandığından emin olmak için siparişte oturumu kapatıp fatura işlemini başlatmak üzere sipariş gönderebilirsiniz.

Servis siparişi marjlarını ve abonelik hareketlerini izlemek için raporlama araçlarını kullanın ve iş açıklamaları ile iş girişlerini yazdırın.

## <a name="business-processes"></a>İş süreçleri

Aşağıdaki şemada **Servis yönetimi** için üst düzey iş süreçleri ve servis süreçlerinin Microsoft Dynamics 365 for Finance and Operations'daki diğer modüllerle hangi noktada tümleştirildikleri gösterilmektedir.

[![Servis yönetimi iş süreci şeması](./media/sm_home_page.gif)](./media/sm_home_page.gif)

## <a name="service-management-at-a-glance"></a>Bir bakışta servis yönetimi

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Önemli görevler</p></th>
<th><p>Birincil formlar</p></th>
<th><p>Sık kullanılan raporlar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Servis sözleşmelerini karşılama</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Servis anlaşmaları (form)</a></p></td>
<td><p><strong>Servis siparişi sınırı</strong></p></td>
</tr>
<tr class="even">
<td><p>Müşteri sorgularını işle</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Servis siparişleri (form)</a></p></td>
<td><p><strong>İş açıklaması</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Gönderme panosu (form)</a></p></td>
<td><p><strong>Hareket - abonelik</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><strong>Abonelik ücreti hareketleri</strong></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a>Servis yönetimi tümleştirmesi

Servis yönetimi Microsoft Dynamics 365 for Finance and Operations'daki şu modüllerle tümleştirilebilir:

  - [Satış ve pazarlama](../sales-marketing/overview-sales-marketing.md)

  - [İnsan kaynakları](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


