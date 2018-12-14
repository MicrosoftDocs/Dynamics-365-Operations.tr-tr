---
title: "Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (27 Kasım 2018)"
description: "Bu konuda, Microsoft Dynamics 365 for Talent Core HR'deki yeni veya değişen özellikler açıklanmaktadır."
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 48e2eea2cc986edc49d5192945c3d913c3bb9756
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a>Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (27 Kasım 2018)

[!include [banner](includes/banner.md)]

**Derleme 8.1.2064**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.


## <a name="changes"></a>Değişiklikler

### <a name="unable-to-create-a-note-in-case-management"></a>Servis Talebi Yönetiminde not oluşturulamıyor

Servis Talebi Yönetimi servis talebi günlüğünde bir not oluşturmaya veya düzenlemeye çalışırken oluşan bir hata için bir değişim yapıldı.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Analytics sekmesinde, ücret çalışma alanında yanlış yazılmış sözcük 

Ücret çalışma alanında, ücret analizi çizelgesinde 'Etnik Köken' kelimesinin yazılışını düzeltmek için bir değişiklik yapıldı.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Çalışan self servis çalışma alanı, bir kullanıcı bir çalışana atanmamış olduğunda görüntülenmiyor. 

**Çalışan self servis** çalışma alanı, bir çalışana atanmamış bir kullanıcı için başlangıçta ilk sayfa olarak seçildiyse bir değişiklik yapıldı. Bu durumda, varsayılan pano görüntülenir.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Bırakma ve Devamsızlık hatası: Bir nesne referansı, bir nesnenin örneğine ayarlanmadı

**Bana atanmış çalışma öğeleri** listesinde, bırakma ve devamsızlık kayıtları onaylandıktan sonra, Bırakma ve Devamsızlıkta bu hatayı düzeltmek için değişiklikler yapıldı.

### <a name="unable-to-recall-an-image-workflow"></a>Bir resim iş akışı çağrılamıyor

Bir resim iş akışını geri çağırdıktan sonra, iş akışı "iptal edildi" olarak ayarlanır ve mevcut talep çalışan self servis çalışma alanında silinebilir.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Geri işe alınan çalışanlar ve yükleniciler, sonlandırmadan sonra birden fazla kez gözükmektedir 

Bu güncelleştirme ile, işine son verildikten sonra işe tekrar alınan çalışanlar çıkılan listede yalnızca bir kez görüntülenir. 

## <a name="known-issue"></a>Bilinen sorun

- **Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir. 
- **Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun. **Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır. (Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)

