---
title: Sayfaları ve parçaları geri döndürmek için sürüm geçmişini görüntüleme
description: Bu makalede, sayfa ve parçaların sürüm geçmişinin nasıl görüntüleneceği ve Microsoft Dynamics 365 Commerce site oluşturucusunda eski sürümlere nasıl geri döndürüleceği açıklanır.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fa2ecdd9d9bc7e60b279d850573b5caa6df2c659
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183685"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Sayfaları ve parçaları geri döndürmek için sürüm geçmişini görüntüleme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu makalede, sayfa ve parçaların sürüm geçmişinin nasıl görüntüleneceği ve Microsoft Dynamics 365 Commerce site oluşturucusunda eski sürümlere nasıl geri döndürüleceği açıklanır.

Commerce süte oluşturucusu, sayfa ve parçaların geçmişini görüntülemenizi ve gerekirse belgeyi eski bir sürümüne geri döndürmenizi sağlar. Belge açıkken **Sürüm geçmişi** iletişim kutusunu açmak için komut çubuğunda **Geçmişi göster** seçeneğini belirleyebilirsiniz. **Sürüm** sekmesinde sayfa ve parçanın tüm sürümleri ve kaydedilen etkinlikler listelenir. Sonrasında listeden belgenin eski bir sürümünü seçebilir, bu sürümü önizleyebilir ve geçerli sürüm olarak geri yükleyebilirsiniz. İletişim kutusunun **Etkinlik** sekmesinde kaydet, yayımla veya yayımdan kaldır etkinlikleri de dahil olmak üzere belgenin tüm etkinlik geçmişi listelenir.

> [!NOTE]
> Site yazarı, belge üzerinde her değişiklik yaptığında ve **Düzenlemeyi bitir** seçeneğini belirlediğinde belgenin yeni bir sürümü oluşturulur. 

Sayfa veya parçanın sürüm geçmişini görüntülemek ve eski bir sürümüne döndürmek aşağıdaki adımları izleyin.

1. Site oluşturucusunda sürüm geçmişini görüntülemek istediğiniz sayfa veya parçayı açın.
1. Komut çubuğunda **Geçmişi göster** seçeneğini belirleyin.

    ![Geçmişi göster düğmesi.](./media/version-history-1.png)

1. **Sürüm geçmişi** iletişim kutusundaki **Sürüm** sekmesinde belgenin eski bir sürümünü seçin. Sağdaki özellikler bölmesi, seçili sürümün küçük resim görünümünü ve kim tarafından ve ne zaman değiştirildiğini gösterir.

    ![Sürüm geçmişi liste görünümü.](./media/version-history-2.png)

1. Belgenin seçili sürümünün tamamen işlenmiş önizlemesini görmek için **Önizleme** seçeneğini belirleyin. Önizlemeyi kapatarak **Sürüm geçmişi** iletişim kutusuna dönmek için **Önizlemeden çık** seçeneğini belirleyin.
1. Belgenin eski bir sürümünü geri yüklemek için **Sürüm** sekmesindeki listeden bu sürümü seçin ve ardından **Geri yükle** seçeneğini belirleyin. **Sürümü geri yükle \<version number\>** ileti kutusu belirir ve geri yükleme eylemini onaylamanızı ister. 

    ![Geri yükleme düğmesi ve onay ileti kutusu.](./media/version-history-3.png)

1. Geri yükleme eylemine devam etmek için **Geri yükle** seçeneğini belirleyin. Site oluşturucu yenilenir ve sayfa veya parçanın geri yüklenen sürümünü gösterir.
1. Geri yüklenen sürümü yayımlamak için **Düzenlemeyi bitir**'i seçin, ardından **Yayımla**'yı seçin.
