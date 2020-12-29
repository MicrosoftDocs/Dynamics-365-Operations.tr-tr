---
title: Kıymet yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde kıymet yaşam döngüsü durumları ve yaşam döngüsü modelleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566036c6361194d910a0fc34bd5d72147585ec4f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439204"
---
# <a name="asset-lifecycle-states"></a>Kıymet yaşam döngüsü durumları

[!include [banner](../../includes/banner.md)]

 

Bu konuda Kıymet Yönetimi'nde kıymet yaşam döngüsü durumları ve yaşam döngüsü modelleri açıklanmaktadır. Kıymet yaşam döngüsü durumları kıymetin etkin mi yoksa devre dışı mı olduğunu tanımlamak için kullanılır. Örneğin, **Oluşturuldu**, **Etkin** ve **Sonlandırıldı** gibi kıymet yaşam döngüsü durumları ayarlayabilirsiniz.

> [!NOTE]
> - Talep yaşam döngüsü durumları kıymet yaşam döngüsü durumlarına bağlanır. Bu nedenle bir talep yeni talep yaşam döngüsü durumuna değiştirildiğinde, talebe iliştirilmiş kıymet yeni kıymet yaşam döngüsü durumuna değiştirilir. Örneğin bir talebin yaşam döngüsü durumu **Gelen** olarak değiştirilirse, iliştirilmiş kıymetin yaşam döngüsü durumu **Kıymet yaşam döngüsü durumu modelleri** sayfasının **Kıymet yaşam döngüsü durumu** hızlı sekmesindeki **Gelen yaşam döngüsü durumu** alanında seçili yaşam döngüsü durumuna değiştirilir. 


Kıymet yaşam döngüsü durumları kıymet yaşam döngüsü modellerinde ayarlanabilir. Buradan çeşitli kıymet türleri için gerekli yaşam döngüsü durumlarını tanımlayabilirsiniz. Önce yaşam döngüsü durumlarını ayarlayın. Daha sonra bir yaşam döngüsü modeli oluşturun ve bu model için yaşam döngüsü durumlarını seçin.

1. **Kıymet yönetimi** \> **Kurulum** \> **Kıymetler** \> **Yaşam döngüsü durumları**'nı seçin.
2. Yeni bir kıymet yaşam döngüsü durumu oluşturmak için **Yeni**'yi seçin.
3. **Yaşam döngüsü durumu** alanında yaşam döngüsü durumu kimliğini girin.
4. **Ad** alanında, bir açıklama girin.

    **Yaşam döngüsü modelleri** alanı kıymet yaşam döngüsü durumunu kullanan kıymet yaşam döngüsü modellerinin sayısını gösterir.

5. Bu yaşam döngüsü durumunun etkin yaşam döngüsü durumunda olması gerekiyorsa (yani bu yaşam döngüsü durumunki kıymetler için iş emirleri oluşturulabilecekse) **Etkin** seçeneğini **Evet** olarak ayarlayın.
6. **Oluşturuldu** yaşam döngüsü durumunda bir kıymeti olan açık kıymet takvim satılarının bu yaşam döngüsü durumundayken silinmeleri gerekiyorsa **Açık takvim satırlarını sil** seçeneğini **Evet** olarak ayarlayın. Bu ayar, artık kıymetle ilgili olmayan açık bakım zamanlamalarını temizlemek istediğinizde (örneğin kıymet artık etkin olmadığında) yararlıdır.

> [!NOTE]
> Kıymet yaşam döngüsü durumları, kıymet yaşam döngüsü modelleri ve kıymet türleri ilişkilidir. Bunlar iş emri yaşam döngüsü durumları, iş emri yaşam döngüsü modelleri ve iş emri türleri ile aynı şekilde kullanılır. 


Gerekli kıymet yaşam döngüsü durumlarını oluşturduktan sonra kıymet yaşam döngüsü modellerinde yaşam döngüsü durumlarını ayarlayabilirsiniz.

1. **Kıymet yönetimi** \> **Kurulum** \> **kıymetler** \> **yaşam döngüsü modelleri**'ni seçin.
2. Yeni bir kıymet yaşam döngüsü modeli oluşturmak için **Yeni**'yi seçin.
3. **Yaşam döngüsü modeli** alanında yaşam döngüsü modeli kimliğini girin.
4. **Ad** alanında, bir açıklama girin.

    **Yaşam döngüsü durumları** alanı kıymet yaşam döngüsü modelinde seçili kıymet yaşam döngüsü durumlarının sayısını gösterir. **Kıymet türleri** alanı yaşam döngüsü modelini kullanan kıymet türlerinin sayısını gösterir.

5. **Yaşam döngüsü durumları** hızlı sekmesinde kıymet yaşam döngüsü modeline eklenmesi gereken kıymet yaşam döngüsü durumlarını seçin:

    - Modelde bir yaşam döngüsü durumu kullanmak için durumu **Kalan yaşam döngüsü durumları** bölümünden seçin ve sağ ok düğmesini ![Sağ ok](media/15-setup-for-objects.png) seçerek durumu **Seçili yaşam döngüsü durumları** bölümüne taşıyın.
    - Modelde tüm kullanılabilir yaşam döngüsü durumlarını kullanmak için **Tüm kullanılabilir yaşam döngüsü durumları** düğmesini ![Tüm kullanılabilir yaşam döngüsü durumları](media/20-setup-for-objects.png) seçin. Tüm yaşam döngüsü durumları **Seçili yaşam döngüsü durumları** bölümüne aktarılır.
    - Modelden bir yaşam döngüsü durumunu kaldırmak için durumu **seçili yaşam döngüsü durumları** bölümünden seçin ve sol ok düğmesini ![Sol ok](media/16-setup-for-objects.png) seçerek durumu **Kalan yaşam döngüsü durumları** bölümüne taşıyın.

6. Seçili yaşam döngüsü durumunu takip edebilecek kıymet yaşam döngüsü durumlarını tanımlamak için **Yaşam döngüsü durumu güncelleştirmeleri**'ni seçin.
7. Onarım için aldığınız kıymetleri işlerken **Kıymet durumu** hızlı sekmesini kullanın. **Gelen/giden** bölümünde onarım için aldığınız bir kıymetin iş akışını göstermek için kıymet yaşam döngüsü durumlarını seçebilirsiniz. Müşterilere veya departmanlara ödünç kıymet sunuyorsanız **Ödünç verilenler** bölümünde ödünç verilen kıymetler için yaşam döngüsü durumlarını seçebilirsiniz.
