---
title: "Pozitif ödemeye genel bakış"
description: "Bu makalede bir bankaya sunulabilecek çeklerin bir elektronik listesinin oluşturulması için kullanılan pozitif ödemeler hakkında bilgi verilmiştir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 7c60a7f9444913c5475d08f959944d463cfcbab0
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="positive-pay-overview"></a>Pozitif ödemeye genel bakış

[!include[banner](../includes/banner.md)]


Bu makalede bir bankaya sunulabilecek çeklerin bir elektronik listesinin oluşturulması için kullanılan pozitif ödemeler hakkında bilgi verilmiştir. 

Pozitif ödeme, bir bankaya sunulabilecek çeklerin bir elektronik listesinin oluşturulması için kullanılır. Pozitif ödeme dosyaları, bankaların çek sahteciliğini önlemesine yardımcı olabilir. Çeklerin her yazıldığında çeklerin bir elektronik listesini oluşturmak için pozitif ödemeyi oluşturursunuz. Ardından, bankaya bir çek sunulduğunda, banka bu çeki daha önce göndermiş olduğunuz çek listesiyle karşılaştırır. Çek, çek listesindeki bir çekle uyuşuyorsa banka çeki serbest bırakır. Çek, listedeki bir çekle uyuşmuyorsa banka, çeki gözden geçirmek için tutar.

Pozitif ödeme SafePay olarak da bilinir. 

Pozitif ödeme dosyaları, alacaklar ve çek tutarları hakkında hassas bilgiler içermektedir. Bu nedenle, banka tarafından alınana kadar dosyaların oluşturulduğu süreden itibaren uygun güvenlik önlemlerini uyguladığınızdan emin olun. Pozitif ödeme dosyaları, web tarayıcısının karşıdan yükleme yönergelerine göre yüklenir. 

Pozitif ödeme dosyaları veri varlıkları kullanılarak oluşturulur. Bir pozitif ödeme dosyası oluşturmadan önce verileri bankanın işleme koyabileceği bir biçime dönüştüren XML için dönüştürme biçimlerini oluşturmanız gerekir. 

Pozitif ödeme bilgisi oluşturmak istediğiniz her bir banka hesabı için, pozitif ödeme biçimini atamanız gerekir. Ödemeleri oluşturduktan sonra tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturabilirsiniz. Alternatif olarak, birden fazla tüzel kişilik ve banka hesabı için aynı anda pozitif ödeme dosyaları oluşturabilirsiniz. 

Bir pozitif ödeme dosyasında listelenen çekler ödendikten sonra bankanızdan bir onay numarası alırsınız. Ardından, pozitif ödeme dosyasını Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümünde onaylayabilirsiniz. 

Bir pozitif ödeme dosyasını değiştirmeniz gerekiyorsa, bunu geri çağırabilirsiniz. Ardından, pozitif ödeme dosyasındaki her bir çek için, çekin bir pozitif ödeme dosyasına dahil edilip edilmeyeceğini gösteren alan sıfırlanır.

Daha fazla bilgi için bkz. [Pozitif ödeme dosyaları kurma ve oluşturma](set-up-generate-positive-pay-files.md).




