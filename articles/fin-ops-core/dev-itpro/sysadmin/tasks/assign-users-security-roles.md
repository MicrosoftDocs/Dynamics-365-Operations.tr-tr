---
title: Kullanıcıları güvenlik rollerine atama
description: Finance and Operations uygulamalarına erişmek için kullanıcıların güvenlik rolleri atanmış olmalıdır.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
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
ms.openlocfilehash: 1a6d904ae3df23dd1c602cfdfecc40411aba5724
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569886"
---
# <a name="assign-users-to-security-roles"></a>Kullanıcıları güvenlik rollerine atama

[!include [banner](../../includes/banner.md)]

Finance and Operations uygulamalarında ortak yetenekler dışında herhangi bir şey kullanmak için, kullanıcıların güvenlik rollerine atanması gerekir. Kuralları ve iş verilerini temel alarak kullanıcıları rollere otomatik olarak atayabilir, kullanıcıları otomatik rol atama dışında tutabilir veya kullanıcıları rollere el ile ekleyebilirsiniz.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]