---
title: İş emri havuzları
description: Bu konuda Varlık Yönetimi'nde iş emri havuzlarıyla çalışma açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875946"
---
# <a name="work-order-pools"></a>İş emri havuzları


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Ortak bir şeyler içeren iş emirlerini gruplamak için iş emri havuzlarını kullanabilirsiniz. Örneğin, şunlar için bir iş emri havuzu oluşturabilirsiniz:

- iş ekibi, örneğin Bakım Ekibi, A, Bakım Ekibi B  

- profesyonel yetenekler, örneğin elektrikçi veya tesisatçı  

- fiziksel yerleşimler  

- zaman planlamaları, örneğin hafta veya diğer dönemler  


Gerekirse, bir iş emri birçok iş emri havuzuna yerleştirilebilir.


## <a name="create-work-order-pool"></a>İş emri havuzu oluşturma

**Tüm iş emri havuzlarında** veya **Etkin iş emri havuzlarında**, iş emri havuzlarınızın genel görünümünü alabilir ve yeni havuzlar oluşturabilirsiniz.

1. **Varlık yönetimi** > **Genel** > **İş emri havuzları** > **Tüm iş emri havuzları** veya **Etkin iş emri havuzları**'na tıklayın.

2. **Yeni**'ye tıklayın.

3. **Havuz** alanına bir iş havuzu kodu ve **Ad** alanına bir ad ekleyin.

4. İş emri havuzunun etkin olduğunu belirtmek için **Etkin** düğmesinde "Evet" seçeneğini belirleyin.

5. İş siparişlerinin otomatik olarak iş emri havuzundan kaldırılmasını istiyorsanız, **İş emri ilişkilerini sil** iki durumlu düğmesinde "Evet" seçeneğini belirleyin.

6. **Yaşam döngüsü durumunu sil** alanında, iş emri yaşam döngüsü durumunu seçin. Örneğin, bir iş emrini tamamlamaya yönelik iş emri yaşam döngüsü durumu, iş emri havuzlarının ilişkilerini otomatik olarak silecek şekilde ayarlanabilir.

7. İş siparişi havuzunuza iş emirlerini hemen eklemeye başlayabilirsiniz. **İş emirleri** hızlı sekmesinde **Satır ekle**'ye tıklayın.

8. **İş emri** alanında bir iş emri seçin. İlgili alanlar otomatik olarak güncelleştirilir.

9. Daha fazla iş emri eklemek istiyorsanız, 7-8 arasındaki adımları yineleyin.

10. **Sıralama düzeni** alanında, iş emirlerinin belirli bir sırada gerçekleştirilmesi gerekip gerekmediğini belirtebilirsiniz. Seçili iş emirleri için belirli bir sıra belirtmek üzere 1, 2, 3 ve bu şekilde sayılar ekleyin.

11. İş emri havuzuna dahil edilen tüm iş emirlerinin listesini görmek için **İş emirleri** düğmesine tıklayın.

12. Bakım zamanlaması, planlanmamış iş emirleri ve planlanan iş emirleri için kapasite yükünü hesaplamak ve görüntülemek üzere **Kapasite yükü**'nü açmak için **Kapasite yükü** düğmesine tıklayın.

13. Bakım zamanlaması, planlanmamış iş emirleri ve planlanan iş emirleriyle ilgili maddeler (yedek parçalar ve diğer gerekli maddeler) için tahminleri hesaplamak ve görüntülemek üzere **Madde tahmini**'ni açmak için **Madde tahmini** düğmesine tıklayın.

14. İş emri havuzundaki iş emirleriyle ilgili satın alma taleplerinin listesini görmek için **İş emri satınalma talebi** listesini açmak üzere **İş emri satın alma talebi** düğmesine tıklayın.

15. İş emri havuzundaki iş emirleriyle ilgili satın alma siparişlerinin listesini görmek için **İş emri satınalma** listesini açmak üzere **İş emri satınalma** düğmesine tıklayın.

>[!NOTE]
>Bir iş emri havuzu artık çalışma planınızla ilgili değilse, **İş emri havuzu** liste görünümünde bu havuz için **Etkin** onay kutusunu "Hayır" olarak ayarlayın.

Örneğin,daha sonra diğer iş emirleri için kullanabileceğiniz boş bir havuz oluşturmak üzere tüm iş emri satırlarını silmek istiyorsanız **İş emri ilişkilerini sil** onay kutusunu seçin. Daha sonra yeni iş emri ilişkileri oluşturmak için iş emri havuzunu kullanmak istiyorsanız **İş emri ilişkilerini sil** onay kutusunun işaretini kaldırmayı unutmayın.


![Şekil 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>İş emri havuzuna iş emri ekleme

Yukarıdaki bölümde açıklandığı gibi, havuzu oluştururken iş emri havuzuna iş emirleri ekleyebilirsiniz. Ayrıca **Tüm iş emirleri** listelerinin birinden iş emri havuzuna iş emri ekleyebilirsiniz.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. Listeden iş emrini seçin ve **İş emri havuzu**'na tıklayın.

3. **Ekle/kaldır** alanında "Ekle"yi seçin.

4. **Havuz** alanında iş emri havuzunu seçin.

5. **Tamam**'a tıklayın.

6. Bir iş emri havuzuna iş emri ekledikten sonra iş emrini havuzda belirli bir sıraya yerleştirmek isterseniz: İŞ emri havuzları liste sayfalarından birini açın, havuzu seçin ve **Düzenle**'ye tıklayın ve **İş emri havuzu** formu > **İş emirleri** hızlı sekmesi > **Sıralama düzeni** alanında havuza dahil edilen iş emirlerini sıralama düzenini ayarlayın.

Seçili iş emrini bir iş emri havuzundan kaldırmak isterseniz, Adım 3'te "Kaldır" öğesini seçin.

