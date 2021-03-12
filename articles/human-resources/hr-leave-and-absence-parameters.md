---
title: Bırakma ve devamsızlık parametrelerini konfigüre et
description: Dynamics 365 Human Resources'ta izin ve devamsızlık için insan kaynakları parametrelerini tanımlayın.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "4997113"
---
# <a name="configure-leave-and-absence-parameters"></a>Bırakma ve devamsızlık parametrelerini konfigüre et

Dynamics 365 Human Resources'ta , izin ve devamsızlık planlarını ayarlamadan önce, aşağıdakiler dahil olmak üzere ilgili tüm insan kaynakları parametrelerinin ayarlarını doğrulamak iyi bir fikirdir.

- İzin talepleri için numara serisi
- Aile sağlık ve izin Yasası (FMLA) ayarları
- İzin ve devamsızlık talepleri için çalışan self servis ayarları
- İzin ve devamsızlık parametreleri

## <a name="view-and-change-human-resources-parameters"></a>İnsan kaynakları parametrelerini görüntüle ve değiştir

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.

2. **Kurulum**'un altında, **İnsan kaynakları parametrelerini** seçin.

3. **Numara serileri** sekmesinde, **izin talebi kodunun** **numara serisi kodunu** doğrulayın ve gerekli değişiklikleri yapın. Bu ayar, isteklere izin vermek üzere otomatik olarak kimlik atamak için kullanılan sırayı belirler.

4. **FMLA** sekmesinde, FMLA ayarlarını doğrulayın ve gerektiği şekilde değiştirin.

5. **Çalışan self servis** sekmesinde, yöneticilerin çalışanlar adına bırakma ve devamsızlık talepleri girip giremeyeceğini belirtin.

7. **Kaydet**'i seçin.

>[!IMPORTANT]
>Şirketler arasında ayrılma ve devamsızlıkların görüntülenmesi Şu anda önizleme modunda. Bırak ve devamsızlık seçeneğini görüntülemek için bunu **korumalı alan** ortamınızda etkinleştirmeniz gerekir. Önizleme özelliklerini etkinleştirme hakkında daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>İnsan kaynakları paylaşılan parametrelerini görüntüle ve değiştir

1. **Personel yönetimi** sayfasında, **Bağlantılar** sekmesini seçin.

2. **Kurulum**'un altında, **İnsan kaynakları paylaşılan parametrelerini** seçin.

3. **Gelişmiş erişim** sekmesinde, Şirket genelinde görüntülenenler görünümüne izin vermek için **şirketler arası bırak görünümünü etkinleştir** için **Evet**'i seçin.

4. **Kaydet**'i seçin.

## <a name="view-and-change-leave-and-absence-parameters"></a>İzin ve devamsızlık parametrelerini görüntüleme ve değiştirme

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.

2. **Kurulum** altında, **İzin ve devamsızlık parametreleri**'ni seçin.

3. **Genel** sekmesinde, aşağıdaki parametreleri ayarlayın:
 
    - **İzin ve devamsızlık birimini** saat veya gün olarak ayarlayın. Gün olarak ayarlarsanız, çalışanların izin isteklerinde günün ilk veya ikinci yarısını seçmelerine izin vermek için **Yarım tüm tanımını etkinleştir**'i seçebilirsiniz. 

    - Tahakkuk oranlarının hizmet ayları kullanılarak izin planları için geçerli olacağı zamanı ayarlamak için **Hizmet ayları geçerlilik tarihi**'ni seçin.

    - Bugün veya tahakkuk dönemi itibarıyla bakiyeyi görüntülemek için **Bakiye hesaplaması**'nı seçin. **Bugün itibarıyla bakiye**'yi seçerseniz, bakiye bugün itibarıyla tahakkukların, ayarlamaların ve isteklerin toplamını görüntüler. **Tahakkuk dönemi itibarıyla bakiye**'yi seçerseniz bakiye, izin planındaki sıklık tarafından tanımlanan tahakkuk dönemi itibarıyla tüm tahakkukların, ayarlamaların ve isteklerin toplamını görüntüler. 

    - Sona erme tarihini ilerletme toplu işi için başlangıç zamanını belirleyin.  
    
    - **Personelin izin satın almasına izin ver** ve **Personelin izin satmasına izin ver** için **Evet**'i seçin. Bu seçenekler için **Evet**'i seçerseniz izin satın alma ve satma ilkeleri oluşturabilir ve personelin izin satın alma ve satma istekleri göndermesine olanak tanıyabilirsiniz.

## <a name="configure-calendar-parameters"></a>Takvim parametrelerini yapılandırma

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.

2. **Kurulum** altında, **İzin ve devamsızlık parametreleri**'ni seçin.

3. **Takvim** sekmesinde, takvim ayarlarını gerektiği şekilde değiştirin.

4. **Kaydet**'i seçin.

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
