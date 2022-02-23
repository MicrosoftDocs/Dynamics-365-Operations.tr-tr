---
title: Bakım bütçeleri oluşturma
description: Bu konuda Varlık Yönetimi'nde bakım bütçesi oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 602a00060c1e56285d9954981d019bececaf90fd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021001"
---
# <a name="create-maintenance-budgets"></a>Bakım bütçeleri oluşturma

[!include [banner](../../includes/banner.md)]

 



Bakım bütçeleri, önleyici bakım için beklenen maliyetlere genel bir bakış sağlamak için kullanılır. Bütçe satırları, bütçe dönemi içinde beklenen başlangıç tarihinin bulunduğu bakım zamanlaması satırları temel alınarak hesaplanır.

Bakım bütçeleri, Varlık Yönetimi'nde kullanılan maliyet türlerini temel alır: **Önleyici**, **Düzeltici** ve **Yatırım**. Yatırım bakımı için bütçe maliyetleri, bütçe dönemindeki değiştirme tarihinin ve ilgili değişiklik değerinin bulunduğu etkin varlıklar için dahil edilir. Geçmiş düzeltme tarihi bütçe hesaplamasına dahilse düzeltici bakım için bütçe maliyetleri dahil edilir. Bu durumda önceki bir döneme ait düzeltici maliyetler, bakım bütçesini hesapladığınız aynı gelecek dönem için hesaplanır.

## <a name="create-a-maintenance-budget"></a>Bakım bütçesi oluşturma

1. **Varlık yönetimi** \> **Sorgular** \> **Bakım bütçesi** \> **Bütçe**'yi seçin.
2. **Bütçe oluştur**'u seçin.
3. **Bakım bütçesi** alanına bir bütçe kimliği girin.
4. **Açıklama** alanına bir açıklama girin.
4. **Dönem** hızlı sekmesinde, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına bütçe döneminin başlangıç ve bitiş tarihlerini girin.
5. Önceki bir dönemde fiili maliyetler temel alınarak hesaplanan düzeltici bütçe maliyetlerini dahil etmek için **Düzeltici başlangıç tarihi** alanına, bu maliyetlerin dahil edileceği dönemin başlangıç tarihini girin.
6. Bütçede gereken ayrıntı düzeyine bağlı olarak beş **Gruplama ölçütü** hızlı sekmesinde ilgili seçenekleri ayarlayın.
7. **Tamam**'ı seçin.
8. **Bütçe satırları**'nı seçerek **Bakım bütçesi satırları** sayfasını açın, burada dönem için oluşturulan tüm bütçe satırlarını görüntüleyebilirsiniz.
9. Bütçeyi onaylamak için **Bakım bütçeleri** sayfasından bütçeyi ve ardından **Onayla**'yı seçin. Ardından **Bütçeyi onayla** iletişim kutusunda, **Tamam**'ı seçin. Adınız **Bakım bütçeleri** sayfasındaki **Onaylayan** alanına girilir.

    > [!NOTE]
    > Bakım bütçesini onayladıktan sonra önce onayı kaldırmadığınız sürece **Bakım bütçesi satırları** sayfasındaki ilgili satırları yeniden hesaplayamaz veya ayarlayamazsınız. Bakım bütçesinin onayını kaldırmak için **Bakım bütçeleri** sayfasından bütçeyi ve ardından **Onayla**'yı seçin. Ardından **Bütçeyi onayla** iletişim kutusunda, **Tamam**'ı seçin.

![Bakım Bütçeleri](media/01-maintenance-budgets.png)

Ayrıca mevcut bütçeyi kopyalayarak yeni bir bakım bütçesi oluşturabilirsiniz. **Bakım bütçeleri** sayfasında, kopyalanacak bütçeyi ve ardından **Kopyala**'yı seçin. Bu yaklaşım, örneğin bir aylık bir bütçe oluşturduğunuzda ve bunu diğer aylara kopyalamak istediğinizde yararlıdır.

> [!NOTE]
> Bakım bütçesi yalnızca bakım zamanlaması satırlarını temel alan bütçe maliyetlerini hesaplar. Aynı dönemdeki fiili maliyetleri **Varlık maliyeti denetimi** sayfasında hesaplayabilirsiniz. 
