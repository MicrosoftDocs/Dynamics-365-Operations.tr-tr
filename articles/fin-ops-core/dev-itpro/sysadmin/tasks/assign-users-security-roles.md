---
title: Kullanıcıları güvenlik rollerine atama
description: Finance and Operations uygulamalarına erişim sağlamak için kullanıcıların güvenlik rollerine atanmış olmaları gerekir.
author: Peakerbl
ms.date: 02/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36874b996cc5708f6fd7fbc45251f3066b5b1c97
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105550"
---
# <a name="manage-users-and-security-roles"></a>Kullanıcıları ve güvenlik rollerini yönetme

[!include [banner](../../includes/banner.md)]

Finans ve Operasyon uygulamalarında ortak yetenekler dışında herhangi bir şey kullanmak için, kullanıcıların güvenlik rollerine atanması gerekir. Kuralları ve iş verilerini temel alarak kullanıcıları rollere otomatik olarak atayabilir, kullanıcıları otomatik rol atama dışında tutabilir veya kullanıcıları rollere el ile ekleyebilirsiniz.

## <a name="automatically-assign-users-to-roles"></a>Kullanıcıları rollere otomatik olarak ata
Bu yordam sistem yöneticilerinin kullanıcıları iş verilerine dayalı olarak rollere otomatik olarak nasıl atayabileceklerini açıklar. 
1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.
2. Ağaçta, 'Muhasebe yöneticisi' seçin. Kuralı yapılandırmak istediğiniz rolü seçin. Bu örnekte, Muhasebe yöneticisi'ni seçin. 
3. İletişim kutusu menüsünü açmak için **Kural ekle**'yi seçin.
4. **Sorgu seçin** listesinde, istenen kaydı bulun ve seçin. Bu kuralda kullanılacak sorguyu seçin.  
5. **Üyelik kuralı adı** listesinde, seçili satırdaki bağlantıya tıklayın.
6. **Sorguyu düzenle**'yi seçin. Sorguyu gerektiği gibi düzenleyin.  
7. **Tamam**'ı seçin.
8. **Otomatik rol atamayı çalıştır**'ı seçin.
9. **Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin (ideal olarak ayrı bir tarayıcı sekmesinde).
10. Rol atama sorgusunun doğru olduğunu onaylamak için çeşitli kullanıcılara atanan rolleri gözden geçirin. Gerekirse ayarlayın ve yeniden çalıştırın.

## <a name="exclude-users-from-automatic-role-assignment"></a>Kullanıcıları otomatik rol atamasının dışında bırakmak
Bu yordamda kullanıcıların otomatik rol atamasından nasıl hariç tutulacağı açıklanmaktadır.

1. Sayfayı kapatın.
2. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.
3. Ağaçta, 'Muhasebe yöneticisi' seçin. Bir rol seçin. Bu örnek için, Muhasebe yöneticisi'ni seçin.  
4. **Role atanmış kullanıcılar** menüsünde, **Kullanıcıları el ile ata/dışarıda tut**'u seçin.
5. **Kullanıcıları role atayın veya rol dışında bırakın** listesinde, seçili satırları işaretleyin. Bir kullanıcı seçin.  
6. **Eylem bölmesi**'nde, **Rol dışında bırakın**'ı seçin.
7. Seçili kullanıcıları rolün dışında bırakmak için **Rol dışında bırak**'ı seçin. Dışarıda bırakmaları kaldırmak için, hariç tutulma durumunu kaldırmak istediğiniz kullanıcıları seçin ve sonra **Durumu sıfırla**'ya tıklayın. Bir kullanıcının durumunu sıfırlayarak bir hariç tutmayı kaldırdığınızda, kullanıcının rolü otomatik olarak atanır. Ancak, durumunu sıfırladığınızda, kullanıcı hemen role atanmaz veya rolden hariç tutulmaz. Bunun yerine kullanıcı otomatik rol atama bir sonraki çalıştığında rolüne eklenir veya çıkartılır.  

## <a name="manually-assign-users-to-roles"></a>Kullanıcıları rollere el ile atama
Güvenlik rollerine el ile atanan kullanıcıların yönetici tarafından el ile kaldırılması gerekir. Bu kullanıcılar otomatik rol ataması kuralları tarafından rollerden kaldırılmaz.

1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.
2. Ağaçta bir rol seçin, **Role atanmış kullanıcılar** menüsünde, **Kullanıcıları el ile ata / dışarıda tut**'u seçin.
4. **Kullanıcıları role ata veya rolün dışında tut**'ta, role atanmamış olan kullanıcılar **Atama modu** **Hiçbiri** olarak listelenir. Role atanması gereken bir veya daha fazla kullanıcı seçin.
5. **Eylem bölmesi**'nde, **Role ata**'yı seçin. **Atama modu** **El ile** olarak güncelleştirilir ve kullanıcılara atanmış yeni bir rol bulunur.

## <a name="manually-remove-users-from-roles"></a>Kullanıcıları rollerden el ile kaldırma
Güvenlik rollerine el ile atanan kullanıcıların yönetici tarafından el ile kaldırılması gerekir. Bu kullanıcılar otomatik rol ataması kuralları tarafından rollerden kaldırılmaz.

1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.
2. Bir kullanıcıyı kaldırmak için şu adımları izleyin:
   1. Ağaçta, bir rol seçin. 
   2. **Role atanan kullanıcılar** alanında, kaldırılması gereken kullanıcıyı seçin.
   3. **Kaldır**'ı seçin ve kullanıcı rolden kaldırılır.
3. Birden çok kullanıcıyı kaldırmak için şu adımları izleyin:
   1. Ağaçta, bir rol seçin. 
   2. **Role atanmış kullanıcılar** alanında, **Kullanıcıları el ile ata/dışarıda tut**'u seçin.
   3. **Kullanıcıları role ata veya rolün dışında tut** sayfasında role atanmamış olan kullanıcılar **Atama modu** sütununda **Hiçbiri** olarak listelenir. Rolün dışında bırakılması gereken kullanıcıları seçin.
   4. **Eylem bölmesi**'nde, **Rol dışında bırakın**'ı seçin. **Atama modu** sütunu **El ile** olarak güncelleştirilir ve kullanıcılar rolün dışında bırakılır.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
