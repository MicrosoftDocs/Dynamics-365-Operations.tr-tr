---
title: Organizasyon hiyerarşisine kanal ekleme
description: Bu makalede, Microsoft Dynamics 365 Commerce'te bir organizasyon hiyerarşisine nasıl kanal ekleneceği açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278610"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Organizasyon hiyerarşisine kanal ekleme


[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te bir organizasyon hiyerarşisine nasıl kanal ekleneceği açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Kanalların bir veya daha fazla organizasyon hiyerarşiyle ilişkilendirilmesi gerekir. Kanalları oluşturmadan önce, organizasyon hiyerarşilerinizin ayarlandığını onaylamanız gerekir.  

Organizasyon hiyerarşilerinin nasıl oluşturulacağı hakkında daha ayrıntılı bilgi için bkz. [Organizasyon hiyerarşileri](channels-org-hierarchies.md).

## <a name="select-a-hierarchy"></a>Hiyerarşi seçme

Hiyerarşi seçmek için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Kanal Kurulumu \> Organizasyon hiyerarşileri**'ne gidin.
1. Listeden, kanalı ekleyeceğiniz organizasyon hiyerarşisini seçin.
1. Eylem bölmesinde hiyerarşi ayrıntılarını görüntülemek için **Görüntüle**'yi seçin.

Aşağıdaki resim, seçili hiyerarşinin organizasyon hiyerarşisi ayrıntılarını gösteriyor.

![Seçili hiyerarşinin organizasyon hiyerarşisi ayrıntıları.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Bir hiyerarşi düğümüne kanal ekleme

Bir hiyerarşi düğümüne kanal eklemek için bu adımları izleyin.

1. Eylem bölmesinde, **Düzenle**'yi seçin.
1. Kanalın eklenmesini istediğiniz hiyerarşi düğümünü seçin ve **Ekle** açılır listesinden **Perakende Kanalı**'nı seçin. 
1. Eklenecek kanalı ve ardından **Tamam** düğmesini seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem bölmesinde, **Yayımla** 'yı seçin ve bu eylemin hemen yürürlüğe girmesini sağlamak için geçmiş bir **Yürürlük tarihi** girin.

Aşağıdaki resimde, hiyerarşi düğümüne eklenecek kanalın nasıl seçildiği gösteriliyor.

![Hiyerarşi düğümüne eklenecek kanalı seçme.](media/channel-add-to-org-hierarchy-2.png)

Aşağıdaki resim, çeşitli kanalların ekli olduğu bir hiyerarşiyi gösteriyor.

![Çeşitli kanalların eklendiği bir hiyerarşi.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Kuruluş hiyerarşinizi planlama](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organizasyon hiyerarşileri](channels-org-hierarchies.md)

[Perakende kanalını ayarlama](channel-setup-retail.md)
    
[Çevrimiçi kanal ayarlama](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
