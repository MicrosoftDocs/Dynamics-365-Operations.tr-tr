---
title: "Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (Ekim 16, 2018)"
description: "Bu konuda, Microsoft Dynamics 365 for Talent Core HR'deki yeni veya değişen özellikler açıklanmaktadır."
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 2eb46f436305a4c81ea99553e4dc07288ee74008
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.contentlocale: tr-tr
ms.lasthandoff: 10/22/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a>Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (19 Ekim 2018)

[!include[banner](includes/banner.md)]

**Derleme 8.1.1067**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.

## <a name="allow-managers-to-update-time-off-requests"></a>Yöneticilerin izin istekleri güncelleştirmesine izin ver

Personel izin isteklerinin, iş akışında onaylandıktan sonra güncelleştirilmesi gerekebilir. Çoğu durumda, yönetici bu güncelleştirmeleri personelin adına sağlar. Bu yeni özellik, yöneticilere personelleri adına izini güncelleştirme ve izin isteklerini iptal etme özelliği sunar. Bu özellik **Adına iş** parametresi tarafından kontrol edilir ve **İnsan kaynağı parametreleri** sayfasından ayarlanabilir. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>İK'nın izin istekleri güncelleştirmesine izin ver

Yukarıdaki özelliği benzer şekilde, personel izin isteklerinin, iş akışında onaylanmasından sonra İK tarafından güncellenmesi gerekebilir. Bu özellik, İK kullanıcılarının izin isteklerini güncelleştirmesini sağlar. Özellik, **Kişiler** çalışma alanında ve **Çalışan** sayfasında **İzin süresini görüntüle** adlı yeni seçenek kullanılarak etkinleştirilir. Bu sayfalarda, İK kullanıcıları isteklerini görüntüleyebilir ve izin hareketlerini güncelleştirebilir; aynı yöneticilerin bu eylemleri yapabildiği gibi.

Bu işlevlere erişimi kontrol eden güvenlik görevi aşağıdaki gibidir:
- Görev: Çalışana özel izin ve devamsızlık işlemlerini koru.
- Ayrıcalık: Tüm çalışanlar için izin ve devamsızlık isteklerini koru.

## <a name="other-changes"></a>Diğer değişimler
Aşağıdaki güncelleştirmeler bu sürümde yapıldı:
- Çalışan işe alma eylemleri, artık **İş akışı tamam** durumunda "sıkışmasın" diye değiştirildi.
- Peronsel kaydı, artık çalışma başlangıç tarihi olmadan oluşturulur.
- Personel self servite gösterilen bir kurs için Dynamics 365 Talent kaydı, artık tarihteki zaman dilimi farkını uygular.
- Excel dosyaları, **Personel Varlığı** kullanılarak artık hatasız şekilde birden çok kez içe aktarılır.

## <a name="known-issue"></a>Bilinen sorun

- **Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir. 
- **Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun. **Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır. (Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)

