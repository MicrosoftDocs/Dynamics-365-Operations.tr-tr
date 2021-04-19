---
title: Varlıkları taşıma, değiştirme ve yükleme
description: Bu konuda Varlık Yönetimi'nde varlıkların nasıl taşınacağı, değiştirileceği ve yükleneceği açıklanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6d7a9c86029505602c562a3de4d2f52eace866f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808556"
---
# <a name="move-replace-and-install-assets"></a>Varlıkları taşıma, değiştirme ve yükleme

[!include [banner](../../includes/banner.md)]

 

Bu konuda Varlık Yönetimi'nde varlıkların nasıl taşınacağı, değiştirileceği ve yükleneceği açıklanmaktadır. Başka varlıklarla ilişkisi olmayan bağımsız varlıklar oluşturabilir veya bir üst varlık (en üst düzey varlık) ve ilgili alt varlıklar (alt varlıklar) içeren bir varlık yapısı oluşturabilirsiniz. Varlık Yönetiminde, bir varlığın yerleşimini taşımak ve değiştirmek için üç yaklaşım vardır:

- **Taşı**: Varlığı başka bir varlık yapısına veya aynı varlık yapısındaki başka bir yerleşime taşıyın.
- **Değiştir**: Bir varlığı onarılması veya yenilenmesi için bir varlık yapısından geçici olarak kaldırın ve yenilenen varlığı daha sonra varlık yapısına geri ekleyin. Alternatif olarak, kullanılan varlığı kalıcı olarak yeni bir varlıkla değiştirin.
- **Yükle**: İşlem yapılacak yerleşime bir üst varlık ve ilgili alt varlıkları yükleyin.

> [!NOTE]
> Taşıdığınız, değiştirdiğiniz veya yüklediğiniz varlık başka bir işlem yapılacak yerleşimle ilişkili olabilir. Bu durumda, varlık işlem yapılacak yerleşimin mali boyutlarını kullanabilir. **İşlem yapılacak yerleşim türleri** sayfasında, işlem yapılacak yerleşimlerdeki mali boyutların işlenmesini ayarlarsınız.

## <a name="move-asset"></a>Varlığı taşı

Varlığı başka bir varlık yapısına veya aynı varlık yapısındaki başka bir yerleşime taşımak için **Varlığı taşı** işlevini kullanın. Ayrıca, bir varlığı varlık yapısının dışına taşıyarak yapı ilişkileri içermeyen bağımsız bir varlık haline gelmesini sağlayabilirsiniz.

> [!NOTE]
> Varlıklar onarılıyorsa veya geçici olarak değiştiriliyorsa bu işlevi kullanmayın. Bunun yerine, bu konunun ilerleyen kısımlarında açıklanan **Varlığı değiştir** işlevini kullanın.

1. **Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**'ı seçin.
2. Listede, taşınacak varlığı seçin. Varlığın alt varlıkları varsa, bu varlıkları da taşırsınız.
3. **Varlığı taşı**'yı seçin.
4. Varlığı bir varlık yapısının parçası olacak şekilde taşımak için **Üst varlık** alanında yeni üst varlığı seçin. Bir alt varlığı taşıyorsanız ve bunu yapı ilişkileri bulunmayan bağımsız bir varlık yapmak istiyorsanız, **Üst varlık** alanını boş bırakın.
5. Varsayılan olarak **Etkin** alanı mevcut tarih ve saate ayarlanır. Ancak, varlık taşıma geçerlilik başlangıcı olarak farklı bir tarih ve saat seçebilirsiniz.
6. **Tamam**'ı seçin.

## <a name="replace-asset"></a>Varlığı değiştir

Onarımlar, yenileme veya aşınmış bir varlığın yeni bir varlıkla kalıcı şekilde değiştirilmesiyle ilgili olarak **Varlığı değiştir** işlevini kullanın. Bu işlev, bir varlık yapısındaki alt varlıkları değiştirmek için kullanılır. Üst varlıklar için (henüz bir üst varlığı bulunmayan varlıklardır), bu değişiklik işlem yapılacak yerleşimde yapılır. Alt varlıkların işlem yapılacak yerleşimde nasıl değiştirileceği hakkında daha fazla bilgi için bkz. [Varlıkları işlem yapılacak yerleşimlere yükleme](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Onarım atölyesi üretim departmanınızla ilişkiliyse, varlıkların onarımı ve değişimini gerçekleştirmek için **Onarım**, **Hurda** ve **Depolama** gibi işlem yapılacak yerleşimler oluşturabilirsiniz.

1. **Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**'ı seçin.
2. Listede, değiştirilecek alt varlığı seçin. Varlığın alt varlıkları varsa, bu varlıkları da değiştirirsiniz.
3. **Varlığı değiştir**'i seçin.

    **Yapı değiştirme** alanı, seçilen varlıkların ve ilgili alt varlıkların varlık yapısında taşındığı son tarihi ve saati gösterir.

4. **Seçili varlık** bölümünde, **Hedef işlem yapılacak yerleşim** alanında, varlığın taşınacağı işlem yapılacak yerleşimi seçin. Örneğin, **Onarım** veya **Iskarta** yerleşimini seçin.

    **Üst varlık** bölümünde, **Etkin** alanı üst varlığın ve ilgili alt varlıkların geçerli işlem yapılacak yerleşime yüklendiği veya taşındığı son tarih ve saati gösterir.

5. **Yeni varlık** bölümünde, **Varlık** alanında, seçili varlık için geçici veya kalıcı değişiklik olarak eklenecek varlığı seçin. Bu varlık halihazırda **Depolama** gibi başka bir işlem yapılacak yerleşimde bulunuyor olabilir.
7. **Yürürlük başlangıcı** bölümünde, **Etkin** alanı varsayılan olarak geçerli tarihe ve saate ayarlanır. Ancak, varlık değiştirme geçerlilik başlangıcı olarak farklı bir tarih ve saat seçebilirsiniz.
8. **Tamam**'ı seçin.

## <a name="install-asset"></a>Varlık yükle

Bir işlem yapılacak yerleşime varlık yapısı yüklemek için **Varlık yükle** işlevini kullanın.

> [!NOTE]
> Her zaman bir üst varlık seçin. Üst varlık ve ilgili alt varlıklar seçili işlem yapılacak yerleşime taşınır.

1. **Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**'ı seçin.
2. Listede, başka bir işlem yapılacak yerleşime yüklenecek üst varlığı seçin.
3. **Varlık yükle**'yi seçin.

    **Öznitelikler** bölümü üst varlık üzerinde ayarlanan varlık özniteliklerini gösterir.

4. **İşlem yapılacak yerleşim** alanında, yeni yerleşimi seçin.
5. Varsayılan olarak **Etkin** alanı mevcut tarih ve saate ayarlanır. Ancak, varlık yapısına yapılan yüklemenin geçerlilik başlangıcı olarak farklı bir tarih ve saat seçebilirsiniz.
6. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]