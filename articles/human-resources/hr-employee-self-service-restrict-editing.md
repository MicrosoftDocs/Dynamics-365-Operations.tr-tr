---
title: Kişisel bilgilerin düzenlenmesini kısıtlama
description: Çalışanların Dynamics 365 Human Resources'daki iletişim bilgilerini düzenlemelerini kısıtlayın.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e3eeb66d4f32b1fea1a43fff9f5b09d87d1f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018721"
---
# <a name="restrict-editing-of-personal-information"></a>Kişisel bilgilerin düzenlenmesini kısıtlama

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Bu konuda, çalışanların Dynamics 365 Human Resources'da iletişim bilgilerini düzenlemesinin nasıl kısıtlanacağı açıklanmaktadır. Çalışanların iş konumları veya e-posta adresleri gibi belirli iletişim bilgilerini düzenlemelerini engellemek isteyebilirsiniz.

> [!NOTE]
> Bu özelliği kullanmak için önce Özellik yönetiminde **(Önizleme) Belirli amaçlar için çalışanların adres ve iletişim bilgilerini eklemesini veya düzenlemesini kısıtlama** özelliğini etkinleştirmeniz gerekir. Önizleme özelliklerini etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).<br><br>![Önizleme özelliğini etkinleştir](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Bir çalışanın ekleyebileceği veya düzenleyebileceği bilgileri seçme

1. Human Resources'ta **Personel yönetimi**'ni, **Bağlantılar**'ı ve sonra **İnsan kaynakları parametreleri**'ni seçin.

   ![Human Resources parametrelerini yapılandır'a gidin](./media/hr-employee-self-service-human-resources-parameters.png)

2. **Human Resources parametreleri** sayfasında **Çalışan self servisi** sekmesini seçin.

   ![Employee Self Service'i seçme](./media/hr-employee-self-service-tab.png)

3. **Çalışan self servisi** sekmesinde, **Adres ve iletişim bilgileri** bölümünde çalışanların eklemesini veya düzenlemesini istemediğiniz tüm bilgilerin işaretini kaldırın. Bu örnekte, **İş** iletişim bilgilerinin işaretini kaldırdık.

   ![İş iletişim bilgileri için düzenlemeyi kısıtlama](./media/hr-employee-self-service-restrict-business.png)

4. **Kaydet**'i seçin.

   ![Değişiklikleri kaydet](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Çalışan deneyimi

Çalışanların iletişim bilgilerini eklemesini veya düzenlemesini kısıtladıktan sonra çalışanlar bilgileri görebilir ancak değiştiremez.

Bu örnekte, çalışanların **İş** iletişim bilgilerini düzenlemelerinin kısıtlandı ancak Çalışan self servisi'ndeki bilgileri görmeye devam edebilir:

![İş iletişim bilgilerini görüntüleme](./media/hr-employee-self-service-restrict-view.png)

Ancak iş iletişim bilgilerini seçtiklerinde, **Adresi düzenle** bölmesi salt okunur olarak görünür ve alanların hiçbirini değiştiremezler.

![İş iletişim bilgileri salt okunur olarak görüntülenir](./media/hr-employee-self-service-restrict-read-only.png)

Ayrıca, yeni adres eklemek için **Ekle**'yi seçerlerse **Amaç** açılan kutusundan **İş**'i seçemezler.

![Çalışan İş adresi ekleyemiyor](./media/hr-employee-self-service-restrict-add.png)

Çalışanlar, **Kişisel bilgiler** sayfasında **İletişim bilgileri**'ni seçip yeni bir adres eklediklerinde de aynı deneyimi yaşarlar. **Amaç** açılan kutusu yalnızca ekleyebilecekleri bilgi türlerini görüntüler. 

![Çalışan Amaç açılan menüsünde İş'i seçemiyor](./media/hr-employee-self-service-restrict-purpose.png)

**İletişim bilgileri** artık kılavuzda **Amaç**'ı gösterir.

![İletişim bilgileri kılavuzunda Amaç gösteriliyor](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Ayrıca bkz.

[Personel ve Yönetici self servisine genel bakış](hr-employee-manager-self-service-overview.md)<br>
[Human Resources parametrelerini yapılandırma](hr-setup-parameters.md)<br>
[Kişisel bilgileri düzenle](hr-employee-manager-self-service-edit-personal-information.md)