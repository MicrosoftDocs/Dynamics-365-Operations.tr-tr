---
title: Önleyici bakıma genel bakış
description: Bu konuda Varlık Yönetimi'nde önleyici bakım açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 02ea3affca727802b241f87b801e0742ac0aa41a
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922103"
---
# <a name="preventive-maintenance-overview"></a>Önleyici bakıma genel bakış

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konuda Varlık Yönetimi'nde önleyici bakım açıklanmaktadır. Önleyici bakım, düzenli hizmet, kalibrasyon ve incelemeler gibi planlı bakım işlerinin dahil olduğu bir disiplindir. **Varlık Yönetimi**'nde, bakım planları oluşturabilir ve bunları varlıklarda ve işlem yapılacak yerleşimlerde ayarlayabilirsiniz. İşlem yapılacak yerleşimlerde bakım sıralarını da ayarlayabilirsiniz. Varlıklardaki bakım planları varlığın yüklü olduğu yerden bağımsız olarak etkindir. İşlem yapılacak yerleşimdeki bakım planları ve bakım sıraları yerleşimde şu anda yüklü olan varlıklar için etkindir. Varlıklarda bakım planları ayarlamak veya işlem yapılacak yerleşimlerde bakım sıraları ayarlamak yerine aynı iş rutininde ilgili bakım işi türlerini gerçekleştirmek istediğiniz birden çok varlığı içeren bakım sıraları oluşturabilirsiniz. İşlem yapılacak yerleşimlerde oluşturulmak yerine varlıklardan oluşturulan bakım sıraları, aynı işlem yapılacak yerleşime yüklenmeyen bir bakım sırası için varlık sayısını seçebileceğiniz anlamına gelir.

Bakım planları tek bir varlıkta önleyici ve reaktif bakım için kullanılır. Bakım sıraları, bir varlık grubu veya kümesinde önleyici bakım için kullanılır. Bakım planları ve bakım sıraları, iş emri teklifleri oluşturmak için kullanılır. İş emri teklifleri, paketlenebilen ve iş emirlerine dönüştürülebilen bakım zamanlaması satırları olarak kaydedilir.

Aşağıdaki çizimde, bakım planları ve bakım sıralarını temel alarak bakım planları ve bakım sıraları oluşturmaktan varlıklar için iş emirleri oluşturmaya kadar iş akışına bir genel bakış sunulmuştur.

![Şekil 1](media/01-preventive-maintenance.png)

