---
title: "Bir çağrı merkezi için bir süreklilik programı kurma"
description: "Bu makalede, çağrı merkezi için bir süreklilik programının nasıl kurulacağı açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e32961f2a0e0e41715d98075cbc5777d256eb187
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Bir çağrı merkezi için bir süreklilik programı kurma

Bu makalede, çağrı merkezi için bir süreklilik programının nasıl kurulacağı açıklanmaktadır.

Yinelenen sipariş programı olarak da bilinen olan süreklilik programında müşteriler önceden tanımlanmış bir plana uygun olarak düzenli ürün sevkiyatları alır. Her bir sevkiyat bir 'ayın kitabı kulübünde' olduğu gibi farklı bir ürün içerebilir veya aynı ürün tekrar tekrar gönderilebilir. Bir süreklilik programı kurmak için mutlaka aşağıdaki görevleri tamamlamanız gerekir.

1.  **Çağrı merkezi parametreleri** sayfasından süreklilik parametrelerini ayarlayın.
2.  Ödeme planı, sevkiyatların zamanlaması ve faturanın önceden düzenlenip düzenlenmeyeceği gibi ayrıntıları belirten bir süreklilik programı oluşturun. Ayrıca, süreklilik programına dahil edilecek ürünlerin bir listesini de eklemeniz gerekir. Her ürün 1'den başlayarak ardışık olarak atanan bir olay kimlik numarası alır. Olay kimlikleri ürünleri gönderilen sipariş belirler.
    -   Müşteriler her sevkiyatta farklı bir ürün alıyorsa ürünler, olay kimliklerine dayalı olarak ve mevcut olaydan başlayarak ardışık olarak gönderilir.
    -   Müşteriler her sevkiyatta aynı ürünü alıyorsa liste sadece bir olaya sahip bir ürün içerir. Aynı olay tekrar tekrar oluşur. Her olayın kaç defa tekrarlanacağını belirtebilirsiniz.

3.  Görev 2'de oluşturduğunuz süreklilik programı temsil eden bir üst ürün oluşturun. Bir satış siparişi için bu ürünü eklerseniz, **süreklilik** sayfası açılır. Ardından, fiili süreklilik siparişi oluşturmak için bu sayfayı kullanabilirsiniz. Üst ürün müşterinin her sevkiyatta aldığı ürünler tek tek belirtmez.

Yukarıda açıklandığı gibi bir süreklilik programı ayarladıktan sonra müşteri için bir süreklilik siparişi oluşturabilirsiniz. Ayrıca, aşağıdaki ek idame görevlerini de gerçekleştirmeniz gerekebilir.

-   **Mevcut süreklilik olay dönemini güncelleştir** – Sisteme mevcut olay döneminin ne olacağını söyleyen bir toplu iş oluşturun.
-   **Süreklilik alt siparişleri oluştur** – Üst süreklilik siparişinden alt siparişler oluşturun.
-   **Süreklilik ödemelerini işle** – Süreklilik satış siparişleriyle ilişkili ödemeler için faturalamayı ve bildirimleri işleyin.
-   **Süreklilik satırlarını genişlet** (gerekiyorsa) – Bir süreklilik olayının tekrarlanabileceği sayıyı girin. Sevkiyatların tekrarlanması çağrı merkezi parametrelerindeki **Süreklilik tekrar eşiği** alanında ayarlanan sınırın ötesinde de genişletilebilir.
-   **Bir süreklilik güncelleştirmesi gerçekleştir** (gerekiyorsa) – Süreklilik programı ile süreklilik üst satış siparişleri arasındaki değişiklikleri eşitleyin.
-   **Süreklilik üst satırlarını ve siparişlerini kapat** – Süreklilik siparişlerini kapatın.



