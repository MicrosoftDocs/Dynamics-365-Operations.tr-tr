---
title: Varlık Ürün Reçeteleri
description: Bu konuda, Varlık yönetimi'ndeki varlık ürün reçeteleri (BOM) açıklanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0430891607ac4558c91b86318aee318d0076007daf59a32eda65cb411d274b3a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751997"
---
# <a name="asset-boms"></a>Varlık Ürün Reçeteleri

[!include [banner](../../includes/banner.md)]

 

Bu konuda, Varlık yönetimi'ndeki varlık ürün reçeteleri (BOM) açıklanmaktadır. **Varlık Ürün Reçetesi** sayfası, tüm kullanım ömrü boyunca bir varlık üzerinde kullanılan tüm öğelerin (yedek parça ve diğer öğeler) listesini gösterir. Yeni bir varlık oluşturduğunuzda, kurulum yordamının bir parçası olarak bir varlık ürün reçetesi ayarlamayı düşünmelisiniz. Bu şekilde, varlık için madde geçmişini oluşturma tarihinden itibaren takip edebilirsiniz.

Bir bakım işini tamamladıktan ve madde tüketimi bir iş emrinee kaydettikten sonra, varlık üzerinde kullanılan yedek parça ve diğer maddelerin tüketimini izleyebilirsiniz. Bu işlev, tüm varlıklarınız için tam bir madde tüketim kaydı tutmanızı sağlar. Örneğin, belirli bir yedek parçanın sıklıkla değiştirilip değiştirilmediğini izlemek veya bir varlık üzerinde kullanılmakta olan yedek parçaları veya diğer maddeleri izlemek için bu kaydı kullanabilirsiniz.

> [!NOTE]
> İş emrinde, madde tüketimi hem yedek parçaları hem de yağlama maddeleri, cıvatalar ve contalar gibi diğer ek maddeleri içerebilir.

Bir varlık ürün reçetesi, Varlık Yönetimi'ndeki kurulumuna göre otomatik olarak güncelleştirilebilir. Sonlandırılmış veya tamamlanan iş emirlerini işlemek için bir iş emri yaşam döngüsü durumu oluşturulduysa ve bu iş emri yaşam döngüsü durumu için **İş emri yaşam döngüsü durumları** sayfasında **Varlık ürün reçetesini güncelleştir** seçeneği **Evet** olarak ayarlandıysa, iş emri bu yaşam döngüsü durumuna güncelleştirildiğinde iş emrinde kullanılan tüm maddeler **Varlık ürün reçetesi** sayfasında otomatik olarak güncelleştirilir. 


Ayrıca, **Varlık ürün reçetesi** sayfasında yeni madde satırları oluşturarak bir varlık ürün reçetesini el ile de güncelleştirebilirsiniz.

**Varlık ürün reçetesi** sayfasında, madde tüketimi bir iş emrine kaydedildikten sonra varlıklar için yedek parça geçmişini izleyebilirsiniz. Bu işlevi kullanmak için, **Yedek parça madde grupları** sayfasında yedek parça kaydı için kullanılması gereken madde gruplarını seçmeniz gerekir.

Varlık ürün reçetesi işlevini kullanmak için, önce gerekli yedek parça madde gruplarını ayarlamanız gerekir. Daha sonra, bir iş emri tamamlandığında varlık ürün reçetesinin otomatik olarak güncelleştirilmesini istiyorsanız, bu güncelleştirmeyi işlemek için bir iş emri yaşam döngüsü durumu ayarlayabilirsiniz. 


## <a name="set-up-spare-parts-item-groups"></a>Yedek parça madde gruplarını ayarlama

Yedek parça geçmişi kurulumu, **Stok ve ambar yönetimi** modülünde oluşturulan madde gruplarını temel alır. Varlık Yönetiminde, seçili madde gruplarındaki maddelerin yedek parça geçmişini izleyebilebilmek için madde gruplarını ayarlayın.

1. **Varlık yönetimi** \> **Kurulum** \> **Varlık** \> **Yedek parça madde grupları**'nı seçin.
2. Bir madde grubu ayarlamak için **Yeni**'yi seçin.
3. **Madde grubu** alanında grubu seçin. Grubun adı otomatik olarak **Ad** alanına girilir.

## <a name="view-and-update-asset-boms"></a>Varlık ürün reçetelerini görüntüleme ve güncelleştirme

Bir iş emrindeki madde tüketimini deftere naklettikten sonra, **Varlık ürün reçetesi** sayfasında kayıtlı madde tüketimini görüntüleyebilirsiniz.

1. **Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Etkin varlıklar**'ı seçin. Listeden varlığı seçin ve ardından **Varlık ürün reçetesi**'ni seçin.

    > [!NOTE]
    > Tüm varlıklardaki tüm madde tüketim kayıtlarını görüntülemek için, **Varlık yönetimi** \> **Sorgular** \> **Varlıklar** \> **Varlık ürün reçetesi**'ni seçin.

2. **Varlık ürün reçetesini güncelleştir**'i seçin. **Seç** öğesini seçerek, güncelleştirmeye gereksinim duyduğunuz varlıkları, varlık türlerini ve kaynakları ekleyebilirsiniz. Güncelleştirmeyi başlatmak için **Tamam**'ı seçin. Güncelleştirme işlevini bir toplu iş olarak da ayarlayabilirsiniz.
3. Maddelerle ilgili daha fazla bilgi görmek isterseniz, stok boyutları ekleyebilirsiniz. **Stok** \> **Boyutlar görünümü**'nü seçin ve ardından görmek istediğiniz boyutların onay kutularını işaretleyin. Bu ayarı **Varlık Ürün Reçetesi** sayfasındaki tüm varlıklar için korumak amacıyla **Ayarı kaydet** seçeneğini **Evet** olarak ayarlayın.
4. Varlık Yönetiminde seçilen satırdaki maddenin varlıklar, iş türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin. 
5. Yalnızca etkin madde satırlarını görmek istiyorsanız, **Görüntüle** \> **Geçerli**'yi seçin. Bitiş erme tarihi geçerli tarihten önce olan satırlar dahil olmak üzere tüm madde satırlarını görmek için **Görüntüle** \> **Tümü**'nü seçin.

> [!NOTE]
> Bir iş emrini tamamladığınızda, ilişkili varlıkla ilgili bazı madde veya yedek parçaların süresi dolmuşsa veya başka maddeler veya yedek parçalarla değiştirilmişse, varlık ürün reçetesini buna göre güncelleştirmeniz önerilir.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Varlık ürün reçetesinde yeni madde satırı oluşturma

Varlıklar için el ile madde satırları oluşturabilirsiniz.

1. **Varlık ürün reçetesi** sayfasında, **Yeni**'yi seçin.
2. **Varlık** alanında, madde satırı eklenecek varlığı seçin.
3. **Satır numarası** alanına sıralı bir satır numarası girin.
4. **Etkin** alanına madde için bir başlangıç tarihi girin.
5. Maddenin süresi dolacaksa, **Bitiş** alanına bir bitiş tarihi girin.
6. **Madde numarası** alanında maddeyi seçin. Ad **Ürün adı** alanına otomatik olarak girilir.
7. **Miktar** alanına kullanılan miktarı girin. **Birim** alanı otomatik olarak güncelleştirilir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]