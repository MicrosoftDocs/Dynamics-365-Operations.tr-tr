---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (16 Ekim 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462801"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (16 Ekim 2018)

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
- Personel self servisinde gösterilen bir kurs için Dynamics 365 Talent kaydı artık tarihteki saat dilimi farkını uyguluyor.
- Excel dosyaları, **Personel Varlığı** kullanılarak artık hatasız şekilde birden çok kez içe aktarılır.

## <a name="known-issue"></a>Bilinen sorun

- **Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir. 
- **Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun. **Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır. (Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]