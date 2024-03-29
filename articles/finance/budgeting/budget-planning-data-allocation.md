---
title: Bütçe planlaması veri tahsisatı
description: Bu makalede, Microsoft Dynamics 365 Finance'teki tahsisat yöntemleri ve bunların nasıl kullanılabileceği açıklanmaktadır.
author: panolte
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788f6dc8aa6cddad5c8eaba748827307a4d38a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901474"
---
# <a name="budget-planning-data-allocation"></a>Bütçe planlaması veri tahsisatı

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Finance'teki tahsisat yöntemleri ve bunların nasıl kullanılabileceği açıklanmaktadır.  

Kestirilen tutarları doğru şekilde değerlendirebilmek için bir bütçe planındaki verileri farklı şekillerde dağıtabilirsiniz.

## <a name="allocation-methods"></a>Tahsisat yöntemleri
Aynı bütçe planında bulunan satırlara dayalı olarak bütçe plan satırları oluşturulması için kullanılabilecek üç tahsisat yöntemi (Dönemler arasında tahsis et, Boyutlara tahsis et ve Genel muhasebe tahsisat kurallarını kullan) bulunmaktadır. Diğer bütçe planlarında bütçe planı satırları oluşturulması için kullanılabilecek üç yöntem (Toplama, Dağıtma ve Bütçe planından kopyalama) daha vardır. Altı tahsisat yönteminin her birinde hedef senaryoyu belirtirsiniz. Hedef senaryo, kaynak senaryoyla aynı veya kaynak senaryodan farklı olabilir. Ek olarak, yeni satırların bütçe planına dahil mi edileceğini, yoksa bütçe planındaki mevcut satırların yerini mi alacağını tanımlayabilirsiniz.

> [!NOTE] 
> Dağıtım veya daha önce ana planda gerçekleştirilen diğer değişiklikler için kullanılan senaryodan farklı bir toplam için benzersiz bir senaryo kullanılmalıdır.  

[![Dönemler genelinde tahsis etme tahsisat yöntemi.](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Dönemler genelinde tahsis et**: Bütçe planı satırlarını kaynak bütçe planı senaryosundan hedef senaryodaki dönemler genelinde tahsis etmek için bir dönem tahsisat kategorisi kullanılır. Kaynak tutarı, dönem tahsisat kategorisinde tanımlanan yüzdeye ve tarihe dayalı olarak hedef senaryodaki birden fazla satıra tahsis edilir.         

[![Boyutlara tahsis etme tahsisat yöntemi.](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Boyutlara tahsis et**: Bütçe planı satırları, seçilen bir bütçe tahsisat koşulunda tanımlanan yüzdelere ve mali boyutlara göre kaynak bütçe planlama senaryosundan hedef senaryodaki bir veya daha fazla satıra tahsis edilir.           

![Toplama grafiği.](./media/aggregatechart-300x230.png)
**Toplama**: Bütçe planı satırları, ilişkili (alt) bütçe planlarındaki kaynak bütçe planı senaryosundan ana bütçe planındaki hedef senaryoya toplanır. Bu yöntem, organizasyonun bir alt düzeyinde hazırlanan bütçe tutarlarının daha yüksek bir düzeyde birleştirilmesini sağlar.          

[![Dağıtma grafiği.](./media/distributechart-300x230.png)](./media/distributechart.png)
**Dağıt**: Bütçe planı satırları, ilişkili planların organizasyon birimlerinin mali boyutlarına göre ana bütçe planındaki kaynak bütçe planlama senaryosundan ilişkili (alt) bütçe planlarındaki hedef senaryoya dağıtılır. Bu yöntem, organizasyonun bir üst düzeyinde hazırlanan bütçe tutarlarının daha lokal bir değerlendirme için dağıtılmasını sağlar.           

[![Genel muhasebe tahsisat kuralları.](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Genel muhasebe tahsisat kurallarını kullan**: Bütçe planı satırları, seçilen genel muhasebe tahsisat kuralına göre kaynak bütçe planlama senaryosundan hedef senaryoya dağıtılır. 

[![Bütçe planından kopyalama.](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Bütçe planından kopyala**: Dağıtma tahsisat yönteminde olduğu gibi, ilgili bir bütçe planındaki satırlara göre hedefte bütçe planı satırları oluşturulur. Ancak, bu yöntem için, kaynak bütçe planının ana plan olması zorunlu değildir, bütçe planı hiyerarşisinde daha yüksek bir düzeyde bulunabilir. Bu tahsisat yöntemi, konsolide tutarların orijinal olarak çok yüksek bir düzeyde bütçelendiği ve daha üst düzeyde bir onay almadan önce ayrıntılı şekilde gözden geçirilmesi ve düzenlenmesi için organizasyonun daha alt bir düzeyine transfer edilmesinin gerektiği durumlarda kullanışlıdır.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Bir bütçe planında tahsisat yöntemlerini kullanma
Bütçe planı sayfasında tahsisatlar gerçekleştirmek için, tahsis edilecek satırları seçin ve ardından **Bütçeyi tahsis et** öğesini tıklayın.

[![Bütçe tahsis et düğmesi.](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Ardından, bir tahsisat yöntemi seçin. Kalan alanlar, seçtiğiniz yönteme dayalı olarak ayarlanır. Bu alanlara bütçe planı verilerinin kaynağı ve hedefi ve ayrıca toplu iş ayarının kolaylaşması açısından hedef tutarları oluşturulduğunda kaynağı belirtilen bir faktörle çarpmanıza izin veren bir seçenek dahildir. Ayrıca, **Planla ekle** seçeneğini de kullanabilirsiniz. Mevcut bütçe planı satırlarını değiştirmek için **Hayır** öğesini veya mevcut bütçe planı satırlarını tutmak ve tahsis edilen tutarlar için yeni satırlar eklemek için **Evet** öğesini seçin.

## <a name="automating-allocations-during-a-workflow"></a>Bir iş akışı sırasında tahsisatları otomatik hale getirme
Tahsisatların bir bütçe planlama iş akışının bir parçası olarak otomatik şekilde gerçekleştirilmesini sağlayan önemli bir özelliktir. Bir bütçe planı, iş akışından geçerken, otomatik hale getirilmiş görevler, belirtilen bir bütçe planlama aşamasında tahsisatı etkinleştirebilir. 

Otomatik tahsisatı ayarlamak için öncelikle **Bütçe planlama yapılandırma** sayfasından bir tahsisat programı oluşturmanız gerekir. Tahsisat programı, otomatik tahsisat çalıştırıldığında kullanılacak tahsisat yöntemini ve çeşitli tahsisat seçeneklerinin (açıklamalar için önceki bölüme bakın) değerlerini tanımlar. 

Ardından, **Bütçe Planlama Yapılandırma** sayfasından bir aşama tahsisatı oluşturursunuz. Aşama tahsisatı, bütçe planlama iş akışına ve aşamasına bir tahsisat programı atar. 

Son olarak, istediğiniz iş akışı aşamasında bütçe planlama aşama tahsisatı için bir otomatik görev ekleyin. Aşağıdaki örnekte, iş akışına iki adet bütçe planlama aşaması tahsisatı (kırmızı çerçeve içine alınmıştır) eklenmiştir.

[![Bütçe planlaması aşama tahsisatları.](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
