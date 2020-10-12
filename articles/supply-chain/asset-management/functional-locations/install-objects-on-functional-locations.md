---
title: Varlıkları işlem yapılacak yerleşimlere yükleme
description: Bu konuda Varlık Yönetimi'nde varlıkları işlem yapılacak yerleşimlere yükleme işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85b9f473cc725896a00501510eea02d7cfb21782
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888883"
---
# <a name="install-assets-on-functional-locations"></a>Varlıkları işlem yapılacak yerleşimlere yükleme

[!include [banner](../../includes/banner.md)]

 

İşlem yapılacak yerleşim yapıları oluşturduktan sonraki adım, varlıkları ilgili işlem yapılacak yerleşimlere yüklemektir. Bu konuda Varlık Yönetimi'nde varlıkları bu işlem yapılacak yerleşimlere yükleme işlemi açıklanmaktadır. Varlık oluşturma hakkında bilgi için bkz. [Varlıklara giriş](../objects/introduction-to-objects.md).

Bir varlık yapısı oluşturduysanız, tüm varlık yapısının işlem yapılacak yerleşime yüklenmesi gerekir. Bu nedenle, işlem yapılacak yerleşimde yalnızca üst varlıklar (üst varlığı olmayan üst düzey varlıklar) seçilebilir. İlgili tüm alt varlıklar (alt varlıklar) da işlem yapılacak yerleşime yüklenecektir. Varlıkları işlem yapılacak yerleşime yüklediğinizde, işlem yapılacak yerleşimin mali boyutları işlem yapılacak yerleşim için seçilen işlem yapılacak yerleşim türündeki ayara bağlı olarak otomatik olarak varlıklara aktarılabilir. İşlem yapılacak yerleşim türlerini ayarlamayla ilgili daha fazla bilgi için bkz. [İşlem yapılacak yerleşim türleri](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> İşlem yapılacak yerleşim için kullanılan işlem yapılacak yerleşim türünde varlık türlerini ayarlayabilirsiniz. Bu durumda, işlem yapılacak yerleşimde varlıklar yüklediğinizde, yalnızca aynı varlık türüne sahip üst varlıklar işlem yapılacak yerleşime yüklenebilir varlıklar listesinde gösterilir.

Varlıkları işlem yapılacak yerleşime yükledikten sonra, bir üst varlığı veya bir varlık yapısını gerektiğinde değiştirebilirsiniz. Varlıkları yüklediğinizde, değiştirilecek bir üst varlık seçin. İlgili tüm alt varlıklar da değiştirilecektir. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Varlık yapısını işlem yapılacak yerleşime yükleme

1. **Varlık yönetimi** \> **Genel** \> **İşlem yapılacak yerleşimler** \> **Tüm işlem yapılacak yerleşimler** veya **Etkin işlem yapılacak yerleşimler**'i seçin.
2. Varlığın yükleneceği işlem yapılacak yerleşimi seçin.
3. **Varlık yükle**'yi seçin.

    **Öznitelikler** bölümü, işlem yapılacak yerleşim için seçilen işlem yapılacak yerleşim türünde ayarlanan varlık öznitelik gereksinimlerinin listesini gösterir. Öznitelikler yalnızca bilgi amaçlıdır. Sistem, öznitelikleri yüklediğiniz varlık üzerinde ayarlanan varlık özniteliklerine karşı doğrulamaz. **Varlık** alanında bir varlık seçtikten sonra bu doğrulamayı yapmanız gerekir.

4. **Varlık** alanında, yüklenecek üst varlığı seçin. İlgili tüm alt varlıklar otomatik olarak yüklemeye eklenir.

    Varlık listesinin sağındaki **Varlık öznitelikleri** bölümü, seçili varlıkla ilgili varlık özniteliklerini gösterir.

5. **Etkin** alanında, varlık yüklemesinin geçerli olmaya başladığı tarih ve saati seçin. Bu tarih ve saatten sonra, varlık ve ilgili alt varlıklar için maliyetler işlem yapılacak yerleşimle ilgili olacaktır.

    > [!NOTE]
    > Varlık üzerinde ayarlanan varlık öznitelikleri **Öznitelikler** bölümüne eklenir. Örneğin, **Ağırlık** öznitelik gereksinimi hem varlık hem de işlem yapılacak yerleşimde bir gereksinim olarak eklenmiştir. Varlığın işlem yapılacak yerleşimle aynı türde öznitelik gereksinimleri varsa, varlığın öznitelik gereksinimlerinin değerleri **Değer** alanlarına girilir. Bu nedenle, varlık değerlerini işlem yapılacak yerleşimde ayarlanan öznitelik gereksinimlerine karşı doğrulayabilirsiniz. İşlem yapılacak yerleşimde ayarlanan öznitelik gereksinimleri onay işareti ile işaretlenir.

6. **Tamam**'ı seçin.

    > [!NOTE]
    > Bir varlığın yüklemesini yeni bir işlem yapılacak yerleşime yükleyerek değiştirmek için, bu yordamın 1 ile 6 arasındaki adımlarını izleyin. Bir varlığı yeni bir işlem yapılacak yerleşime yüklediğinizde, varlık önceki işlem yapılacak yerleşimden otomatik olarak kaldırılır. Yeni bir işlem yapılacak yerleşime yüklemeden önce varlık üzerinde oluşturulan tüm etkin bakım istekleri veya iş emirleri otomatik olarak yeni işlem yapılacak yerleşime **aktarılmaz.** Bu bakım istekleri ve iş emirleri varlık için hala gerekliyse, varlık yeni yerleşime yüklendikten sonra bunları el ile yeniden oluşturmanız gerekir.

7. İşlem yapılacak yerleşimde yüklü olan alt varlıklar da dahil olmak üzere tüm varlıkların listesini görüntülemek için, **Tüm işlem yapılacak yerleşimler** sayfasında işlem yapılacak yerleşimi seçin ve ardından **Varlıklar**'ı seçin.
8. Etkin bakım isteklerinin, etkin iş emirlerinin veya işlem yapılacak yerleşimde yüklü olan varlıklarla ilgili hata kayıtlarının listesini görüntülemek için, **Tüm işlem yapılacak yerleşimler** sayfasında işlem yapılacak yerleşimi ve ardından **İstekleri**, **İş emirlerini** veya **Hatalar**'ı seçin.

> [!NOTE]
> Varlıkla ilgili veriler değiştiğinde, varlığın yüklü olduğu işlem yapılacak yerleşimde otomatik olarak güncelleştirilir. Bu otomatik güncelleştirme bakım istekleri, iş emirleri, varlık arıza kayıtları, bakım kesinti kayıtları ve varlık ölçü kayıtları değişiklikleriyle ilgilidir.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>İşlem yapılacak yerleşimde otomatik olarak bir varlık oluşturma

İşlem yapılacak yerleşimde *bir* varlığın otomatik olarak oluşturulması işlemini gerçekleştirmek için işlem yapılacak yerleşim aşamaları ve işlem yapılacak yerleşim türleri ayarlayabilirsiniz. Varlık, işlem yapılacak yerleşimle aynı kimliği ve adı alır. Bu işlev, bir bina gibi büyük ve statik bir varlık üzerinde bakım işlemi yaparken yararlı olabilir.

İşlem yapılacak yerleşimde otomatik olarak bir varlık oluşturmadan önce, aşağıdaki kurulum verilerinin kullanılabilir olması gerekir:

- Bir varlığın otomatik olarak oluşturulmasını gerçekleştirmek için işlem yapılacak yerleşim türü oluşturun. **Kıymet türü** alanında bir kıymet türü seçin. Daha fazla bilgi için bkz. [İşlem yapılacak yerleşim türleri](../setup-for-functional-locations/functional-location-types.md).
- Bir varlığın otomatik olarak oluşturulmasını gerçekleştirmek için işlem yapılacak yerleşim yaşam döngüsü durumu oluşturun. **Varlık oluştur** seçeneğini **Evet** olarak ayarlayın. Daha fazla bilgi için bkz. [İşlem yapılacak yerleşim yaşam döngüsü durumları](../setup-for-functional-locations/functional-location-stages.md).

Kurulum verileri kullanılabilir olduktan sonra bir varlık oluşturmaya hazır olursunuz.

1. **Tüm işlem yapılacak yerleşimler** sayfasında, varlığın otomatik olarak oluşturulmasını istediğiniz işlem yapılacak yerleşimin, bu amaçla oluşturduğunuz işlem yapılacak yerleşim türünü kullandığından emin olun.
2. Listeden işlem yapılacak yerleşimi seçin.
3. **İşlem yapılacak yerleşim durumunu güncelleştir**'i ve ardından bu amaçla oluşturduğunuz yaşam döngüsü durumunu seçin. Bir varlık artık işlem yapılacak yerleşime otomatik olarak yüklenir. Bu varlık, işlem yapılacak yerleşimle aynı ada sahip olur.
