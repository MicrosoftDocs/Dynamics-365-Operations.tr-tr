---
title: İşlem yapılacak yerleşim türleri
description: Bu konu Varlık Yönetimi'nde işlem yapılacak yerleşim türleri oluşturma işlemini açıklar.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c64a0c07bf692385370e4bd2a99f51b211cd397
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018715"
---
# <a name="functional-location-types"></a>İşlem yapılacak yerleşim türleri

[!include [banner](../../includes/banner.md)]

 

Bu konu Varlık Yönetimi'nde işlem yapılacak yerleşim türleri oluşturma işlemini açıklar. İşlem yapılacak yerleşim türleri, varlıkların işlem yapılacak yerleşime nasıl yükleneceği de dahil olmak üzere işlem yapılacak yerleşim gereksinimlerini yönetmek için kullanılır. Belirli işlem yapılacak yerleşim türünü kullanan işlem yapılacak yerleşimde kullanılacak varlık türlerini, bakım planlarını, işlem yapılacak yerleşim özniteliklerini ve varlık öznitelik gereksinimlerini ayarlayabilirsiniz. İşlem yapılacak yerleşim oluştururken, işlem yapılacak yerleşim türü zorunludur.

>[!NOTE] 
>İşlem yapılacak yerleşimlerle çalışmak için, yalnızca yeni varlıklar oluşturmak amacıyla kullanılmak üzere varsayılan bir işlem yapılacak yerleşim oluşturmanız gerekir. Bu varsayılan işlem yapılacak yerleşim için gerçekten basit olan ve birden çok varlığın varsayılan işlem yapılacak yerleşime yüklenmesini sağlayan bir varsayılan işlem yapılacak yerleşim türü oluşturmanız gerekir. İşlem yapılacak yerleşimleri ayarlamayla ilgili daha fazla bilgi için bkz. [İşlem yapılacak yerleşimler oluşturma](../functional-locations/create-functional-locations.md).

## <a name="create-a-default-functional-location-type"></a>Varsayılan işlem yapılacak yerleşim türü oluşturma

Bu yordam, varsayılan işlem yapılacak yerleşim için kullanılacak varsayılan işlem yapılacak yerleşim türünün nasıl oluşturulacağını gösterir.

1. **Varlık yönetimi** > **Kurulum** > **İşlem yapılacak yerleşimler** > **İşlem yapılacak yerleşim türleri**'ni seçin.
2. İşlem yapılacak yerleşim türü oluşturmak için **Yeni**'yi seçin.
3. **İşlem yapılacak yerleşim türü** alanına "Varsayılan" gibi bir işlem yapılacak yerleşim türü kodu girin ve **Ad** alanına adı girin.
4. **İşlem yapılacak yerleşim yaşam döngüsü modeli** alanında bir yaşam döngüsü modeli seçin.
5. Bu türü kullananan işlem yapılacak yerleşime (varsayılan işlem yapılacak yerleşim) daha fazla varlık yüklenmesine izin vermek için **Birden çok varlık** düğmesini "Evet"e getirin.

Şimdi, yalnızca varsayılan işlem yapılacak yerleşimde kullanılacak varsayılan işlem yapılacak yerleşim türü oluşturulur. Bu varsayılan işlem yapılacak yerleşim türüne daha fazla gereksinim veya kısıtlama eklemeniz gerekmez.


## <a name="create-functional-location-types"></a>İşlem Yapılacak Yerleşim Türleri Oluşturma

1. **Varlık Yönetimi** > **Kurulum** > **İşlem yapılacak yerleşimler** > **İşlem yapılacak yerleşim türleri**'ni seçin.
2. İşlem yapılacak yerleşim türü oluşturmak için **Yeni**'yi seçin.
3. **İşlem yapılacak yerleşim türü** alanına işlem yapılacak yerleşim türü kodunu ve **Ad** alanına adı girin.
4. **İşlem yapılacak yerleşim yaşam döngüsü modeli** alanında bir yaşam döngüsü modeli seçin. İşlem yapılacak yerleşim yaşam döngüsü durumları ve yaşam döngüsü modelleri hakkında daha fazla bilgi için bkz. [İşlem yapılacak yerleşim yaşam döngüsü durumları](../setup-for-functional-locations/functional-location-stages.md).
5. Bu işlem yapılacak yerleşim türünü kullananan işlem yapılacak yerleşime çeşitli varlıkların yüklenebilmesi gerekiyorsa **Birden çok varlık** düğmesini "Evet"e getirin. "Hayır" seçeneğini belirlerseniz, bu işlem yapılacak yerleşim türünü kullanan işlem yapılacak yerleşimde yalnızca *bir* varlık yükleyebilirsiniz.
6. Bu türdeki işlem yapılacak yerleşime yüklenen varlıkların otomatik olarak işlem yapılacak yerleşimle ilgili mali boyutları kullanmasını istiyorsanız **Varlık boyutunu güncelleştir** düğmesini "Evet" olarak ayarlayın. Bu, [İşlem yapılacak yerleşimler oluşturma](../functional-locations/create-functional-locations.md) formunda mali boyutları değiştirirseniz ve işlem yapılacak yerleşim bu geçiş düğmesi "Evet" olarak ayarlanmış bir işlem yapılacak yerleşim türü kullanıyorsa, mali boyutlar bu işlem yapılacak yerleşime yüklü olan tüm varlıklarda otomatik olarak güncelleştirilir anlamına gelir.
7. Oluşturduğunuz işlem yapılacak yerleşim ile aynı kod ve ada sahip işlem yapılacak yerleşim için otomatik olarak *bir* varlık oluşturmak istiyorsanız **Varlık türü** alanı kullanılır. Örneğin, bir yapı veya boru hattı gibi statik bir işlem yapılacak yerleşim oluşturuyorsanız, bu ilgili olabilir. Bu durumda, otomatik olarak oluşturulan varlık için kullanmak istediğiniz varlık türünü seçin. Bu alanda bir seçim yaparsanız, **Birden çok varlık** düğmesinin "Hayır" olarak ayarlanması gerektiğini unutmayın.
8. **Varlık türleri** hızlı sekmesinde, işlem yapılacak yerleşim türüyle ilgili varlık türlerini seçin. **Satır ekle**'yi ve varlık türlerini seçin. Burada varlık türleri eklerseniz, bu işlevsel konum türünü kullanarak yalnızca bu varlık türlerini kullanan varlıklar işlem yapılacak yerleşime yüklenebilir. **Varlık türleri** hızlı sekmesinde hiçbir varlık türü seçilmemişse, tüm varlık türleri yüklenebilir.
9. **Bakım planları** hızlı sekmesinde, bu işlem yapılacak yerleşim türünü kullanan yeni işlem yapılacak yerleşimlerde otomatik olarak ayarlanması gereken bakım planlarını seçin. **Satır ekle**'yi ve bakım planlarını seçin. Burada bakım planları eklerseniz, bu işlem yapılacak yerleşim türünü kullanan işlem yapılacak yerleşimde yalnızca bu planlar kullanılabilir.
10. **Varlık öznitelik gereksinimleri** hızlı sekmesinde, bu işlem yapılacak yerleşim türünü kullanan yeni işlem yapılacak yerleşimlerde otomatik olarak ayarlanması gereken varlık özniteliklerini ayarlayın. **Satır ekle**'yi ve özniteliği seçin. Bu öznitelik gereksinimleri yönergeler olarak işlev görür. Bir varlık üzerinde ayarlanan özniteliklere karşı doğrulanmazlar (**Varlık yönetimi** > **Genel** > **Varlıklar** > **Tüm varlıklar** > liste sayfasından varlığı seçin > **Genel** sekmesi > **Öznitelikler** düğmesi). Bu öznitelik gereksinimleri varlıkları işlem yapılacak yerleşimlere yüklerken gösterilir.
11. **İzin verilen türler** hızlı sekmesinde, seçili işlem yapılacak yerleşim türünü kullanan bir üst işlem yapılacak yerleşim türüyle ilgili alt işlem yapılacak yerleşim türleri için geçerli olması gereken işlem yapılacak yerleşim türlerini seçin.
12. **Öznitelikler** hızlı sekmesinde, bu işlem yapılacak yerleşim türünü kullanan işlem yapılacak yerleşimlerde otomatik olarak ayarlanması gereken işlem yapılacak yerleşim özniteliklerini seçin. **Satır ekle**'yi ve özniteliği seçin.


>[!NOTE] 
>**Genel** hızlı sekmesinde, işlem yapılacak yerleşim türünde ayarlanan varlık türleri, bakım planları, varlık öznitelik gereksinimleri, izin verilen türler, öznitelikler ve işlem yapılacak yerleşimlere ilişkin genel bir bakış alabilirsiniz. **İşlem yapılacak yerleşimler** alanı işlem yapılacak yerleşim türünü kullanan işlem yapılacak yerleşimlerin sayısını gösterir. Ayarları bir işlem yapılacak yerleşim türünden seçili işlem yapılacak yerleşim türüne kopyalamak için **Kopyala** düğmesini kullanabilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]