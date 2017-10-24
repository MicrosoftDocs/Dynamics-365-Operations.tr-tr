---
title: "Sipariş tutmaları"
description: "Bu konu Dynamics 365 for Retail kullanarak siparişlerdeki tutmaları açıklar."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="order-holds"></a>Sipariş tutmaları

[!include[banner](includes/banner.md)]


Bu konu Dynamics 365 for Retail kullanarak siparişlerdeki tutmaları açıklar.

Sipariş çeşitli nedenlerle bekletmeye alınabilir. Örneğin, müşteri adresi veya ödeme yöntemi doğrulanıncaya kadar veya bir yönetici müşterinin kredi limiti gözden geçirene kadar siparişi beklemeye alabilirsiniz. Satış işlemi sırasında satış siparişlerinin beklenmeye alınması gereken zamanlar vardı. Örneğin, bir satış siparişi, Müşteri ödeme ile ilgili sorunlar nedeniyle şüpheli dolandırıcılık nedeniyle veya bir yöneticinin sipariş incelemesi gerektiğinde beklemeye alınabilir. Bir satış siparişi beklemeye alındığında, bir sipariş tutma kodu satış siparişine tutma nedenini belirtmek için atanır. Satış siparişi tutma kodları **Satış ve pazarlama** &gt; **Kurulum** &gt; **Satış siparişleri** &gt; **Sipariş tutma kodları**'nda yapılandırılır. Bir satış siparişi oluşturma zamanında veya sonra el ile beklemeye alınabilir. Ayrıca, sipariş otomatik olarak, dolandırıcılık kurallarına göre beklemeye alınabilir. Bir satış siparişi beklemedeyken bilgilerle güncelleştirmeniz gerekebilir. Alternatif olarak, üzerinde çalışmaya devam ederken satış siparişini denetlemek isteyebilirsiniz. Bir satış siparişi denetleyebilirsiniz, yeniden kaydedebilirsiniz ve hatta sipariş bekletme çalışma ekranını kullanarak başka bir kullanıcının denetlemesini geçersiz kılabilirsiniz (**Perakende** &gt; **Müşteriler** &gt; **Sipariş tutmaları**). Siparişin tamamlanması hazır olduğunda, sipariş işlemini tamamlamadan önce tutma kaldırmanız gerekir.




