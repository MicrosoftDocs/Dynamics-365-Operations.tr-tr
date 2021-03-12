---
title: Kuruluş hiyerarşilerini ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te organizasyon hiyerarşilerinin nasıl ayarlanacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997787"
---
# <a name="set-up-organization-hierarchies"></a>Kuruluş hiyerarşilerini ayarlama


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te organizasyon hiyerarşilerinin nasıl ayarlanacağı açıklanmaktadır.

## <a name="overview"></a>Özet

Kanalları oluşturmadan önce, organizasyon hiyerarşilerinizi ayarlandığınızdan emin olmanız gerekir.

İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyon hiyerarşilerini kullanabilirsiniz. Örneğin, vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz. Ardından, yasal olarak gerekmeyen ama dahili raporlama için kullanılan mali bilgileri raporlamak için başka bir hiyerarşi oluşturabilirsiniz.

Bir organizasyon hiyerarşisi oluşturmadan önce organizasyonları oluşturmanız gerekir. Daha fazla bilgi için bkz. [Tüzel kişilikleri oluşturma](channels-legal-entities.md) veya [İşletme birimlerini oluşturma](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)".


Daha fazla bilgi edinmek için aşağıdaki konulara bakın.
- [Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Organizasyon hiyerarşinizi planlama](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Kuruluş hiyerarşisi oluşturma](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Kuruluş hiyerarşisi oluşturma

Bir organizasyon hiyerarşisi oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Kanal Kurulumu \> Organizasyon hiyerarşileri**'ne gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ad** alanına bir değer girin.
1. **Amaç** bölümünde, **Amaç ata**'yı seçin.
1. Listede, istenen kaydı bulun ve seçin. Organizasyon hiyerarşinize atanacak bir amaç seçin.
1. **Atanan hiyerarşiler** bölümünde, **Ekle**'yi seçin.
1. Listede, seçili satırı işaretleyin. Yeni oluşturduğunuz hiyerarşiyi bulun.
1. **Tamam**'ı seçin.

Aşağıdaki resimde, hayali "Adventure Works" mağazaları kümesi için oluşturulmuş örnek bir organizasyon hiyerarşisi gösterilmektedir.

![Örnek organizasyon hiyerarşisi oluşturma](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Hiyerarşiye organizasyonlar ekleme

Bir hiyerarşiye organizasyonlar eklemek için bu adımları izleyin.

1. Listede, istenen kaydı bulun ve seçin. Hiyerarşinizi seçin.
1. Eylem bölmesinde, **Görüntüle**'yi seçin.
1. Gerekirse kuruluşlar ekleyin.
1. Bir organizasyon eklemek için **Düzenle**'yi ve ardından **Ekle** 'yi seçin. Değişiklikleri tamamladıktan sonra bir taslak kaydedebilir ve değişiklikleri yayımlayabilirsiniz.

Aşağıdaki resimde, "Mall", "Outlet", "Çevrimiçi" ve "Çağrı Merkezi" kanalları için dört maliyet merkezi yer alan hiyerarşi köküne eklenmiş bir tüzel kişilik gösterilmektedir. Bunun ardından, çeşitli perakende ve çağrı merkezi kanalları ve çevrimiçi kanallar her birine eklenebilir.

![Örnek hiyerarşi tasarımcısı](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Kuruluş hiyerarşinizi planlama](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Tüzel kişilik oluşturma](channels-legal-entities.md)

[Çalışma birimleri oluşturma](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)
