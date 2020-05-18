---
title: Proje bütçeleri için tahmin modelleri oluşturma
description: Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklamaktadır.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321791"
---
# <a name="create-forecast-models-for-project-budgets"></a>Proje bütçeleri için tahmin modelleri oluşturma 

[!include [banner](../includes/banner.md)]

Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklamaktadır. Bütçe denetimine tabi olan bir proje, iki tür bütçe kullanır: orijinal ve kalan. Bir proje bütçesi oluşturduğunuzda, **Tahmin modelleri** sayfasında oluşturulan orijinal ve kalan bütçe tahmin modellerini belirtmeniz gerekir. Belirtilen modellere dayalı proje bütçeleri, proje bütçesini kaydettiğinizde oluşturulur.

> [!NOTE]
> Bütçe denetimi için kullanılan bir tahmin modelinde alt model bulunamaz veya alt model olarak kullanılamaz.

1. **Proje yönetimi ve muhasebe** > **Kurulum** > **Tahminler**  > **Tahmin modelleri**'ni seçin.
2. Yeni bir tahmin modeli oluşturmak için **Yeni**'yi seçin ve yeni model için bir model kimlik numarası ve adı girin. 
3. Tahmin modeli için tahmin satırlarında herhangi bir değişiklik yapılmasını önlemek için **Durduruldu** seçeneğini **Evet** olarak ayarlayın. 
4. Modelin ilişkili olduğu tahmin satırlarının genel muhasebede nakit akışı tahminleri oluşturması gerekiyorsa **Nakit akışı tahminlerine dahil et**'i **Evet** olarak işaretleyin. 
5. Proje tarihini fatura tarihi olarak kullanmak için, **Tahmini Fatura tarihi**'ni **Evet** olarak ayarlayın. 
6. **Bütçe türü** alanında, aşağıdaki model türlerinden birini seçin:

   - **Orijinal bütçe**: İlk bütçe oluşturulduğunda ve onaylandığında kabul edilen orijinal bütçe tutarlarını kullanın.
   - **Kalan bütçe**: Projenin ömrü boyunca kalan bütçe tutarlarını kullanın. Bu tahmin modelindeki bakiyeler gerçek hareketler tarafından azaltılır ve bütçe revizyonları tarafından artırılır veya azaltılır.
   - **İleri taşı**: Projeyle ilgili İleri taşıma bütçe tutarlarını kullanın. İleri taşıma, kullanılmayan bütçe tutarlarını bir mali yıldan diğerine aktarmak için çalıştırılabilecek, isteğe bağlı bir işlemdir.

7. Aşağıdaki seçenekleri gerektiği gibi ayarlayın:

   - Proje tarihini fatura tarihi olarak kullanmak için **Tahmini fatura tarihi**'ni etkinleştirin.
   - **Süren iş ile tahmin**'i süren işe dayalı tahmin için etkinleştirin ve sonra süren iş türünü seçin. 
   - Varsayılan **Bütçe türü**'nü **Hiçbiri** olarak ayarlayabilir veya yeni bir tür girebilirsiniz. Bütçe türü bir kaydı değiştirdikten sonra değiştirilemez.     
    > [!NOTE]
    > Varsayılan bütçe türünü değiştirirseniz, diğer tüm seçenekler güncelleştirmeler için kullanılamaz hale gelir ve bu tahmin modelini yeniden kullanamazsınız. 
   


 

