---
title: Varlık yönetimini sabit kıymetlerle tümleştirme
description: Bu konu, sabit kıymetleri bakım yapılan varlıklarla bağlamak için Varlık Yönetimi ve Sabit kıymetler modüllerinin nasıl tümleştirileceğini açıklamaktadır.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439189"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Varlık yönetimini sabit kıymetlerle tümleştirme

[!include [banner](../../includes/banner.md)]

**Varlık Yönetimi** ve **Sabit kıymetler** modüllerini tümleştirerek sabit kıymetler ile bakım yapılan varlıkları bağlayabilirsiniz. Sabit kıymet kullanıcıları daha sonra yeni veya varolan sabit kıymetten bir bakım yapılan varlık oluşturabilir ve Varlık yönetimi kullanıcıları bakım yapılan varlığı varolan bir sabit kıymetle ilişkilendirebilir. Bu özellik, Sabit kıymetler kullanıcılarının ilgili bakım varlıklarının iş emirlerinden deftere nakledilen maliyetleri görüntülemesini de kolaylaştırır.

> [!NOTE]
> Bu konuda, *bakım yapılan varlıklar* **Varlık Yönetimi** modülündeki varlıkları, *sabit kıymetler* ise **Sabit kıymetler** modülündeki varlıkları ifade eder.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Sabit kıymetlerden oluşturulan yeni bakım yapılan varlıklar için varsayılan konum ayarlama (isteğe bağlı)

Bu isteğe bağlı yapılandırma, sabit kıymetlerden oluşturulan yeni bakım yapılan varlıklar için varsayılan bir işlem yapılacak yerleşim ayarlamanıza olanak tanır. Tam olarak tamamlamanız koşuluyla bu yapılandırmayı tipik olarak yalnızca bir kez tamamlarsınız.

Bu yapılandırmayı tamamlamak için aşağıdaki adımları izleyin.

1. **Varlık yönetimi \> Kurulum \> Varlık yönetimi parametreleri**'ne gidin.
1. **Sabit kıymetler** sekmesinde, **İşlem yapılacak yerleşim** alanında, varsayılan yerleşimi seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Tümleştirilmiş bakım yapılan varlıklar ve sabit kıymetlerle çalışma

Bu bölümde, tümleşik Varlık yönetimi ve Sabit kıymetler özellikleriyle çalışabileceğiniz çeşitli yöntemleri gösteren bir grup yordam sağlanmaktadır.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Varolan bir bakım yapılan varlığı sabit kıymetle ilişkilendirme

Mevcut bir bakım yapılan varlığı sabit kıymetle ilişkilendirmek için aşağıdaki adımları izleyin.

1. **Varlık yönetimi \> Varlıklar \> Tüm varlıklar** (veya **Etkin varlıklar**'ı) seçin.
1. Bir varlık seçin.
1. **Sabit kıymet** hızlı sekmesinde, **Sabit kıymet numarası** alanında, mevcut bir sabit kıymeti seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Seçili bakım yapılan varlık ile ilişkilendirilen sabit kıymeti görüntüleme

Seçili bakım yapılan varlık ile ilişkilendirilen sabit kıymeti görüntülemek için aşağıdaki adımları izleyin.

1. **Varlık yönetimi \> Varlıklar \> Tüm varlıklar** (veya **Etkin varlıklar**'ı) seçin.
1. Bir varlık seçin.
1. **Sabit kıymet** hızlı sekmesinde, **Sabit kıymet numarası** alanında, bağlantıyı seçin.

    Seçili varlıkla ilgili **Sabit kıymetler** sayfası açılır. (Bu sayfa genellikle **Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler** konumunda bulunur.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Seçili sabit kıymetle ile ilişkilendirilen bakım yapılan varlığı görüntüleme

Seçili sabit kıymet ile ilişkilendirilen bakım yapılan varlığı görüntülemek için aşağıdaki adımları izleyin.

1. **Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.
1. Bir varlık seçin.
1. Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Görüntüle** grubunda **Bakım yapılan varlık** öğesini seçin.

    Seçili sabit kıymet ile ilişkilendirilen varlığın **Bakım yapılan varlık** sayfası açılır. (Bu sayfa genellikle **Varlık yönetimi \> Varlıklar \> Tüm varlıklar** konumunda bulunur.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Sabit kıymetle ilişkili bakım maliyetlerini görüntüleme

Varlık yönetimi iş emirleri bakım yapılan varlıklar için deftere nakledilebilir ve bu iş emirlerinin her biri genellikle bir maliyete sahiptir. Sabit kıymet bakım yapılan varlık ile ilişkilendirildiğinde, ilgili maliyetleri görmek için doğrudan sabit kıymetten gidebilirsiniz.

Sabit kıymet ile ilişkilendirilen bakım maliyetlerini görüntülemek için aşağıdaki adımları izleyin.

1. **Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.
1. Bir varlık seçin.
1. Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Görüntüle** grubunda **Bakım maliyeti** öğesini seçin.

    **Bakım maliyeti** sayfası açılır ve ilgili maliyetleri gösterir.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Mevcut bir sabit kıymet için yeni bir bakım yapılan varlık oluşturma

Mevcut bir sabit kıymet için yeni bir bakım yapılan varlık oluşturmak üzere aşağıdaki adımları izleyin.

1. **Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.
1. Bir varlık seçin.
1. Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Yeni** grubunda **Bakım yapılan varlık oluştur** öğesini seçin. (Bu seçenek kullanılamıyorsa, bakım yapılan varlık zaten seçili sabit kıymetle ilişkilendirilmiş olabilir.)
1. Varlık oluşturma işlemini [Varlık oluşturma](../objects/create-an-object.md)'da açıklandığı şekilde tamamlayın.

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Yeni sabit kıymet oluşturma ve bunun için yeni bir bakım yapılan varlık ekleme

Yeni bir sabit kıymet oluşturmak ve bunun için yeni bir bakım yapılan varlık eklemek üzere aşağıdaki adımları izleyin.

1. **Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Sabit kıymet oluşturma işlemini [Sabit kıymet oluşturma](../../../finance/fixed-assets/tasks/create-fixed-asset.md)'da açıklandığı şekilde tamamlayın.
1. Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Yeni** grubunda **Bakım yapılan varlık oluştur** öğesini seçin.
1. Varlık oluşturma işlemini [Varlık oluşturma](../objects/create-an-object.md)'da açıklandığı şekilde tamamlayın.

### <a name="remove-the-association-between-two-assets"></a>İki varlık arasındaki ilişkilendirmeyi kaldırma

Bazı durumlarda, bakım yapılan varlığın sabit kıymetiyle ilişkisini kaldırmanız gerekebilir. Örneğin, bir sabit kıymetten [yeni bir bakım yapılan varlık oluşturmak](#new-maintenance-from-fixed) istiyorsanız, önce mevcut ilişkilendirmeyi kaldırmalısınız.

Bakım yapılan varlık ile sabit kıymet arasındaki mevcut ilişkilendirmeyi kaldırmak için aşağıdaki adımları izleyin.

1. **Varlık yönetimi \> Varlıklar \> Tüm varlıklar** (veya **Etkin varlıklar**'ı) seçin.
1. Sabit kıymeti bulun ve açın.
1. **Sabit kıymet** hızlı sekmesinde, **İşlem yapılacak yerleşim** alanındaki değeri temizleyin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
