---
title: Amortisman defterleri ayarlama (Mayıs 2016)
description: Bu görev kılavuzunda yeni bir amortisman defteri oluşturulup bir sabit kıymet grubuyla ilişkilendirilecek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186912"
---
# <a name="set-up-depreciation-books-may-2016"></a>Amortisman defterleri ayarlama (Mayıs 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda yeni bir amortisman defteri oluşturulup bir sabit kıymet grubuyla ilişkilendirilecek.  Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.


## <a name="create-a-depreciation-book"></a>Amortisman defteri oluşturun
1. Sabit kıymetler > Kurulum > Amortisman defterleri'ne gidin.
2. Yeni'ye tıklayın.
3. Amortisman defteri alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Amortismanı hesapla onay kutusunu işaretleyin veya kutunun işaretini kaldırın.
6. Amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. Listede, istediğiniz amortisman profilini bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Alternatif amortisman profili alanında, açılır menü düğmesine tıklayarak aramayı açın.
10. Listede, istediğiniz amortisman profilini seçin.
11. Listede, seçili satırdaki bağlantıya tıklayın.
    * Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır. Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.  
12. Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur onay kutusunu işaretleyin veya kutunun işaretini kaldırın.
13. Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.
14. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Amortisman defterini bir sabit kıymet grubuyla ilişkilendirin.
1. Sabit kıymet grupları'na tıklayın.
2. Sabit kıymet grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Amortisman yöntemi alanında bir seçenek belirtin.
6. Servis ömrü alanına bir sayı girin.
    * Amortisman dönemleri alanı değerinin Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.  

